# Prozess Optimierung

>[!NOTE] Langsamer Seitenaufbau vermeiden
> Ausgang nach Programmierung der Landingpage
> > Request Timing Blocked: -1 ms DNS Resolution: 0 ms Connecting: 0 ms TLS Setup: 0 ms Sending: 0 ms ==**Waiting: 1.98 s**== Receiving:...
> 
> Das ist deutlich zu lange und sorgt für schlechte USability, da Nutzer durchschnittlich nach 200-500ms Ladezeiten schon die Webseite verlassen. Also gehts jetzt darum umzustrukturieren, Bottlenecks zu vermeiden und die Zeit zu reduzieren.

## Aktueller Stand
### Projektstruktur
![[Pasted image 20241003101851.png]]

### Verbindung zur DB

Verbindung zum Cluster in der MongoDB durch mongoose
``` 
/db.js
import mongoose from "mongoose";

const connect = async () => {
  try {
    await mongoose.connect(process.env.MONGODB_URI, {
      useNewUrlParser: true,
      useUnifiedTopology: true,
    });
    console.log("Mongo connection succesfull");
  } catch (error) {
    throw new Error("Error in connection to mongodb.");
  }
};

export default connect;
```

Modelle Fetchen die Information von der passenden Datenbank 
``` 
/models/Abstimmung.js
import mongoose from "mongoose";

const { Schema } = mongoose;

// Abstimmungsergebnis Schema for Abstimmung
const abstimmungsergebnisSchema = new Schema({
  ja_stimmen: {
    type: Number,
    default: null,
  },
  nein_stimmen: {
    type: Number,
    default: null,
  },
  enthalten_stimmen: {
    type: Number,
    default: null,
  },
});

// Teilnehmer Schema for Namentliche Abstimmungen
const teilnehmerSchema = new Schema({
  Name: {
    type: String,
    required: true,
  },
  Fraktion: {
    type: String,
    required: true,
  },
  Stimme: {
    type: String,
    enum: ["Ja", "Nein", "Enthaltung"],
    required: true,
  },
});

// Namentliche Abstimmungen Schema
const namentlicheAbstimmungenSchema = new Schema({
  Titel: {
    type: String,
    required: true,
  },
  Drucksache: {
    type: String,
    required: true,
  },
  Abstimmungsergebnis: abstimmungsergebnisSchema,
  Teilnehmer: [teilnehmerSchema],
});

// Antrag Schema for Anträge
const antragSchema = new Schema({
  istangenommen: {
    type: Boolean,
    required: true,
  },
  Titel: {
    type: String,
    required: true,
  },
  Drucksache: {
    type: String,
    required: true,
  },
  Fraktion: {
    type: String,
    required: true,
  },
  Seitenanzahl: {
    type: Number,
    required: true,
  },
  istneu: {
    type: Boolean,
    required: true,
  },
  TOP: {
    type: String,
    required: true,
  },

  Abstimmungsergebnis: abstimmungsergebnisSchema,
});

// Abstimmung Schema
const abstimmungSchema = new Schema({
  Tagung: {
    Tagungsnummer: {
      type: Number,
      required: true,
    },
    Sitzungsnummer: {
      type: Number,
      required: true,
    },
    Datum: {
      type: String,
      required: true,
    },
    Anträge: [antragSchema],
    NamentlicheAbstimmungen: [namentlicheAbstimmungenSchema],
  },
});

// Export the Abstimmung model
export default mongoose.models.Abstimmung ||
  mongoose.model("Abstimmung", abstimmungSchema);

```

