# Danksagung
>TODO

# Kurzfassung
>TODO

## Schlüsselwörter
>TODO

# Abstract
> TODO


# Inhaltsverzeichnis
1. **[[#Einleitung]]**
   1. [[#Ziele der Arbeit]]
   2. [[#Stand der Technik]]
   3. [[#Vorgehensweise]]
2. **[[#2 Analyse]]**
   1. [[#2.1 Datenquellen]]
   2. [[#2.2 Benutzeranalyse]]
   3. [[#2.3 Kontextanalyse]]
   4. [[#2.4 Problemanalyse/Aufgabenanalyse]]
   5. [[#2.5 Fazit zur Analyse]]
3. **[[#3 Konzeption]]**
   1. [[#3.1 Konzeptionsvorgehen]]
   2. [[#3.2 Anwendungsfälle]]
   3. [[#3.3 Funktionalitäten]]
   4. [[#3.4 Systemarchitektur]]
   5. [[#3.5 Interface Design]]
   6. [[#3.6 Fazit der Konzeption]]
4. **Realisierung**
   1. [[#Realisierung der Systemarchitektur]]
   2. [[#Realisierung des Interfaces]]
   3. [[#Fazit zur Realisierung]]
5. [[#Dialogbeispiele]]
6. **Summative Evaluation**
   1. [[#Ziel]]
   2. [[#Methode]]
      1. [[#Design]]
      2. [[#Teilnehmer]]
      3. [[#Setting und Instrumente]]
      4. [[#Prozedur]]
   3. [[#Diskussion]]
   4. [[#Fazit zur Evaluation]]
7. **Zusammenfassung und Ausblick**
   1. [[#Zusammenfassung]]
   2. [[#Offene Punkte]]
   3. [[#Ausblick]]
   4. [[#Abschließendes Fazit]]
8. [[#Abbildungen]]
9. [[#Tabellen]]
10. **Quellen**
    1. [[#Literatur]]
    2. [[#Weblinks]]
    3. [[#Software]]
11. [[#Abkürzungen]]
12. [[#Glossar]]
13. **Anhänge**
    1. [[#Anhang A: Inhalt ...]]

# Einleitung

>[!NOTE] Do's und Dont's
>**Abholen**
>Leser abholen und in das Thema einführen, d.h. breit beginnen und dann zuspitzen auf die konkrete Anwendung, um die es geht.
>
>**Why should i care?**
>- Relevanz des Themas in den Folgeabsätzen
>- Mit dem Prinzip zeigen nicht sagen
>  
>**Kein Copy-Paste aus dem Exposé**
>Die Einleitung geht über das Exposé hinaus und einige Punkte aus dem Exposé sind hier auch irrelevant, z.B. der konkrete Zeitplan. Nutzen Sie das Exposé als Grundlage, aber schreiben Sie einen neuen Text.
>

In der digitalen Ära ist die politische Debatte in den Weiten des Internets allgegenwär-
tig, insbesondere in sozialen Medien. Plattformen wie Instagram, TikTok und YouTube
Shorts bieten zwar eine Vielzahl von Inhalten, jedoch werden Themen aufgrund der
Darstellungsform oft nur oberflächlich behandelt. Diese kurzweiligen Formate können
dazu führen, dass Nutzende unvollständige Informationen erhalten, was wiederum zu
verzerrten Meinungsbildern und Fehlinformationen führen kann. Dies wirft die Frage
auf, wie wir eine informierte und ausgewogene Diskussion über politische Standpunkte
fördern können.

**Aktueller Stand**
Um sich über die neuesten politischen Debatten auf der aktuellen Webseite des Land-
tags von Schleswig-Holstein (https://www.landtag.ltsh.de/) zu informieren, müssen die
Nutzenden zunächst mit politischen Begriffen wie "Parlament" und "Plenardokumente"
vertraut sein, um anschließend zur Navigation zu gelangen. Diese Navigation führt dann
zu einer Auflistung aller Transkripte zu allen Sitzungen. Hierbei fehlt eine übersichtli-
che Struktur, die es den Nutzenden ermöglicht, schnell und gezielt Informationen zu
den behandelten Themen in den verschiedenen Sitzungen zu finden. Stattdessen wird
erst durch das Öffnen der Dokumente ersichtlich, welche Themen in welcher Sitzung
behandelt werden. Im optimalen Szenario, in dem die Nutzenden die Webseite und den
spezifischen Sitzungsinhalt kennen, können sie das gewünschte Dokument durch sechs Klicks finden. Dies erfordert jedoch ein genaues Verständnis der Website-Navigation
und der Sitzungsinhalte. Da diese Kenntnisse nicht vorausgesetzt werden können, ist die
Webseite ineffizient und unübersichtlich, um sich einen Überblick zu den Positionen
der Landtagsdebatten zu verschaffen.

**Principle of Least Effort**
Das Phänomen, dass Menschen dazu neigen, den Weg des geringsten Widerstands zu
wählen, wird als "Principle of Least Effort" (Prinzip des geringsten Aufwands) bezeich-
net. Es deutet darauf hin, den einfachsten und schnellsten Weg zu wählen, um ein be-
stimmtes Ziel zu erreichen, anstatt sich mit komplexen oder zeitaufwändigen Optionen
zu befassen (Zipf, 2016). Im Kontext von Webseiten lässt sich daraus schließen, dass
Nutzende dazu neigen eine Software zu verwenden, die eine klare und benutzerfreundli-
che Navigation und unkomplizierte Prozesse anbietet. Durch diese Bedingungen ist we-
niger Anstrengung erforderlich, um die gewünschten Informationen zu finden. Mehr als
fünf Schritte, die zum Erreichen der gewünschten Informationen nötig sind, steigern die
Wahrscheinlichkeit, dass Nutzende unzufrieden die Tätigkeit abbrechen (What is the
Principle Of Least Effort?, 2017).

**E-Partizipation**
In bestimmten Kontexten kann das Konzept der E-Partizipation als ein verbindendes
Angebot fungieren, das die Interaktion zwischen den Bürgern und den staatlichen Insti-
tutionen erleichtert. E-Partizipation beschreibt die Nutzung digitaler Technologien zur
Förderung und Erleichterung der politischen Teilhabe und des Engagements der Bürger
und Bürgerinnen. Die benutzerfreundliche Bereitstellung der Transkripte der Landtags-
debatten kann dazu beitragen die Transparenz politischer Entscheidungsprozesse zu
erhöhen und Bürgern über politische Themen zu informieren. Um die Nutzerfreundlich-
keit zu erhöhen kann das Format der Plenardokumente thematisch aufgebrochen wer-
den.

**Polarisierung und „Filterbubbles“**
Einige Untersuchungen weisen darauf hin, dass soziale Medien zur verstärkten Polari-
sierung und Verzerrung von Informationen beitragen können (wie zitiert in Kubin &
Von Sikorski, 2021). So können Kommentare, die politische Gegner herabsetzen, zu
einer Zunahme der „affective Polarisierung“ führen (Suhay et al., 2018). Es fördert also
eine zunehmende Distanz zwischen politisch gegensätzlichen Gruppen. Die Tendenz
zur Bildung des „Confirmation Bias“ in sozialen Medien aufgrund der Bestätigung ei-
gener Ansichten führt dazu, dass sich isolierte Lager bilden. Sobald diese Lager einge-
nommen wurden, besteht zunehmend weniger Verständnis für abweichende Meinungen,
die Nutzenden agieren in „Filterbubbles“ und werden nur begrenzt mit von der eigenen
Meinung abweichenden Standpunkten konfrontiert. Darüber hinaus wird in derselben
Review analysiert, dass kontroverse oder emotionale Inhalte oft eine höhere Viralität in
sozialen Medien haben.
Im Gegensatz zur Annahme, dass eine Polarisierung in sozialen Medien unvermeidbar
ist, können sowohl soziale als auch traditionelle Medien Nutzenden verschiedene
Standpunkte präsentieren und den Dialog zwischen verschiedenen Gruppen fördern 
(Udani et al., 2018; Valenzuela et al., 2021; Wojcieszak et al., 2020). So kann durch das
Präsentieren von Mehrinformationen ein konstruktiver Dialog initiiert werden (Beam et
al., 2018). Eine ausgewogene Präsentation von Informationen in den Medien kann dazu
beitragen, die politische Polarisierung zu reduzieren (Kubin et al., 2021).


## Ziele der Arbeit
> **Konkretisieren**
> Sie haben vor diesem Abschnitt gezeigt, worum es geht und warum es wichtig ist. Jetzt gehen Sie konkret auf die Ziele ihrer Arbeit ein. Worum kümmern Sie sich und warum konkret das? Was haben Sie erreicht (Vergangenheitsform?)

Eine Herangehensweise könnte darin bestehen, ein überparteiliches und effizientes Sys-
tem zur Verfolgung politischer Debatten nach Themen zu entwickeln. Dies könnte
durch die Schaffung einer Online-Plattform geschehen, auf der Bürger und Bürgerinnen
einfacheren Zugang zu einer Vielzahl von politischen Standpunkten erhalten und sich
darüber informieren können. Ein zentraler Aspekt dieser Plattform wäre die Bereitstel-
lung einer zusammengefassten Version der Transkripte von Landtagsdebatten, die alle
relevanten Argumente der beteiligten Parteien zu einem bestimmten Thema übersicht-
lich auflistet.
Diese Herangehensweise würde einen Übergang von traditionellen, sitzungsbasierten
Dokumenten hin zu themenorientierten Informationen ermöglichen, was den Zugang zu
politischen Inhalten für alle erleichtert. Durch die Moderation der Landtagsdebatten
wird sichergestellt werden, dass alle beteiligten Parteien eine ähnliche Gesprächszeit
erhalten. Jede Fraktion kann für einen Redner bis zu 10 Minuten sprechen, und alle wei-
teren Redner dürfen jeweils höchstens 5 Minuten reden (§ 56 Form und Dauer der Re-
de, o. J.). Das sorgt für eine ausgewogene Darstellung verschiedener Standpunkte und
gewährleistet, dass keine Partei gegenüber einer anderen bevorzugt wird.

**Ziel**
Im Rahmen dieser Bachelorarbeit steht die Entwicklung eines Informationssystems im
Fokus. Es soll Nutzern und Nutzerinnen ermöglichen, sich schnell und einfach über
aktuelle oder vergangene Landtagsdebatten in Schleswig-Holstein zu informieren. Die
Relevanz dieses Projekts wird durch die enorme Menge an Daten deutlich, die allein in
dieser Wahlperiode (2022-2027) durch monatliche Plenumssitzungen entstanden sind -
über 4000 Seiten an Informationen, die bisher unübersichtlich zugänglich sind. Dieses
Problem soll durch eine Webseite gelöst werden, die Informationen durch eine Künstli-
che Intelligenz zusammenfasst und über eine intuitive Benutzeroberfläche zugänglich
macht. Der Fokus liegt hierbei auf der grafischen Oberfläche und deren Gebrauchstaug-
lichkeit, weswegen während der Entwicklung voraussichtlich mit Platzhalterdaten gear-
beitet wird.

Die Entwicklung der Arbeit greift die Idee auf, die bereits im JIL von Anna-Katharina
Dhungel und Lea Watermann (Watermann & Dhungel, o. J.) als Figmaprototypen fest-
gehalten wurde. Jedoch ist zu beachten, dass das Design während des Entwicklungspro-
zesses variieren kann.

Ein zentraler Ansatzpunkt bei der Entwicklung der Benutzeroberfläche ist die Theorie
der zwei Modi des kognitiven Denkens, wie von Kahneman (2012) beschrieben. Dieser Ansatz legt nahe, dass das reflektierte Denken (System 2) gegenüber dem impulsiven
Denken (System 1) bevorzugt werden sollte, um vorschnelle Beurteilungen zu vermei-
den. Durch gezieltes Nudging wird angestrebt, den Nutzern zunächst einen Überblick
über die verschiedenen Argumente der Debatte zu verschaffen, bevor sie auf die Stand-
punkte der Parteien zugreifen können. Dies soll dazu beitragen, blinde Standpunktüber-
nahmen zu vermeiden.

Zur Verbesserung des User Interfaces werden Design Heuristiken verwendet, wie sie in
der Sammlung kognitiver Verzerrungen in dem Artikel von Mobile Spoon (Bouhnick,
2019) dargelegt sind. Dark Patterns, die gewöhnlich darauf abzielen den Nutzer so lan-
ge wie möglich in Interaktion mit der Software zu halten, werden vermieden, um si-
cherzustellen, dass Nutzer nur so viel Zeit wie nötig auf der Website verbringen muss,
um an die benötigten Informationen zu gelangen. Für das Layout und die Strukturierung
des Informationssystems werden die Gestaltprinzipien nach Johnson (2014) herangezo-
gen. Diese Prinzipien, wie die Nähe, Ähnlichkeit und Kontinuität, sind entscheidend für
die visuelle Organisation von Informationen und tragen dazu bei, die Nutzererfahrung
zu verbessern (Johnson, 2014). Das angestrebte Ergebnis ist ein Informationssystem in
Form einer Web-Anwendung, die es Bürgern und Bürgerinnen ermöglicht, einen um-
fassenden Überblick über die Inhalte und Standpunkte der Landtagsdebatten von
Schleswig-Holstein zu erhalten. Zunächst soll die Machbarkeit des Vorhabens gezeigt
werden. Dafür wird erwogen, einen begrenzten Zeitraum von 1-2 Jahren (z. B. 2022-
2023) aus den insgesamt 4000 Seiten der Landtagsdebatten von 2022-2027 einzubeziehen, um die Entwicklung und den Umfang des Projekts realistisch einzuschätzen.




## Vorgehensweise
>**Einleitung als erste Schritt im Menschenzentrierten Gestaltungsprozess**
>Die Vorgehensweise spiegelt im Prinzip das Planen des menschenzentrieten Gesaltungsprozesses wieder. Das haben Sie im Expose angefangen und hier (was dann tatsächlich gemacht wurde) überarbeitet dargestellt.
>
>**Vorgehen**
>Wie sind Sie vorgegangen, um die Ziele der Arbeit zu erreichen? Oft bietet sichdas Diagram der DIN EN ISO 9241-210 an (wenn Sie hier eine ABbildung verwenden, dann müssen Sie sich auch das vorgehen gehalten haben!).
>
>**Orientierung im Bericht:** Wo findet der Leser die Ergebnisse der einzelnen Schritte und was beinhalten diese (kurz halten)? Verweise auf Folgekapitel am besten im Stil "Werden in der Analyse (Kapitel 2) ..." statt "in Kapitel 2 wird ..." - das Vorgehen gibt die Kapitel vor, nicht umgekehrt.
>
>![[Pasted image 20241006100127.png]]
>**Abbildung** **1****:** Menschzentrierter Gestaltungsprozess (DIN EN ISO 9241-210)

Im Rahmen dieser Bachelorarbeit wurde ein menschenzentrierter Gestaltungsprozess durchgeführt, um eine nutzerfreundliche informative Webseite, für die Debatten des Landtages Schleswig Holsteins,  zu entwickeln. Dieser Prozess orientierte sich an den Vorgaben der DIN EN ISO 9241-210 (Abbildung 1) und legte besonderen Wert darauf, die Bedürfnisse und Anforderungen der Nutzerinnen und Nutzer in den Mittelpunkt zu stellen.  

![[Pasted image 20241006100127.png]]

### Phase 1: Verstehen des Nutzungskontextes und Festlegen der Nutzungsanforderungen

Um den Nutzungskontext umfassend zu verstehen und die Nutzungsanforderungen klar zu definieren, wurden in der Analyse mehrere Methoden eingesetzt. Zunächst wurde eine **Umfrage** durchgeführt, um allgemeine Fragen zur Landespolitik und zur Informationsbeschaffung der Zielgruppe zu klären. Diese Umfrage lieferte erste Einblicke in das Informationsverhalten der potenziellen Nutzerinnen und Nutzer sowie deren Erwartungen an ein Informationssystem, das politische Inhalte verständlich aufbereitet (Kapitel 2.1).

Anschließend wurden **Kontextinterviews** nach dem Meister/Schüler-Prinzip durchgeführt, um die Nutzungssituation in der Praxis besser zu verstehen. Diese Interviews ermöglichten es, den Ort und das Verhalten der Nutzer während der Informationsbeschaffung genau zu beobachten und somit reale Nutzungsszenarien zu analysieren (Kapitel 2.2).

Parallel dazu wurde eine **Literaturrecherche** durchgeführt, um wissenschaftliche Erkenntnisse und bewährte Methoden im Bereich nutzerzentrierter Gestaltung zu analysieren. Die Ergebnisse der Recherche halfen, den theoretischen Rahmen der Arbeit zu fundieren und die Gestaltung der Webseite auf aktuellen Forschungsergebnissen zu stützen (Kapitel 2.3).

Zur weiteren Veranschaulichung der Nutzungssituationen wurde das **Szenario Based Design** eingesetzt. Hierbei wurden verschiedene Szenarien entwickelt, die den aktuellen „Ist“-Zustand der Nutzung abbildeten. Diese Szenarien zeigten typische Nutzungsmuster und halfen dabei, bestehende Probleme und Anforderungen an das zukünftige System besser zu verstehen (Kapitel 2.4).

Am Ende dieser Phase wurde eine Problem- und Aufgabenanalyse auf Basis des Szenario-Based Designs durchgeführt. Diese Analyse identifizierte die zentralen Herausforderungen, denen die Nutzerinnen und Nutzer im aktuellen System begegnen, und leitete daraus konkrete Anforderungen ab, die im neuen System berücksichtigt und integriert werden sollten. ( Kapitel 2.5)
### Phase 2: Festlegung der Nutzungsanforderungen

Basierend auf den Erkenntnissen der Analysephase wurden die Nutzungsanforderungen der Webseite festgelegt. Diese Anforderungen umfassten funktionale, ästhetische und technische Aspekte, die sich direkt aus den Bedürfnissen der Nutzerinnen und Nutzer sowie den spezifischen Nutzungssituationen ableiteten. Ziel war es, eine benutzerfreundliche und effektive Lösung zu schaffen, die den Nutzern eine einfache und effiziente Informationsbeschaffung ermöglicht. (Kapitel 2.6)

### Phase 3: Erarbeiten von Gestaltungslösungen

In der Konzeptionsphase wurden die festgelegten Anforderungen in konkrete Gestaltungslösungen überführt. Zunächst erfolgte eine **Strukturierung der Inhalte**. Diese stellte sicher, dass die Informationen auf der Webseite logisch gegliedert und leicht zugänglich waren. Die Informationsarchitektur basierte auf den Nutzungsanforderungen und wurde darauf ausgelegt, den Nutzer effizient zu den gewünschten Inhalten zu führen (Kapitel 3.1).

Darauf aufbauend wurde das **User Interface (UI)** entwickelt. In einem iterativen Prozess wurden zunächst Skizzen erstellt, um die grundlegende Struktur und die Hauptfunktionen der Webseite zu visualisieren. Anschließend folgte die Erstellung von interaktiven Prototypen im Rahmen des **Rapid Prototypings**, um die Navigation und die Funktionalitäten der Webseite frühzeitig zu testen. Diese Prototypen wurden schrittweise in detaillierte **Wireframes** überführt, die eine klare Darstellung der Seitenstruktur und der Benutzeroberfläche boten. Schließlich wurden **Mockups** erstellt, die das finale visuelle Design der Webseite einschließlich Farbgestaltung, Typografie und Layout zeigten (Kapitel 3.2).

Um die Qualität und die Nutzerfreundlichkeit des Designs sicherzustellen, wurden kontinuierlich **UX-Tests** durchgeführt. Dabei wurden entweder **Remote-Usability-Tests** oder **Guerilla-Tests** eingesetzt, um Feedback von realen Nutzern zu erhalten. Die Ergebnisse dieser Tests flossen direkt in die Optimierung des Designs ein. Durch die iterative Anwendung der Lean UX Methode konnten Probleme frühzeitig identifiziert und behoben werden, wodurch eine kontinuierliche Verbesserung des Nutzererlebnisses gewährleistet wurde (Kapitel 3.3).


# 2 Analyse

Junge Menschen stoßen im Internet zunehmend auf unvollständige oder falsche Informationen. Um zu verhindern, dass sie diese irreführenden Inhalte unbewusst übernehmen, ist es sinnvoll, die aufgenommenen Informationen mit den ursprünglichen Aussagen zu überprüfen oder sich präventiv mit aktuellen landespolitischen Debatten und Beschlüssen auseinanderzusetzen. Dies trägt dazu bei, das politische Verständnis auf Landesebene zu fördern, da sich die Landespolitik oft stark von der bundesweiten Politik unterscheidet. Da dieser zusätzliche Rechercheaufwand oft in einem eigentlich entspannten Umfeld erfolgt, sollte der Prozess besonders nutzerfreundlich, schnell und jederzeit von überall aus einfach zugänglich sein.

## 2.1 Datenquellen

Für die Analyse dieser Arbeit wurden verschiedene Datenquellen genutzt, um ein umfassendes Verständnis des Nutzungskontexts und der Anforderungen an das geplante Informationssystem zu erlangen. Diese Quellen umfassen eine Umfrage, Kontextinterviews, sowie wissenschaftliche Literatur. Im Folgenden werden die einzelnen Datenquellen näher erläutert.

**Umfrage**
>Wann? Worüber? Kategorien der Fragen? Wie viele Personen haben teilgenommen? Welche zentrale Eigenschaften haben die Personen? (Mittelwert SD von Alter, Berufsbezeichnung)

Im Zeitraum vom **07.08.2024 bis 25.08.2024** wurde eine in **Google Forms** erstellte Umfrage über **Landespolitik Allgemein** und die Möglichkeiten, sich darüber zu informieren, im Bekanntenkreis geteilt. Insgesamt haben **11 Teilnehmende** an der Umfrage teilgenommen. Der Mittelwert des Alters der Teilnehmenden liegt bei **25,73 Jahren**, mit einer Standardabweichung von **3,28 Jahren**. Von den Teilnehmenden waren **8 Personen männlich** und **3 Personen weiblich**. In Bezug auf den Bildungsabschluss hatten **4 Teilnehmende die Allgemeine Hochschulreife (Abitur)**, **3 Teilnehmende einen Bachelor**, **2 Teilnehmende eine Berufsausbildung**, **1 Teilnehmender eine Fachhochschulreife (Fachabitur)** und **1 Teilnehmender ein Staatsexamen**. Bei der Nutzungsfrequenz von Informationen über Landespolitik gaben **7 Personen an, dies seltener zu tun**, während **2 Personen dies nie tun** und **2 Personen dies monatlich tun**.


**Kontextinterviews**
>Wie Personengruppen bestimmt? Welche Fragen gestellt wuden (Oberkategorien)? Kurz Methode erklären? Relevanz der Person beschreiben?

Im Rahmen dieser Studie wurden Kontextinterviews durchgeführt, um tiefere Einblicke in die Nutzung von sozialen Medien in Bezug auf die Landespolitik zu gewinnen. Ein kontextuelles Interview ist ein Interview, das im natürlichen Umfeld der Benutzer stattfindet, um die Interaktion der Nutzenden mit der Anwendung zu verstehen. Dabei wurde besonders auf den Nutzungskontext, die Motivation und die Strategien der Teilnehmer geachtet [Link].

Die Personengruppen wurden anhand spezifischer Kriterien ausgewählt. Ziel war es, Nutzende zu identifizieren, die zwischen **16 und 35 Jahren alt sind**, soziale Medien aktiv nutzen und nicht im politischen Bereich arbeiten. Diese Vorgaben helfen, eine Gruppe von Personen zu bestimmen, die eine distanzierte Perspektive auf politische Themen haben und deren Meinungen und Verhaltensweisen in diesem Kontext von Interesse sind. 

Um die Teilnehmenden auszuwählen, wurden im junge Studentinnen angesprochen, die die oben genannten Kriterien erfüllen. Die Interviews fanden an Orten (Schreibtisch/Couch) statt, die für die Teilnehmenden relevant sind, um die tatsächliche Nutzung von sozialen Medien zu beobachten und direktes Feedback zu den Aktivitäten und Gedanken der Nutzenden zu erhalten.

Um den Prozess der Informationsbeschaffung vergleichbar zu machen, wurde mithilfe einer Aufgabe die Situation simuliert und beide Teilnehmerinnen wurden gebeten eine Aufgabe (Kapitel 2.x) zu bearbeiten, in der sie sich über ein ausgewähltes Thema informieren sollen. Die Fragen wurden in einem offenen, explorativen Rahmen durchgeführt, wobei sich die Fragen während des Gesprächs entwickelt haben. 


**Wissenschaftliche Literatur**
> Wo (Suchbegriffe) haben Sie wann, mit welchen Suchbegriffen gesucht?

Um ein umfassenderes Verständnis der Zielgruppe zu gewinnen, wurde eine systematische Literaturrecherche durchgeführt. Als Primäre Datenbank wurde Google Scholar genutzt, um relevante wissenschaftliche Arbeiten und Berichte zu identifizieren. Hierbei wurden gezielte Suchbegriffe eingegeben, um einen Überblick über das Thema zu erhalten. Die verwendeten Suchbegriffe umfassten „Fake News und Desinformation Jugend Bericht“, „Mediennutzung im digitalen Zeitalter“, „Einfluss sozialer Medien auf Nachrichten“, „Politik in sozialen Medien“ sowie „Junge Erwachsene Politik in sozialen Medien“. Diese Suchanfragen führten am 27.08.2024 zu etwa 51.900 Ergebnissen für den Begriff „Reuters Institute Digital News Report 2023“ innerhalb von nur 0,13 Sekunden. Am 28.08.2024 wurde zusätzlich der Begriff „Jugend Information Medien 2022“ eingegeben, wobei ich eine visuell aufbereitete Version der Studie in den Ergebnissen fand. Durch diese gezielte Recherche gelangte ich schließlich zu den relevanten Berichten, die entscheidende Einblicke in die Mediennutzung und den Einfluss von sozialen Medien auf die Jugend bieten.

| Datenbank      | Suchbegriff                                                               | Datum    | Ergebnisse                                 |
| -------------- | ------------------------------------------------------------------------- | -------- | ------------------------------------------ |
| Google Scholar | Reuters Institute Digital News Report 2023                                | 27.08.24 | Ungefähr 51.900 Ergebnisse (**0,13** Sek.) |
| Google Scholar | Jugend Information Medien 2022 (visuiell aufgearbeitete Version genommen) | 28.08.24 | Ungefähr 27.400 Ergebnisse (**0,09** Sek.) |

### BAUR-Merkhilfe
>Chesnut, D., & Nichols, K. (2014). _UX For Dummies_. John Wiley & Sons.

Um die gesammelten Informationen strukturiert auszuwerten wird die BAUR-Merkhilfe verwendet. Bei der Betrachtung einer Situation ist es essenziell, den **Benutzer** zu identifizieren, um zu verstehen, wer die zentrale Rolle in diesem Kontext spielt und welche Bedürfnisse und Erwartungen er oder sie hat. Anschließend werden die **Aufgaben und Ziele** des Benutzers analysiert. Diese Aspekte sind entscheidend, da sie aufzeigen, welche spezifischen Ziele der Benutzer verfolgt und welche Aufgaben erforderlich sind, um diese zu erreichen. (Ludewig, 2020)

Darüber hinaus spielt die **Umgebung** eine wesentliche Rolle in der Gesamtdynamik der Situation. Die physische, soziale und technische Umgebung beeinflusst maßgeblich das Nutzerverhalten und die Interaktionen. Schließlich ist die Identifikation der **Ressourcen**, die in dieser Situation zur Verfügung stehen oder benötigt werden, unerlässlich. Ressourcen können sowohl materielle als auch immaterielle Mittel umfassen, die den Benutzer bei der Erreichung seiner Ziele unterstützen.


## 2.2 Benutzeranalyse
>Wer sind die Benutzer/innen der Entwicklung?

### 2.2.1 Analyse der Benutzer der Online-Umfrage
Die Teilnehmer der Online-Umfrage , zeigen ein klares Profil einer heterogenen Gruppe junger Menschen im Alter von 16 bis 30 Jahren, mit unterschiedlichen Bildungsabschlüssen.
Ein zentrales Interesse der Befragten liegt in relevanten gesellschaftlichen Themen wie **Klimapolitik**, Wahlprogrammen, Rechtsextremismus sowie Desinformation und sozialen Fragen. Diese Themen spiegeln ein Bewusstsein für aktuelle gesellschaftliche Herausforderungen wider, was auf eine allgemeine Sensibilität für politische und soziale Belange hinweist (vgl. Anhang 1.1). Gleichzeitig ist zu betrachten, dass sich in den meisten Fällen häufig bis gar nicht mit Landespolitischen Themen auseinandergesetzt wird.

Die Umfrageergebnisse legen nahe, dass die Landtagspolitik für die Teilnehmer an Interesse gewinnen könnte, wenn die Themen einfacher zugänglich und verständlich aufbereitet werden. So stimmen 30 % der Befragten voll und 60 % zumindest teilweise zu, dass sie sich intensiver mit Landtagsthemen befassen würden, wenn diese transparenter präsentiert werden (vgl. Anhang 1.1). Dieses Bedürfnis nach zugänglicher und verständlicher Information deutet auf eine allgemeine Hürde hin: die Komplexität und Unübersichtlichkeit der politischen Themen könnte viele der Befragten davon abhalten, sich intensiver mit der Materie auseinanderzusetzen.

Ein weiterer wichtiger Aspekt der Analyse ist die Präferenz der Nutzer für visuelle Informationen gegenüber textuellen Inhalten. Rund 50 % der Befragten geben an, dass sie Informationen visuell besser verstehen als in Textform, was auf die Notwendigkeit hinweist, Inhalte entsprechend aufzubereiten (vgl. Anhang 1.1). Zudem zeigt die Umfrage, dass 60 % der Teilnehmer kurze Texte bevorzugen, während nur 30 % neutral gegenüber längeren Texten eingestellt sind. Diese Präferenzen legen nahe, dass eine gezielte und prägnante Kommunikation der Inhalte essenziell ist, um die Aufmerksamkeit und das Interesse der Benutzer zu wecken und zu halten.

### 2.2.2 Analyse der Kontextinterviews
Die Analyse der beiden Kontextinterviews zeigt ein differenziertes Bild der Nutzer, die Informationen zu politischen Themen, insbesondere zur Landtagspolitik, suchen. Die Befragten sind zwei junge weibliche Erwachsene, die das Internet aktiv zur Informationsbeschaffung nutzen. Während der erste Nutzer regelmäßigen in Kontakt mit politischen Informationen hat, zeigt der zweite Nutzer eine geringere Vertrautheit mit Landtagsdebatten und deren Relevanz.

Der erste Nutzer ist zwar an politischen Themen interessiert, findet jedoch die Fülle an Informationen überwältigend. Die Kombination aus allgemeinem Zeitmangel und der Notwendigkeit, sich ständig auf dem Laufenden zu halten, führt zu einer Abnahme des Interesses. Der zweite Nutzer hingegen hat eine Vorliebe für Hintergrundinformationen, verliert jedoch schnell das Interesse, wenn die Informationen zu lang oder unübersichtlich sind. Dies deutet auf ein Bedürfnis nach klar strukturierten und leicht verständlichen Inhalten hin.

Beide Nutzer stehen vor erheblichen Herausforderungen bei der Informationsbeschaffung. Der erste Nutzer empfindet politische Informationen oft als schwer zugänglich und unübersichtlich, was zu Frustration führt. Er ist sich auch unsicher, ob die Informationen, die er findet, korrekt und vollständig sind. Der zweite Nutzer hat Schwierigkeiten, den Überblick über die Informationen auf Webseiten zu behalten, insbesondere wenn diese lange Texte oder unstrukturierte Inhalte bieten. Dies führt zu Desinteresse und kann das Engagement der Nutzer verringern.

Die Präferenzen der beiden Nutzergruppen zeigen deutlich, dass sie eine strukturierte und gut navigierbare Webseite bevorzugen. Der erste Nutzer wünscht sich eine Plattform, die relevante Informationen schnell und übersichtlich präsentiert. Der zweite Nutzer legt Wert auf kurze, prägnante Zusammenfassungen sowie eine visuelle Aufbereitung der Informationen. 

### 2.2.3 Analyse der Wissenschaftlichen Quellen
Die digitale Medienlandschaft ist im stetigen Wandel und wird zunehmend von mobilen und plattformbasierten Informationsquellen dominiert. Der **Reuters Institute Digital News Report 2023** (Newman et al., 2023)  hebt hervor, dass Krisen wie der Ukraine-Krieg und die Coronavirus-Pandemie diesen Wandel erheblich beschleunigt haben. Ein zentrales Merkmal dieses Wandels ist der Rückgang direkter Besuche auf Nachrichten-Websites, wobei nur etwa 22 % der Befragten diese als ihre bevorzugte Informationsquelle angeben, ein Rückgang um 10 Prozentpunkte seit 2018. Besonders auffällig ist, dass jüngere Nutzer zunehmend soziale Medien, Suchmaschinen und Aggregatoren nutzen, um Nachrichten zu konsumieren, was die veränderte Rolle traditioneller Medien unterstreicht. Plattformen wie YouTube und TikTok gewinnen an Bedeutung, während Facebook im journalistischen Kontext an Einfluss verliert.

Ein weiteres wichtiges Ergebnis des Reports ist die Skepsis der Nutzer gegenüber den Algorithmen, die bestimmen, welche Nachrichten ihnen angezeigt werden. Nur 30 % der Befragten halten diese Auswahl für vorteilhaft, was einen Rückgang um 6 Prozentpunkte seit 2016 darstellt. Dies deutet auf ein wachsendes Misstrauen hin, das möglicherweise mit dem Rückgang des Vertrauens in Nachrichten zusammenhängt. Das Vertrauen in Nachrichten ist weltweit um 2 Prozentpunkte gesunken, und es wird beobachtet, dass etwa 36 % der Befragten aktiv Nachrichten vermeiden. Diese Tendenz zur Nachrichtenvermeidung ist besonders besorgniserregend, da sie zeigt, dass eine signifikante Anzahl von Nutzern das Bedürfnis hat, sich von negativen Informationen abzugrenzen.

Die **JIM-Studie 2022** bietet ergänzende Einblicke in die Herausforderungen, mit denen insbesondere Jugendliche konfrontiert sind. Der Bericht dokumentiert, dass 58 % der Befragten bereits mit Fake News in Kontakt gekommen sind und dass etwa die Hälfte beleidigende Kommentare im Internet erlebt hat. Diese Erfahrungen sind besonders häufig unter Jugendlichen anzutreffen, die vermehrt extremen politischen Ansichten und Verschwörungstheorien ausgesetzt sind. Die Studie zeigt auch, dass der Anteil der Jugendlichen, die im Netz mit solchen Inhalten konfrontiert werden, mit dem Alter steigt. Diese Entwicklung wirft Fragen auf, ob bestimmte Teilgruppen, wie z.B. unterschiedliche Schularten oder Geschlechter, besser in der Lage sind, zwischen legitimen Informationen und Desinformation zu unterscheiden.

Ein zentrales Ergebnis beider Studien ist die Notwendigkeit, die Medienkompetenz zu fördern. Die **JIM-Studie** legt nahe, dass die Sensibilisierung für Desinformation und die Fähigkeit, mit solchen Inhalten umzugehen, entscheidend sind, um Jugendliche in ihrer Informationsverarbeitung zu stärken. Beide Studien verdeutlichen, dass es eine Lücke zwischen dem Informationsbedarf der Nutzer und der bereitgestellten Informationsqualität gibt. Während Nutzer zunehmend auf digitale und soziale Medien zurückgreifen, ist das Vertrauen in die Informationen, die sie dort finden, gering. Dies erfordert eine sorgfältige Überprüfung der Inhalte und eine verstärkte Bildung im Bereich Medienkompetenz, um sowohl das Vertrauen als auch das Engagement der Nutzer in die politische und gesellschaftliche Diskussion zu fördern.

## 2.3 Kontextanalyse
Die Nutzungskontexte der Befragten ergeben klare Anforderungen an die Gestaltung einer Informationsplattform zu politischen Themen, insbesondere in Bezug auf die Landtagspolitik. Die Interviews bieten wertvolle Einsichten in die räumlichen und zeitlichen Kontexte der Informationsbeschaffung und zeigen dabei deutliche Präferenzen sowie Herausforderungen auf.

### 2.3.1 Nutzungskontext: Online-Umgebung
Beide Interviewpartner nutzen bevorzugt Desktop-Computer oder Laptops für ihre Recherche, da diese Geräte eine komfortablere Handhabung mehrerer geöffneter Reiter ermöglichen und somit eine übersichtlichere Navigation durch verschiedene Informationsquellen bieten. Diese Präferenz deutet darauf hin, dass die Nutzung der Plattform primär auf PC-Umgebungen zugeschnitten sein sollte. Mobile Geräte, wie Smartphones, kommen ergänzend zum Einsatz, insbesondere für schnelle Informationssuche unterwegs. Da beide Nutzer die Recherche hauptsächlich im Internet betreiben, insbesondere auf offiziellen Webseiten oder über Suchmaschinen wie Google, sollte die Informationsplattform besonders benutzerfreundlich und gut navigierbar gestaltet werden, um ein positives Nutzungserlebnis zu gewährleisten.

### 2.3.2 Anforderungen an Webseiten und Dokumente
Ein zentrales Thema in beiden Interviews ist die Schwierigkeit, sich auf politischen Webseiten, wie etwa der des Landtags, zurechtzufinden. Während im ersten Interview die Seiten als unübersichtlich und schwer navigierbar beschreibt, konnte im zweiten Interview nach anfänglichen Schwierigkeiten eine positivere Haltung entwickeln, sobald die Struktur der Seite besser verstanden wurde. Darüber hinaus stellen beide Nutzer fest, dass lange, unstrukturierte Dokumente, wie etwa Debattenprotokolle, zu Frustration und Motivationsverlust führen. Das Fehlen eines klaren roten Fadens sowie die überwältigende Menge an Informationen führen oft zum Abbruch der Recherche. Daraus ergibt sich die Anforderung, dass Dokumente auf der Plattform prägnant, strukturiert und leicht zu durchstöbern sein müssen, um die Nutzer bei der Informationssuche nicht zu überfordern. (siehe Anhang Interview Ergebnisse 1+2)


## 2.4 Problemanalyse/Aufgabenanalyse
> Welches der Probleme werden addressiert?

### 2.4.1 Problemszenario
Lisa ist eine engagierte junge Frau, die sich leidenschaftlich für soziale Themen wie Klimaschutz, Bildung und soziale Gerechtigkeit einsetzt. Sie möchte regelmäßig verfolgen, wie die Politik im Landtag diese Themen behandelt, um informiert und aktiv zu bleiben. Allerdings hat sie Schwierigkeiten, die relevanten Informationen auf der Webseite des Landtags zu finden. Die Webseite ist unübersichtlich, und die Debattenprotokolle sind nicht nach Themen, sondern nur nach Sitzungen sortiert, was es ihr erschwert, spezifische Positionen der Parteien zu ihren Herzensthemen zu finden.
![[Szenario 1.canvas|Szenario 1]]
### 2.4.2 Aufgabenanalyse

**Aufgabenanalyse für die zu entwickelnde Software im Rahmen der Bachelorarbeit**

In der vorliegenden Aufgabenanalyse wird die zu entwickelnde Software untersucht und in zentrale Aufgabenbereiche gegliedert. Das Ziel der Software ist es, politische Debatten, Argumente und Abstimmungen für Nutzende übersichtlich, interaktiv und informativ darzustellen. Besonderes Augenmerk liegt dabei auf der Darstellung von Argumenten zu politischen Themen, welche mithilfe einer KI gefiltert und strukturiert werden sollen. Die Nutzerführung, Usability und Barrierefreiheit spielen dabei eine wichtige Rolle, um eine breite Zielgruppe anzusprechen und den Zugang zu politischer Information zu erleichtern.

 **Benutzeroberfläche (User Interface)**
Ein modernes und minimalistisches Design bildet die Grundlage der Benutzeroberfläche. Hierbei liegt der Fokus darauf, den Nutzenden eine klare und intuitive Struktur zu bieten, sodass die wichtigsten Inhalte schnell und einfach zugänglich sind. Responsiveness, also die Anpassungsfähigkeit an unterschiedliche Bildschirmgrößen und Endgeräte, ist entscheidend, damit die Anwendung sowohl auf Desktop-Rechnern als auch auf mobilen Geräten optimal genutzt werden kann. Die Argumente zu den politischen Themen sollen interaktiv eingeblendet werden können, um die Informationen gezielt und bedarfsgerecht anzuzeigen, ohne den Nutzenden zu überfordern. Eine übersichtliche Navigation hilft dabei, den Informationsfluss zu lenken und die Inhalte effizient zu erschließen.

 **Argumente und Inhalte**
Im Zentrum der Software steht die Darstellung von politischen Argumenten und Inhalten. Hierbei sollen die Standpunkte der Parteien, Abstimmungsergebnisse sowie die Pro- und Kontra-Argumente zu den jeweiligen Themen abgebildet werden. Besonders wichtig ist die Verknüpfung dieser Argumente mit ihren Primärquellen, um den Nutzenden die Möglichkeit zu bieten, die Originaldokumente einzusehen und die Herkunft der Argumente zu überprüfen. Die Darstellung von Zitaten der Parteien sowie Vorschläge und Änderungen zu den jeweiligen Themen soll die Diskussion transparent und nachvollziehbar machen.

**Weitere Informationen**
Neben der reinen Argumentation und Darstellung von Abstimmungen soll die Software Hintergrundinformationen zu den jeweiligen Themen anbieten. Dies ermöglicht den Nutzenden, sich umfassend und tiefgehend in die Debatte einzuarbeiten. Ziel ist es, den Nutzenden eine klar verständliche Beschreibung der Debattenthemen sowie die damit verbundenen Ziele und Absichten zu liefern. Die Verlinkung von Primärquellen spielt auch hier eine zentrale Rolle, um den Informationsgehalt zu erhöhen und Vertrauen in die dargestellten Inhalte zu schaffen. Darüber hinaus sollen verwandte Gesetze und gesetzliche Regelungen, die das jeweilige Thema betreffen, leicht zugänglich gemacht werden.

**User Experience**
Die Nutzererfahrung steht im Fokus der Softwareentwicklung. Eine umfassende und leistungsfähige Suche soll es den Nutzenden ermöglichen, gezielt nach relevanten Themen und Informationen zu suchen. Dabei soll die Suche auch Vorschläge aus den aktuellsten Sitzungen liefern, um stets aktuelle Inhalte bereitstellen zu können. Barrierefreiheit ist ein weiterer wichtiger Punkt. Es wird angestrebt, die Anwendung für alle Nutzenden zugänglich zu machen, indem beispielsweise Kontraste für Menschen mit Sehschwächen optimiert und alternative Beschreibungen für Bilder und Icons angeboten werden, um die Software auch für Screenreader zugänglich zu machen. Ein gut strukturierter Informationsbereich, der die Inhalte klar und verständlich aufbereitet, sowie die Möglichkeit, Vorschlagsthemen einzureichen, runden das Konzept ab.

## 2.5 Fazit zur Analyse

Die Analyse zeigt, dass es insbesondere junge Menschen schwer haben, verlässliche und verständliche Informationen zur Landespolitik zu finden. Dies liegt vor allem an der unübersichtlichen und komplexen Aufbereitung der Inhalte sowie der allgemeinen Überflutung mit Informationen. Die Nutzerpräferenzen legen nahe, dass eine klare Struktur, visuelle Aufbereitung und kurze, prägnante Texte essentiell sind, um das Interesse und die Effizienz der Nutzung zu fördern.

Basierend auf den verschiedenen Nutzungsanforderungen ergibt sich folgende Priorisierung:
- **Absolut notwendig (Muss-Kriterien)**:
    - Voll funktionstüchtige Webseite mit Suchfunktion für die Inhalte
    - Anzeige von mindestens 3 Sitzungen (Proof of Concept; potenziell Platzhalterdaten statt automatisierter KI)
    - Übersichtliche Navigation zwischen den Sitzungen und Drucksachen
- **Wichtig (Soll-Kriterien)**:
    - Verlinkung zu Primärquellen
    - Barrierefreiheit für alle Nutzer
- **Nice-to-have (Kann-Kriterien)**:
    - Automatische Verknüpfung der Plenardokumente mit dem Backend
    - KI-Schnittstelle zum Filtern von Informationen und befüllen der DB

- **Unwichtig (Kür-Kriterien)**:
    - Mehrsprachigkeit
    - Dark Mode
    - Weitere Personalisierungsfunktionen
    - Darstellung von Daten zu allen Beschlüssen

Die durchgeführte Analyse hat gezeigt, dass junge Menschen häufig Schwierigkeiten haben, sich in der Landespolitik zurechtzufinden. Insbesondere die bereitgestellten Informationen erweisen sich oft als unübersichtlich und schwer verständlich. Dies resultiert aus der Komplexität der Inhalte und der Vielzahl an Informationen. Somit bietet es sich an eine klare Struktur, ansprechende visuelle Gestaltung und prägnante Texte zu bieten. Zukünftige Entwicklungen sollten verstärkt auf Automatisierung und KI-basierte Funktionen setzen, um den Zugang zu den Inhalten weiter zu erleichtern. Der Fokus sollte auf einer verbesserten Suchfunktion und eines Inhaltlichen Überblickes liegen, um den Zugang zur Landespolitik für alle Nutzer zu optimieren.

# 3 Konzeption

Die Analyse hat gezeigt, dass junge Menschen Schwierigkeiten haben, verlässliche und verständliche Informationen zur Landespolitik zu finden. Um diesen Herausforderungen zu begegnen, wird in der Konzeption eine Lösung entwickelt, die direkt auf die identifizierten Bedürfnisse und Anforderungen der Nutzer eingeht.

Zunächst wird das Vorgehen zur Konzeption beschrieben (Kapitel 3.1), gefolgt von Anwendungsfällen (Kapitel 3.2) und den wesentlichen Funktionalitäten des Systems (Kapitel 3.3). Besonderer Fokus liegt auf den Muss-Kriterien aus der Analyse, um eine gute Grundlage für die Evaluation zu schaffen. 
## 3.1 Konzeptionsvorgehen

In einem iterativen Prozess, der auf den Erkenntnissen der Analyse aufbaut, werden nun die Methoden beschrieben, die zur Entwicklung der Lösung eingesetzt wurden. Zunächst wurden **Use Cases** erstellt, um die spezifischen Bedürfnisse und Anforderungen der Nutzer zu identifizieren. Diese Use Cases spiegeln reale Nutzungsszenarien wieder und durch die Definition dieser Szenarien konnten die zentralen Aufgaben und Herausforderungen der Nutzer klarer umrissen werden.
Im Anschluss an die Erstellung der Use Cases wurden die **Funktionalitäten** priorisiert. Diese Priorisierung erfolgte anhand der in der Analyse festgelegten Muss-, Soll- und Kann-Kriterien (Kapitel 2.5). Die Funktionalitäten sollen Struktur für das User Interface bieten um einen klaren Fokus auf die wichtigsten Features zu setzen, um die Nutzerbedürfnisse zu erfüllen.
Die nächste Phase des Konzeptionsprozesses umfasste die Spezifikation der **Systemarchitektur**. Hierbei wurde ein technisches Framework entwickelt, das die Implementierung der priorisierten Funktionalitäten ermöglicht. Die Systemarchitektur berücksichtigt Aspekte wie die Datenverarbeitung, die Anbindung an externe Informationsquellen und die Benutzerinteraktion.
Im letzten Schritt wurde das **Interface** erstellt. Dabei lag der Fokus auf einer benutzerfreundlichen Gestaltung, die eine intuitive Navigation und Interaktion ermöglicht. Entwürfe und Prototypen wurden iterativ entwickelt und durch Feedback von potenziellen Nutzern verfeinert. Um die Ergebnisse der Analyse und das Konzeptionsvorgehen strukturiert aufzubereiten, wurde ein **Analyse-Workshop** durchgeführt, in dem die Erkenntnisse gemeinsam mit Vertretern der Zielgruppe diskutiert wurden (Kumar, 2013). 

## 3.2 Anwendungsfälle

Die Anwendungsfälle bieten eine Möglichkeit, die Ergebnisse der Analyse zu konkretisieren und zu verdeutlichen, wie das geplante System in der Praxis eingesetzt wird. Sie helfen dabei, die Nutzerinteraktionen und die damit verbundenen Anforderungen zu skizzieren, ohne bereits ins Detail der technischen Umsetzung zu gehen. Die folgenden Anwendungsfälle illustrieren typische Szenarien, in denen Nutzer auf das System zugreifen werden.


**Erster Anwendungsfall: Validierung von Informationen**
Eine Person stößt über soziale Medien oder andere Plattformen auf Informationen, die überraschend, dramatisch oder im Widerspruch zu ihrem aktuellen Wissensstand stehen. In diesem Moment möchte sie die Validität der Informationen überprüfen, um fundierte Entscheidungen zu treffen oder ihre Meinung zu bilden. Das System ermöglicht es der Person, die entsprechenden Aussagen schnell zu verifizieren, indem es über eine Suchfunktion alle Debatten zu dem gewünschten Thema und seiner Aktualität auflistet. Dies soll ein informiertes und kritisches Herangehen an politische Inhalte fördern.


**Zweiter Anwendungsfall: Überblick über neue Beschlüsse**
Eine Person steht vor der Herausforderung, auf der Grundlage neuer Beschlüsse Entscheidungen für ihre eigenen Vorhaben zu treffen. Um dies zu tun, benötigt sie einen schnellen und klaren Überblick darüber, welche Beschlüsse im Landtag angenommen oder abgelehnt wurden. Das System soll eine übersichtliche Darstellung dieser Informationen, inklusive einer Zusammenfassung der wichtigsten Punkte und Argumente. Diese Funktion ermöglicht es der Person, schnell zu erfassen, welche Auswirkungen die Beschlüsse auf ihre Planung haben können.


 **Dritter Anwendungsfall: Überblick über Debatten während der Wahlperiode**
Eine Person möchte sich einen Überblick darüber verschaffen, welche Debatten während der aktuellen Wahlperiode geführt wurden. Sie möchte durch die verschiedenen Sitzungen stöbern und sich gezielt mit den Themen auseinandersetzen, die sie interessieren. Das System bietet eine benutzerfreundliche Möglichkeit, durch die Protokolle der Debatten zu navigieren, sodass die Nutzerin oder der Nutzer relevante Sitzungen auswählen und detaillierte Informationen zu spezifischen Themen einsehen kann. Diese Funktion fördert ein besseres Verständnis der politischen Diskussionen und Entscheidungen, die die Wahlperiode geprägt haben.



## 3.3 Funktionalitäten

Im Rahmen der Konzeptionsphase wurde "Card Sorting" als Methode gewählt, um die Funktionalitäten der geplanten Plattform zu definieren und zu priorisieren. Beim Card Sorting wurde eine Teilnehmergruppe von 3 weibliche studierenden, zwischen 20-26 Jahren, alle Funktionalitäten aus der Analysephase auf Zettel auf einem Miro-Board dargestellt. Die Gruppe sollte als nächstes die Zettel Inhaltlich Gruppieren und anschließend besonders wichtige Features priorisieren. Diese Methode soll dabei helfen, die mentalen Prozesse besser nachvollziehbar zu machen, welche Funktionalitäten wichtig sind und erwartet werden (ZITIEREN). In der Abbildung 1 wird das Ergebnis des Card Sorting-Prozesses dargestellt, das die thematischen Gruppierungen und deren übergeordnete Themen visualisiert. 

![[remote-blog/BachelorArbeitObsidian/Konzeptionsphase/InhalteStruktieren.canvas|InhalteStruktieren]]
Die Ergebnisse des Card Sortings lassen sich in vier klare Kategorien einteilen: **Inhalte**, **Beschreibung**, **Design** und **Features**.
In der Kategorie **Inhalte** ist besonders wichtig, dass alle Argumente in dafür als auch dagegen aufgelistet werden und zudem eine Verlinkung zur Originalquelle erfolgt, idealerweise mit der genauen Seitenzahl. Zusätzlich sollten die Abstimmungen der jeweiligen Sitzung leicht auffindbar sein.
Für das **Design** wurde der Wunsch nach einer modernen und minimalistischen Gestaltung deutlich. Außerdem ist es essenziell, dass das Interface durch ein responsives Design von allen Geräten aus problemlos zugänglich ist. Zudem wurde eine intuitive Navigation über eine kombinierte Top- und Seitenleiste gefordert, um die Bedienung zu erleichtern.
Bei der **Beschreibung** war es besonders wichtig, dass die Hintergrundinformationen zu den Debatten in einem kurzen, prägnanten Absatz angeboten werden, um den Nutzern einen schnellen Überblick zu ermöglichen.
Die Kategorie **Features** umfasst den Wunsch nach einer leistungsfähigen Suchfunktion sowie einer barrierefreien Gestaltung. Dazu gehören unter anderem optimierte Farben und Kontraste, eine einfachere Sprache und die Option, Textinhalte in Audio umzuwandeln (Text-to-Speech).
Diese Struktur stellt sicher, dass sowohl funktionale als auch ästhetische Anforderungen der Nutzer berücksichtigt werden und die Plattform für eine breite Zielgruppe nutzerfreundlich gestaltet wird.


## 3.4 Systemarchitektur

## Webseiten
Die vorgestellten Funktionalitäten erfordern eine durchdachte Systemarchitektur, um eine effiziente und skalierbare Lösung zu gewährleisten. Deswegen wird ein Ansatz basierend auf dem Model-View-Controller (MVC)-Architekturmuster verwendet. Diese Struktur stellt sicher, dass die Verantwortlichkeiten klar aufgeteilt sind, und bietet eine Grundlage für Erweiterbarkeit sowie Wartbarkeit des Systems. Die drei Hauptkomponenten (Model, View, Controller) interagieren miteinander, um die verschiedenen Anforderungen der Webseiten zu erfüllen.

**Landingpage**
Die Landingpage dient als Einstiegsseite und zentraler Anlaufpunkt für Nutzende. Sie bietet eine Übersicht der neuesten Sitzungen und Beschlüsse sowie eine zentrale Suchfunktion. Diese Suchfunktion stellt die Kernfunktionalität der Seite dar, um Nutzern schnellen Zugang zu spezifischen Themen zu ermöglichen.

| **Model**      | - neuesten Informationen zu Sitzungen und Beschlüssen<br>- Verwendet Abfragen für aktuelle Daten und Beschlüsse                                                                                  |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **View**       | - Benutzeroberfläche zeigt offentsichtliche Suche, sowie eine Übersicht über die neueste Sitzung/Beschlüsse<br>- Min. modernes Design, das den ersten Eindruck prägt und intuitiv zugänglich ist |
| **Controller** | - steuert Interaktion zwischen Nutzereingaben (Suchfunktion) und den Datenmodellen<br>-Bei Suchanfragen ruft Controller spezifischen Themen aus der Datenbank                                    |

**Debatten-page**
Diese Seite bietet eine kompakte, aber umfassende Übersicht über alle Sitzungen und Debatten, einschließlich ihrer Themen, Argumente und Vorschläge. Nutzer sollen sich schnell einen Überblick verschaffen können und bei Bedarf tiefer in spezifische Themen eintauchen können.

| **Model**      | - Stellt umfangreiche Informationen zu allen Sitzungen, Debatten, Abstimmungen und Argumenten bereit<br>- Muss logisch strukturiert sein, um schnelle Abfragen zu ermöglichen                                                             |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **View**       | - Ausgewogene Gestaltung, die umfassende Informationen bietet und gleichzeitig die Übersichtlichkeit wahrt<br>- Ermöglicht die Navigation zwischen verschiedenen Sitzungen und Debatten<br>- Benutzerfreundlich, ohne überladen zu wirken |
| **Controller** | - Verwaltert die Datenanforderungen der View<br>- Organisiert und bündelt Informationen zu Debatten, um diese in kompakter Form bereitzustellen                                                                                           |


**Drucksachen-page**
Diese Seite bietet detaillierte Informationen zu einer einzelnen Drucksache. Hier sollen die Informationen, die auf der Debatten-page kompakt dargestellt wurden, umfassender und übersichtlicher aufbereitet werden. Zudem ermöglicht die Seite den Zugriff auf vorherige oder nachfolgende Drucksachen.

| **Model**      | - Liefert spezifische Daten zu einer Drucksache sowie deren Argumente und Vorschläge<br>- Fokussierte Abfragen reduzieren die Datenlast und verbessern die Ladezeiten                                                              |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **View**       | - Bietet mehr Raum für die Darstellung der Inhalte<br>- Das Layout ist professionell und informativ, ohne jedoch langweilig zu wirken<br>- Ermöglicht es Nutzern, detailliert in die einzelnen Aspekte der Drucksache einzutauchen |
| **Controller** | - Ruft nur die relevanten Daten der ausgewählten Drucksache ab und übergibt diese an die View<br>- Regelt die Navigation zwischen vorherigen und nachfolgenden Drucksachen                                                         |



### Datenbankmodell
Die Struktur der Datenbank ist so gestaltet, dass sie die parlamentarischen Abläufe  nachvollziehbar abbildet. Im Zentrum steht die **Wahlperiode** und innerhalb von der finden viele **Sitzungen** statt, in denen viele verschiedene Themen diskutiert werden. Jede Sitzung bezieht sich auf eine Vielzahl von **Drucksachen**, die als parlamentarische Dokumente oder Gesetzesvorlagen eine zentrale Rolle im Debattenprozess einnehmen.

Eine **Drucksache** ist dabei immer einem bestimmten **Thema** zugeordnet und kann durch die Diskussion in einer Sitzung zu einer Abstimmung führen. Das Modell sieht vor, dass über jede Drucksache abgestimmt werden kann, wobei die Ergebnisse der Abstimmung – also die **Ja-Stimmen**, **Nein-Stimmen** und **Enthaltungen** – sowie die Verteilung der Stimmen nach Fraktionen in der Datenbank festgehalten werden. Diese Struktur ermöglicht es, sowohl die inhaltlichen Diskussionen als auch die formalen Abstimmungen detailliert nachzuvollziehen.

Ein weiterer wichtiger Bestandteil der Drucksachen sind die dazugehörigen **Argumente**. Jede Drucksache kann eine Vielzahl von Argumenten enthalten, die entweder für oder gegen die Drucksache sprechen. Jedes **Argument** besteht aus einem Text, der eine bestimmte Position darstellt und von einer **Fraktion** stammt. Zudem wird die Quelle des Arguments – sei es ein schriftliches Dokument oder eine Rede – ebenfalls dokumentiert. Diese Argumente sind essenziell, um die verschiedenen Sichtweisen und Diskussionen innerhalb des parlamentarischen Prozesses transparent darzustellen.

Darüber hinaus bietet die Struktur der Datenbank die Möglichkeit, **Vorschläge** und **Alternativanträge** zu erfassen. Eine Drucksache kann verschiedene **Alternativvorschläge** oder **alternative Drucksachen** enthalten, die von anderen Fraktionen eingebracht werden. Diese Alternative dienen dazu, unterschiedliche Lösungsvorschläge für ein bestimmtes Problem zu präsentieren oder bestehende Drucksachen zu ergänzen oder zu modifizieren.

![[databaseStructure.canvas|databaseStructure]]

## 3.5 Interface Design

Das User Interface stellt den Kern der Interaktion zwischen der Plattform und den Nutzern. In einem Iteretativen Prozess wurde von einfachen Papierskizzen bis zu einem interaktiven Interface in Form eines Mock-Ups abgeschlossen.

### **Papierskizzen**
Die erste Phase der Interface-Gestaltung umfasste die Erstellung verschiedener Papierprototypen und einzelner Elemente (siehe Abbildung 1). Diese Prototypen dienten dazu, erste Ideen hinsichtlich Layouts und Stilrichtungen festzuhalten und zu visualisieren. Die Wahl von Papier als Medium erfolgte bewusst, um Flexibilität zu gewährleisten und schnelles, unkompliziertes Feedback zu ermöglichen.

![[IMG_20241011_093202.jpg|500]]
Abbildung 1


**Idee 1**
In der ersten Designidee werden die grundlegenden Funktionen ähnlich implementiert, jedoch in einem modernen und lebendigen Layout. Die Grundstruktur der Webseite präsentiert Titel und Beschreibungstexte auf der linken Seite in einer ansprechenden Bubble-Form. Diese Darstellung fungiert als primäres visuelles Element und ermöglicht den Nutzern, jederzeit zu erkennen, wo sie sich auf der Webseite befinden und welches Thema im Fokus steht.

Die Bubble-Elemente fördern nicht nur die Orientierung, sondern regen die Nutzer auch zur Interaktion an, indem sie dazu ermutigt werden, tiefer in die Inhalte einzutauchen. Die Konsistenz dieses Designs zieht sich durch alle drei Seiten der Webseite und gewährleistet somit ein einheitliches Nutzererlebnis (siehe Abbildung 1).

Zudem wird die Verbindung zwischen den Seiten durch ein durchgängiges Navigationskonzept gestärkt. Jede Seite ist strategisch miteinander verlinkt, sodass Nutzer nahtlos zwischen den Themen wechseln können. Diese intuitive Navigation ermöglicht den Nutzern, schnell und unkompliziert auf verwandte Inhalte zuzugreifen, wodurch die Gesamterfahrung der Webseite bereichert wird. Der Fokus liegt hierbei nicht nur auf visueller Konsistenz, sondern auch auf der Schaffung eines innovativen und eigenständigen Designs, das die Benutzerfreundlichkeit optimiert.

![[IMG_20241011_093232.jpg]]


**Idee 2:**
Die zweite Designidee verfolgt das Ziel einer klar strukturierten und benutzerfreundlichen Darstellung. Im Zentrum steht eine Landingpage (Blatt 1 in Abbildung 2), die den Fokus auf Debatten oder die Suchfunktion lenkt. Dies erleichtert den Nutzern den schnellen Zugang zu relevanten Informationen, indem sie unmittelbar zu den gewünschten Inhalten navigieren können. Weiter unten auf der Seite sind die aktuellsten Sitzungen sowie die Abstimmungen der letzten Tagungsübersicht zu finden.

Auf der Debattenseite (Blatt 2 in Abbildung 2) wird eine intuitive Navigation implementiert. Auf der linken Bildschirmseite befindet sich eine Navigationsleiste, die es ermöglicht, mühelos zwischen verschiedenen Sitzungen zu wechseln. Auf der rechten Bildschirmseite wird eine Inhaltsübersicht platziert, die es den Nutzern erlaubt, gezielt zwischen den besprochenen Themen einer Sitzung hin- und herzuspringen. Diese duale Navigationsstruktur gewährleistet eine schnelle Orientierung und erleichtert den Zugang zu spezifischen Diskussionsthemen. Der Hauptbereich der Seite, zentral auf dem Bildschirm positioniert, ist für die detaillierte Darstellung der Themen einer Sitzung vorgesehen. Hier finden sich alle Informationen zu den behandelten Themen, ihren Hintergründen sowie den vorgebrachten Argumenten und Alternativvorschlägen. Das Layout folgt dem Prinzip des F-Form-Musters (Nielsen, 2006), einem bewährten Designansatz, der das natürliche Leseverhalten der Nutzer auf Webseiten berücksichtigt. Durch die Anordnung der Informationen in dieser Struktur wird gewährleistet, dass die wichtigsten Inhalte schnell erfasst werden, während tiefere Informationen für interessierte Nutzer leicht zugänglich bleiben.

Durch die Interaktion mit den Titeln eines Themas gelangen die Nutzer direkt zu den detaillierten Inhalten auf der Drucksachen-Seite (Blatt 3 in Abbildung 2). Sobald diese spezifische Ansicht aufgerufen wird, erfolgt eine Änderung im Layout: Alle Menüs und Navigationselemente werden ausgeblendet, um den Fokus vollständig auf die Inhalte des Themas zu lenken. Der gewonnene Raum auf dem Bildschirm wird durch vergrößerten White Space sowie eine größere Schriftgröße genutzt, um eine angenehmere und leserfreundlichere Darstellung der Informationen zu ermöglichen. Diese Reduktion auf das Wesentliche und die bewusste Gestaltung des freien Raums verbessern nicht nur die Lesbarkeit, sondern fördern auch die Konzentration auf die zentralen Inhalte des Themas.

Durch diese Kombination aus strukturiertem Design, benutzerzentrierter Navigation und fokussierter Informationsdarstellung wird eine Umgebung geschaffen, die sowohl eine schnelle Informationserfassung als auch eine tiefgehende Auseinandersetzung mit den Inhalten unterstützt.

![[IMG_20241011_093225.jpg]]



**Nutzerfeedback:**
Das Nutzerfeedback von einer Studentin und einem jungen Erwachsenen zeigt, dass das erste Layout zwar ansprechender wahrgenommen wurde, jedoch Orientierungsschwierigkeiten auftraten. Insbesondere wurden die "Bubbles" als Werbeobjekte interpretiert. Zudem fiel negativ auf, dass die mobile Version überdimensionierte Farbflächen aufwies. Im zweiten Design wurde die Struktur positiv hervorgehoben. Die Menüs wurden schnell erkannt und der Hauptinhalt identifiziert. Negativ wurde jedoch die Eintönigkeit angesprochen, was auf die fehlenden tatsächlichen Informationen zurückgeführt wurde. Basierend auf diesem Feedback wurde das zweite Design priorisiert. Nutzer besuchen Webseiten nicht primär aufgrund ihrer visuellen Attraktivität; entscheidend ist die Benutzerfreundlichkeit, die es ermöglicht, Aufgaben schnell und effizient zu erledigen (Lindgaard, G., et all, 2003). 



### **Rapid Prototyping**
Der Papier-Prototyp wurde in der nächsten Iteration als Wireframes umgesetzt, um ein Gefühl für die Menge und Anordnung der tatsächlichen Informationen zu vermitteln. Auch hierbei wurden wurden 2 Ansätze tiefer verfolgt und anschließend in einem Workshop für Feedback analysiert.

**Layout 1**
Die erste Landing Page soll Themen aus den letzten zwei Sitzungen durch interaktive Elemente durch das Zenter als eine Art Galerie durch bewegen. Zusätzlich sollen die Abstimmungen der letzten Tagung im selben Stil angezeigt werden. Zusätzlich eine zentrale Suche in der Top-Bar um direkt sein Thema suchen zu können (siehe Abbildung 3). Die Intention des Layouts war, den Nutzer mit Beispielthemen neugierig zu machen auf die aktuellen geschehnisses des Landtags-Schleswig Holsteins zu machen.
![[Screenshot from 2024-10-11 10-10-15.png]]

Auf der Debattenpage sollen die Sitzungen (hier Platzhalter Sitzung 24) in dem linken Menü hinzugefügt werden. Auf der rechten Seite sind die Themen der Sitzung zu finde. So ist es dem Nutzer möglich zu überprüfen, ob Themen dabei sind, die ihn interessieren. In der Mitte des Bildschirms ist, wie auf dem Papier-Prototypen, der Hauptkontent. Dargestellt werden Elemente wie die Sitzung auf der sich der Nutzer befindet und ihr Datum, sowie der Titel des ersten Themas und sein Hintergrund. Darunter werden dann die Argumente in Pro und Kontra darstellung aufgelistet. Mit dem zweiten Tab (Nummer 8, Abbildung 3), können die Parteien zu ihren Standpunkten eingeblendet werden und falls vorhanden, Alternativvorschläge/Anträge. Dieser Extra Interaktionsschritt soll den "My Side" Effekt reduzieren (Quelle?) und den Nutzer dazu nudgen, sich erst mit den Argumenten der Debatte auseinanderzusetzen, bevor er die Argumente seiner präferierten Partei übernimmt. Der Nudge basiert auf dem "least effort" Prinzip von Kahnemann. Mit dem Stil werden alle Themen der Sitzung untereinander aufgelistet (siehe Abbildung 3).

![[Screenshot from 2024-10-11 10-10-34.png]]

Auf der Drucksachen-Seite werden die zuvor ausgewählten Themen, entweder von der Debattenseite oder den Suchergebnissen, angezeigt. Der Inhalt bleibt dabei konsistent, jedoch soll die Darstellung größer und übersichtlicher erfolgen. Diese gestalterischen Anpassungen sind in diesem Mock-Up noch nicht vollständig umgesetzt, da der Fokus in dieser Phase auf der reinen Verfügbarkeit der Informationen liegt. Die Darstellung der Argumente erfolgt in Form von sogenannten "Cards", die auf Grundlage des Gestaltgesetzes der **Nähe** umgesetzt werden. Dieses Gesetz besagt, dass Elemente, die nahe beieinander positioniert sind, als zusammengehörig wahrgenommen werden. Dadurch sollen die Argumente klar als eine kohärente Informationseinheit erfasst werden (Abbildung 4).

In derselben Ansicht werden auch Alternativvorschläge angezeigt, sodass der Nutzer direkt zwischen verschiedenen Ansätzen oder Positionen wählen kann. Der Tab „Parteistandpunkte“ listet zudem die beteiligten Parteien der Landesregierung auf und zeigt deren jeweilige Positionen, Argumente und Vorschläge in Bezug auf das Thema. Diese klare und strukturierte Präsentation unterstützt die Nutzer dabei, die Standpunkte der Parteien sowie die zugrundeliegenden Argumente schnell und effizient zu erfassen (Abbildung 5).  Auf der mobilden Ansicht, wird die Inhaltsangabe von den Themen, in die Linke Übersicht verschoben und wird durch das Hamburgermenüitem geöffnet. Somit sind die Themen unter der Sitzung aufgeslisted.

![[Screenshot from 2024-10-11 10-10-52.png]] 
![[Screenshot from 2024-10-11 10-11-07.png]]

Die Suche ist von jeder Seite aus zu erreichen und soll den Hintergrund undeutlich machen. Die Such-Ergebnisse sollen den Titel des Themas, die Drucksache, die Sitzung und das Datum wiedergeben. Sollten mehrere Suchergebnisse zu dem genau selben Thema erscheinen, sollen diese nach Aktualität sortiert werden, sodass die aktuellsten Ergebnisse ganz oben gelistet sind.

![[Screenshot from 2024-10-11 10-10-44.png]]





**Layout 2**  
Der größte Unterschied befindet sich in der Landingpage, hier sollen statt zufällige aktuelle Themen, die Themen der aktuellsten Drucksache aufgelistet werden (Abbildung 6). Die Abstimmungsergebnisse werden auch nicht mehr dynamisch, sondern statisch angezeigt und werden durch das Gestaltprinzip der Kontinuität darauf eindeuten, dass gescrollt werden muss, um die restlichen zu finden (sollten es mehr Abstimmungen sein, als auf den Bildschirm passen, was selten der Fall ist). Zusätzlich wird das Video der letzten Debatte verlinkt, um einen schnellen Zugang zu der Originalquelle zu haben.

![[Screenshot from 2024-10-11 10-22-17.png|520]]![[Screenshot from 2024-10-11 15-42-31.png|150]]

Die anderen Seiten des zweiten Layouts sind ähnlich aufgebaut, jedoch wird stärker mit Abständen (Spacing) gearbeitet, um eine noch klarere Struktur zu schaffen. Auf der Debattenseite werden die Sitzungen (z. B. Sitzung 24) ebenfalls im linken Menü aufgelistet, während auf der rechten Seite die Sitzungsthemen erscheinen. Der Hauptinhalt in der Mitte bleibt vergleichbar mit Layout 1, mit den Details zur Sitzung, dem Datum und dem ersten Thema, sowie einer Pro- und Kontra-Darstellung der Argumente. Über einen Schalter (Nummer 8, Abbildung 3) lassen sich die Standpunkte der Parteien einblenden. Dieser zusätzliche Interaktionsschritt zielt ebenfalls darauf ab, den "My Side"-Effekt zu reduzieren und den Nutzer dazu zu animieren, sich zunächst mit den Argumenten der Debatte auseinanderzusetzen, bevor er die Positionen seiner bevorzugten Partei übernimmt. Auch hier basiert der Nudge auf dem "Least Effort"-Prinzip von Kahnemann.



![[Screenshot from 2024-10-11 10-22-24.png]]

![[Screenshot from 2024-10-11 10-22-29.png]]

![[Screenshot from 2024-10-11 10-22-35.png]]

![[Screenshot from 2024-10-11 10-22-40.png]]

![[Screenshot from 2024-10-11 10-22-48.png]]

![[Screenshot from 2024-10-11 10-22-55.png]]

![[Screenshot from 2024-10-11 10-23-01.png]]

![[Screenshot from 2024-10-11 10-23-04.png]]

Mobile:
![[Screenshot from 2024-10-11 15-41-54.png]]

![[Screenshot from 2024-10-11 15-41-59.png]]

![[Screenshot from 2024-10-11 15-42-04.png]]



**Feedback**

Um zu ermitteln, welche Elemente der beiden Layouts bei den Nutzern besser ankommen, wurde ein 30-minütiger Workshop durchgeführt. Der Workshop basierte auf den Erkenntnissen der Analysephase und legte besonderen Wert auf das Feedback zu Layout, Informationsmengen und Usability. Das Feedback der Teilnehmer wurde sowohl in Form von Kommentaren als auch durch vier "Entweder-oder"-Fragen erfasst. Diese dienten dazu, ein finales Layout zu entwickeln, das die am besten bewerteten Elemente kombiniert. Das Endergebnis sollte dann in der nächsten Iteration mit funktionstüchtigen Mock-Ups umgesetzt werden.

In der Abstimmungsrunde des Workshops mit 6 Teilnehmern entschieden sich 67 % der Teilnehmer für das strukturierte Layout (Layout 2) der Landingpage. Dies deutet auf eine Präferenz für eine klarere und besser organisierte Struktur hin (Abb.4). Hinsichtlich der Informationsdarstellung gab es mit 50 % keine klare Tendenz zwischen den beiden Layouts, was auf eine ausgeglichene Wahrnehmung dieser Designaspekte hinweist (Abb.6). Die Darstellung der Suchfunktion, bei der das Abtrennen durch Layout mit dem Abtrennen durch Whitespace verglichen wurde, erhielt jedoch mit einer deutlichen Zustimmung von 100 % als effektiver bewertet (Abb. 7). Bei der letzten Abstimmung, in der visuelle Hierarchien im Fokus standen, entschied sich eine Mehrheit von 57 % für das Layout mit größerer Schrift und klareren Unterschieden zwischen Titeln und Paragraphen, was die Benutzerfreundlichkeit durch verbesserte Lesbarkeit unterstreicht (Abb. 8).

![[Bildschirmfoto 2024-09-09 um 09.54.50.png|150]] ![[Bildschirmfoto 2024-09-09 um 09.54.56.png|150]] ![[Bildschirmfoto 2024-09-09 um 09.55.10.png|150]] ![[Bildschirmfoto 2024-09-09 um 09.55.05.png|150]]

Im Rahmen des Workshops wurden die Prototypen nicht nur präsentiert, sondern auch direkt für die Teilnehmer getestet angeboten. Zum Abschluss des Workshops fand eine offene Feedbackrunde statt, in der die Teilnehmer ihre Eindrücke und Verbesserungsvorschläge teilten. Dabei wurden angesprochen, dass nicht alle Argumente eindeutig in Pro- und Kontra-Kategorien eingeteilt werden können, was die Strukturierung der Inhalte in einigen Fällen erschweren könnte. Dennoch wurde der Vorschlag, das Video der letzten Sitzung direkt auf der Seite einzubinden, positiv aufgenommen, insbesondere da es auf der Originalwebseite schwer auffindbar ist. Die Navigation wurde hingegen von den Nutzern als verbesserungswürdig eingestuft. Dabei war unklar, welche Menüleiste auf der derzeitigen Seite navigiert und welche zwischen den Seiten navigiert. Mehr Kontextinformationen, insbesondere zu politischen und gesellschaftlichen Hintergründen, wurden als wünschenswert erachtet, um den Nutzern ein besseres Verständnis der Themen zu ermöglichen.

Zusätzlich wurde angemerkt, dass deutliche **Call-to-Action-Elemente** fehlen. Solche Elemente könnten die Nutzer stärker dazu animieren, sich aktiv mit den Inhalten auseinanderzusetzen oder direkt in Interaktion zu treten, wodurch die Usability der Webseite insgesamt verbessert werden könnte.

**Mock Ups**
Der nächste Schritt bei der Entwicklung des User-Interfaces bestand darin, eine detaillierte visuelle Darstellung der Webseite zu erstellen, die dem finalen Design möglichst nahekommt. Denn nach Sharp, Rogers und Preece (2007) sind Mockups effektiv, um potenzielle Designprobleme zu identifizieren. In diesem Stadium wurden auf Basis des Nutzerfeedbacks konkrete Entscheidungen zur Layoutsverbesserung, sowie eine Farbpalette, Typografie, Bildauswahl und Layoutanpassungen getroffen. Da es sich um eine Webanwendung im Bundesland SH handelt, wurde als Primärfarbe eine gesättigte Form des Rot und als Sekundär das Blau von der Flagge Schleswig-Holsteins gewählt, dies soll an den lokalen Geostandpunkt erinnern. Die Schriftfamilie "Switzer" (Webseitenverlinkung) kombiniert eine moderne und zeitlose Ästhetik, inspiriert von den Neo-Grotesk-Schriften der 1980er und 1990er Jahre. Obwohl dieser Stil nicht in der Schweiz entstanden ist, wurde er von heimischen Designern stark geprägt. (Webseitenverlinkung nachfügen). Die H1 ist nicht die größte Überschrift, fällt aber aus durch die besonders große Font-Weight und der Primärfarbe. Die größte H-Überschrift ist H2 und alle folgenden Text-Stile werden kleiner und oder verlieren Kontrast, um eine klare Hierarchie für den Nutzenden beim lesen anzubieten (Link zu Gestaltgesetzt).  

![[UI-Stylesheet.png]]

Durch das Style-Sheetsheat wird der Stil auf der Webseite einheitlich, was den Kognitive Load der Nutzenden gering hält, und somit die Usability stärkt. Das Ziel ist es, dass die Funktionalität, dem Design folgt, deswegen gibt es lediglich eine kleine Auswahl an Button/Links und Stilmittel die Elemente bekommen, mit denen interagiert werden kann. So müssen die Nutzenden der Webseite nur einmal die Funktionalität der Elemente "erlernen" und können bei dem nächsten mal, wenn sie auf ein ähnliches Element mit dem selben Stil gelangen, die zu erwartende Funktionalität erfüllt bekommen. Zusätzlich wurde auf einen Hohen Kontrast zwischen Schrift und Hintergrund geachtet, und das Line-Spacing von ... für optimale Lesbarkeit bei längeren Texten angepasst. 
Die für die Landingpage übernommenen Elemente setzen sich aus der Übersicht der Themen von der Aktuellsten Sitzung (und ihren Hintergründen) und der dazu Hochgeladenen Sitzung zusammen, einer Top-Navbar und der Abstimmungsergebnisse. Die Cards der Abstimmungsergebnisse wurden insofern verwändert, dass sie hervorheben, ob einem Thema (Drucksache) zugestimmt oder abgelehnt wird, statt Kreisdiagramme, da nicht bei jeder Abstimmung die Stimmenanzahl gegeben ist. Zusätzlich wurden rote und grüne Hintergrundfarben hinzugefügt, zu schnellen Identifikation des Ergebnisses, wobei für die Berücksichtigung von Barrierefreiheit ein Daumenicon mit Label hinzugefügt wurde. Bei Interaktion mit der Card, wird diese geflippt und das Abstimmungsverhalten der Parteien wird in die 3 Kategorien "Dafür", "Dagegen" und "Enthalten" eingeordnet. Diese Kategorien werden durch die Daumenicons repräsentiert und in der Implementierung mit einem "Screen-Read-Only" label versehen, dass keine visuelle Darstellung hat. Die Suche ist groß und mittig auf der Navigationsbar zu finden und öffnet beim anklicken ein Overlay für die Eingabe und die Suchergebnisse.  


![[Pasted image 20241015075122.png]]


Die Dokumentenseite ist mit dem Grundlegenden Layout der Wireframes übernommen. So ist auf der linken Seite eine Navigation zwischen den Verschiedenen Dokumenten zu finden- Über die sind die Debatten und Abstimmungen zu erreichen, wobei der Fokus in der Implementierung bei den Debatten gesetzt wird. Die ausgewählte Sitzung wird im Zentrum mit ihren Themen (Drucksachen) aufgelistet, so dass der Nutzer sich über die Themen informieren kann. Auch hier wurden die Stile des Style-Sheats angewand, wodurch die H1 Überschriften etwas kleiner und Rot sind, und als Ankerpunkt dienen, sodass der Nutzer weiß, wenn er orientierungslos sein sollte, kann er über die Roten Titel schnell herausfinden wo er sich aufhält. Der Hintergrund bekommt ein leichtes Blau als Hintergrundfarbe, sodass die Nutzenden es als Informationselement wahrnehmmen. Unter der Beschreibung befinden sich die Tabs für Argumente, wobei das ausgewählte argument farbig Hervorgehoben wird um als "aktiv" wahrgenommen zu werden. Die Verlinkung sind durch die Primärlinkfarbe eindeutig zu identifizieren. 
![[Pasted image 20241015075202.png]]

Unter den Debatten befinden sich alle Abstimmungen der Sitzung, im selben Stil wie der Landingpage um gebrauch von dem Gestaltgesetzt der Kontinuität zu machen (Quelle einfügen).
![[Pasted image 20241015075306.png]]


![[Pasted image 20241015075218.png]]

![[Pasted image 20241015075241.png]]
## 3.6 Fazit der Konzeption

--- vs ---

3.1 Inhalte Strukturieren
3.2. UI erstellen (Skizzen $\rightarrow$ Prototypen (Rapid Prototyping) $\rightarrow$ Wireframes $\rightarrow$ Mockups)
3.3. Ux-Tests $\rightarrow$ LeanUX (Remote-Usability Tests oder Guerilla-Tests)


# Datenqualität KIAZ
- Präsentationen aufbereiten
- Beispiele, 
- Visualisierung des Mehrwaufwands und den niedrigeren Ständen, 

13.11 

Quellen:
Nielsen, J. (2006). F-shaped pattern for reading web content. _Nielsen Norman Group_. https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/

Lindgaard, G., & Dudek, C. (2003). What is this evasive beast we call user satisfaction? _Journal of Usability Studies_, 1(2), 100-109

>[!NOTE] Test
>test

https://befonts.com/switzer-font-family.html