``` 
/models/Sitzung.js
import mongoose from "mongoose";

const { Schema } = mongoose;

// Argument Schema
const argumentSchema = new Schema({
  argumentId: {
    type: Number,
    required: true,
  },
  argumentText: {
    type: String,
    required: true,
  },
  fraktion: {
    type: String,
    required: true,
  },
  source: {
    type: {
      type: String,
      enum: ["PDF", "Text"],
      required: true,
    },
    page: {
      type: Number,
      default: null,
    },
    url: {
      type: String,
      default: null,
    },
  },
  status: {
    type: String,
    enum: ["Pro", "Kontra"],
    required: true,
  },
});

// Fraktion Vote Schema
const fraktionVoteSchema = new Schema({
  name: {
    type: String,
    required: true,
  },
  stimmen: {
    type: Number,
    required: true,
  },
});

// Abstimmungsergebnis Schema
const abstimmungsergebnisSchema = new Schema({
  ja_stimmen: {
    type: Number,
    required: true,
  },
  nein_stimmen: {
    type: Number,
    required: true,
  },
  enthalten_stimmen: {
    type: Number,
    required: true,
  },
  fraktion_ja: [fraktionVoteSchema],
  fraktion_nein: [fraktionVoteSchema],
  status: {
    type: String,
    required: true,
  },
});

// Vorschlag Schema
const vorschlagSchema = new Schema({
  neueDrucksache: {
    type: String,
    required: true,
  },
  titel: {
    type: String,
    required: true,
  },
  verbesserungen: [
    {
      adjustmentId: {
        type: Number,
        required: true,
      },
      adjustment: {
        type: String,
        required: true,
      },
      fraktion: {
        type: String,
        required: true,
      },
    },
  ],
});

// Drucksache Schema
const drucksacheSchema = new Schema({
  drucksacheId: {
    type: Number,
    required: true,
  },
  nummer: {
    type: Number,
    required: true,
  },
  titel: {
    type: String,
    required: true,
  },
  kategorie: {
    type: String,
    required: true,
  },
  arguments: [argumentSchema],
  abstimmungsergebnis: abstimmungsergebnisSchema,
  vorschlaege: [vorschlagSchema],
  isNew: {
    type: Boolean,
    default: false,
  },
});

// Sitzung Schema
const sitzungSchema = new Schema(
  {
    sitzungId: {
      type: Number,
      required: true,
    },
    number: {
      type: Number,
      required: true,
    },
    datum: {
      type: String,
      required: true,
    },
    wahlperiode: {
      type: Number,
      required: true,
    },
    drucksachen: [drucksacheSchema],
  },
  { timestamps: true },
);

export default mongoose.models.Sitzung ||
  mongoose.model("Sitzung", sitzungSchema);
```

APIs sammeln die Informationen und stellen sie dem Front-End bereit.

```
/src/app/api/abstimmungen/routing.js
import { NextResponse } from "next/server";
import connect from "../../../../db";
import Abstimmung from "../../../../models/Abstimmung";

export const GET = async (request) => {
  try {
    await connect();
    const abstimmungen = await Abstimmung.find();

    return new NextResponse(JSON.stringify(abstimmungen), { status: 200 });
  } catch (error) {
    return new NextResponse("Error in fetching Sitzung" + error, {
      status: 500,
    });
  }
};

```

```
/src/app/api/sitzungen/routing.js
import { NextResponse } from "next/server";
import connect from "../../../../db";
import Sitzung from "../../../../models/Sitzung";

export const GET = async (request) => {
  try {
    await connect();
    const sitzungen = await Sitzung.find();

    return new NextResponse(JSON.stringify(sitzungen), { status: 200 });
  } catch (error) {
    return new NextResponse("Error in fetching Sitzung" + error, {
      status: 500,
    });
  }
};
```

> **Problem**:  
Jede API-Anfrage stellt eine separate Verbindung zur Datenbank her, was zu unnötigen Verbindungsaufbauten und längeren Ladezeiten führt. Dies erzeugt einen Flaschenhals, insbesondere wenn mehrere Anfragen gleichzeitig gestellt werden, da die Verbindungen nicht wiederverwendet werden.
>
>**Lösung**idee:  
>Statt für jede Anfrage eine neue Verbindung aufzubauen, wird nun eine zentrale Datenbankverbindung hergestellt und über alle APIs hinweg wiederverwendet. Dies reduziert den Overhead durch wiederholte Verbindungsaufbauten und beschleunigt die Antwortzeiten der APIs erheblich.
>

## Lösungsstrategie

>[!NOTE] Veränderungen und Neues
>**Struktur**
> - Modelle in den Source Ordner verschoben (Struktur und Übersichtlichkeit)
> - lib um Serververbindung zu erstellen
> - abstimmungsergebnisseSchemas um bestPractice besser umzusetzen
> 
> **Neues**
> -  Ordner: ../app/lib, ../models/schemas
> - Files: ../libs/connectDB.js, ../schemas/abstimmungsergebnisseSchema.js


### Neue Projektstruktur
![[Pasted image 20241003104138.png]]

### Verbindung zur DB

Verbindung zum Cluster in der MongoDB durch mongoose
``` 
/db.js
import mongoose from "mongoose";

const connect = async () => {
  try {
    await mongoose.connect(process.env.MONGODB_URI, {
      useNewUrlParser: true,
      useUnifiedTopology: true,
    });
    console.log("Mongo connection succesfull");
  } catch (error) {
    throw new Error("Error in connection to mongodb.");
  }
};

export default connect;
```

Verbindung über Mongoose aufbauen
```
src/lib/connectedDB.js
import mongoose from "mongoose";

let isConnected = false;

const connectDB = async () => {
  if (isConnected) return;

  try {
    await mongoose.connect(process.env.MONGODB_URI, {
      useNewUrlParser: true,
      useUnifiedTopology: true,
    });
    isConnected = true;
    console.log("Connected to MongoDB");
  } catch (error) {
    console.error("MongoDB connection error:", error);
  }
};

export default connectDB;

```

Modelle Fetchen die Information von der passenden Datenbank 
``` 
import mongoose from "mongoose";
import abstimmungsergebnisSchema from "./schemas/abstimmungsergebnisSchema";
const { Schema } = mongoose;

// Teilnehmer Schema for Namentliche Abstimmungen
const teilnehmerSchema = new Schema({
  Name: {
    type: String,
    required: true,
  },
  Fraktion: {
    type: String,
    required: true,
  },
  Stimme: {
    type: String,
    enum: ["Ja", "Nein", "Enthaltung"],
    required: true,
  },
});

// Namentliche Abstimmungen Schema
const namentlicheAbstimmungenSchema = new Schema({
  Titel: {
    type: String,
    required: true,
  },
  Drucksache: {
    type: String,
    required: true,
  },
  Abstimmungsergebnis: abstimmungsergebnisSchema,
  Teilnehmer: [teilnehmerSchema],
});

// Antrag Schema for Anträge
const antragSchema = new Schema({
  istangenommen: {
    type: Boolean,
    required: true,
  },
  Titel: {
    type: String,
    required: true,
  },
  Drucksache: {
    type: String,
    required: true,
  },
  Fraktion: {
    type: String,
    required: true,
  },
  Seitenanzahl: {
    type: Number,
    required: true,
  },
  istneu: {
    type: Boolean,
    required: true,
  },
  TOP: {
    type: String,
    required: true,
  },

  Abstimmungsergebnis: abstimmungsergebnisSchema,
});

// Abstimmung Schema
const abstimmungSchema = new Schema({
  Tagung: {
    Tagungsnummer: {
      type: Number,
      required: true,
    },
    Sitzungsnummer: {
      type: Number,
      required: true,
    },
    Datum: {
      type: String,
      required: true,
    },
    Anträge: [antragSchema],
    NamentlicheAbstimmungen: [namentlicheAbstimmungenSchema],
  },
});

// Export the Abstimmung model
export default mongoose.models.Abstimmung ||
  mongoose.model("Abstimmung", abstimmungSchema);


```

``` 
import mongoose from "mongoose";

const { Schema } = mongoose;

// Argument Schema
const argumentSchema = new Schema({
  argumentId: {
    type: Number,
    required: true,
  },
  argumentText: {
    type: String,
    required: true,
  },
  fraktion: {
    type: String,
    required: true,
  },
  source: {
    type: {
      type: String,
      enum: ["PDF", "Text"],
      required: true,
    },
    page: {
      type: Number,
      default: null,
    },
    url: {
      type: String,
      default: null,
    },
  },
  status: {
    type: String,
    enum: ["Pro", "Kontra"],
    required: true,
  },
});

// Fraktion Vote Schema
const fraktionVoteSchema = new Schema({
  name: {
    type: String,
    required: true,
  },
  stimmen: {
    type: Number,
    required: true,
  },
});

// Abstimmungsergebnis Schema
const abstimmungsergebnisSchema = new Schema({
  ja_stimmen: {
    type: Number,
    required: true,
  },
  nein_stimmen: {
    type: Number,
    required: true,
  },
  enthalten_stimmen: {
    type: Number,
    required: true,
  },
  fraktion_ja: [fraktionVoteSchema],
  fraktion_nein: [fraktionVoteSchema],
  status: {
    type: String,
    required: true,
  },
});

// Vorschlag Schema
const vorschlagSchema = new Schema({
  neueDrucksache: {
    type: String,
    required: true,
  },
  titel: {
    type: String,
    required: true,
  },
  verbesserungen: [
    {
      adjustmentId: {
        type: Number,
        required: true,
      },
      adjustment: {
        type: String,
        required: true,
      },
      fraktion: {
        type: String,
        required: true,
      },
    },
  ],
});

// Drucksache Schema
const drucksacheSchema = new Schema({
  drucksacheId: {
    type: Number,
    required: true,
  },
  nummer: {
    type: Number,
    required: true,
  },
  titel: {
    type: String,
    required: true,
  },
  kategorie: {
    type: String,
    required: true,
  },
  arguments: [argumentSchema],
  abstimmungsergebnis: abstimmungsergebnisSchema,
  vorschlaege: [vorschlagSchema],
  isNew: {
    type: Boolean,
    default: false,
  },
});

// Sitzung Schema
const sitzungSchema = new Schema(
  {
    sitzungId: {
      type: Number,
      required: true,
    },
    number: {
      type: Number,
      required: true,
    },
    datum: {
      type: String,
      required: true,
    },
    wahlperiode: {
      type: Number,
      required: true,
    },
    drucksachen: [drucksacheSchema],
  },
  { timestamps: true },
);

export default mongoose.models.Sitzung ||
  mongoose.model("Sitzung", sitzungSchema);

```

APIs sammeln die Informationen und stellen sie dem Front-End bereit.

```
/src/app/api/abstimmungen/routing.js
import { NextResponse } from "next/server";
import connect from "../../../../db";
import Abstimmung from "../../../../models/Abstimmung";

export const GET = async (request) => {
  try {
    await connect();
    const abstimmungen = await Abstimmung.find();

    return new NextResponse(JSON.stringify(abstimmungen), { status: 200 });
  } catch (error) {
    return new NextResponse("Error in fetching Sitzung" + error, {
      status: 500,
    });
  }
};

```

```
/src/app/api/sitzungen/routing.js
import { NextResponse } from "next/server";
import connect from "../../../../db";
import Sitzung from "../../../../models/Sitzung";

export const GET = async (request) => {
  try {
    await connect();
    const sitzungen = await Sitzung.find();

    return new NextResponse(JSON.stringify(sitzungen), { status: 200 });
  } catch (error) {
    return new NextResponse("Error in fetching Sitzung" + error, {
      status: 500,
    });
  }
};
```







>Perfomanceverbesserung: 
>$$\text{Prozentuale Reduzierung} = \left( \frac{1980 \, \text{ms} - 155 \, \text{ms}}{1980 \, \text{ms}} \right) \times 100 = \left( \frac{1825 \, \text{ms}}{1980 \, \text{ms}} \right) \times 100 = 92,17\%$$