# Landingpage
```
import Link from "next/link";

import { Span } from "next/dist/trace";
import { notFound } from "next/navigation";
import SecondPage from "@/components/landingpage/SecondPage";
import MainPage from "@/components/landingpage/MainPage";
import { getData } from "@/components/serverComponents";

export default async function HomePage() {
  const data = await getData();

  return (
    <div className="relative w-full">
      <div className="fixed w-full z-40">
        <div className="px-16 flex  justify-between items-center py-4 border border-red-200 bg-white ">
          <Link href="/" className="text-xl blur-none">
            LT-Debatten SH
          </Link>
          <nav className="hidden md:flex gap-12 items-center text-md font-semibold">
            <Link className="nav-link" href="/plenardokumente">Plenardokumente</Link>
            <Link className="nav-link" href="/ki-info">KI-Info</Link>
            <Link className="nav-link" href="/about">About us</Link>
            <Link className="nav-link" href="/posts">Posts</Link>
          </nav>

          
          <div className="flex md:hidden items-center gap-4">
            <button className="p-2">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" className="w-6 h-6">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
              </svg>
            </button>
            <button className="p-2">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" className="w-6 h-6">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6h16M4 12h16M4 18h16" />
              </svg>
            </button>
          </div>        </div>
      </div>

      {/* Main content of the homepage */}
      <MainPage />

      {/*Second Page */}
      <SecondPage data={data} />
    </div>
  );
}

```


## Main Page
```
"use client";
import Image from "next/image";
const MainPage = () => {
  return (
    <header className=" relative ">
      <div className="fixed inset-0 -z-10 mt-80">
        <div className="relative w-full h-screen">
          <Image
            src="/images/LandtagSH.jpg"
            alt="Background image"
            fill
            style={{ objectFit: "cover" }}
            quality={100}
            priority={true}
          />
          <div
            className="absolute inset-0 bg-gradient-to-b from-white from-10%  via-30% to-transparent"
            style={{ height: "70%" }}
          ></div>
        </div>
      </div>
      <div className="relative flex flex-col min-h-screen justify-between max-w-6xl mx-auto pt-20 sm:pt-24 lg:pt-32 border border-red-200 ">
        {/* Landing Screen */}
        <div className="flex flex-col items-center justify-center gap-8 mt-24 ">
          <h1 className="text-center title">
            Das IT-System für den politischen Überblick in Schleswig-Holstein
          </h1>

          <div className="flex flex-col items-center justify-center gap-4 max-w-3xl ">
            <p className="text-xl text-center leading-8 mx-16">
              Verschaffe dir schnell eine Übersicht zu allen{" "}
              <span className="text-lapis-500">Sitzungen</span> und deren
              <span className="text-lapis-500"> Argumente</span>,{" "}
              <span className="text-lapis-500">Standpunkte</span> der Parteien
              und den Status der{" "}
              <span className="text-lapis-500">Abstimmungen</span>.
            </p>

            <div className="flex gap-4">
              <button className="btn-primary">Los gehts</button>
              <input
                className="border-2 border-gray-300 rounded-md p-2 w-fill drop-shadow-strong"
                type="text"
                placeholder="Thema suchen..."
              />
            </div>
          </div>
        </div>

        <div className="flex flex-row translate-y-40 bg-white -mx-8 pt-4 z-30 rounded-lg">
          <div className="w-1/3 px-8">
            <h2 className=" text-xl font-semibold">Landtagssitzungen</h2>
          </div>
          <div className="flex flex-col  gap-4 w-2/3 px-8">
            <p className="text-lg text-zinc-500 leading-7">
              Landtagstagungen sind die offiziellen Sitzungen des Parlaments
              eines Bundeslandes, in denen die Abgeordneten über Gesetze und
              politische Themen beraten und abstimmen. Sie folgen einer
              festgelegten Tagesordnung und behandeln verschiedene
              landespolitische Fragen wie Bildung, Wirtschaft und Gesundheit.
              Regierungsmitglieder nehmen daran teil, um die Position der
              Landesregierung zu vertreten. Die Sitzungen sind in der Regel
              öffentlich, um Transparenz zu gewährleisten, und enden oft mit
              Abstimmungen, die die politische Ausrichtung des Landes festlegen.
            </p>
            <button className="btn-secondary text-lg ">Alle Sitzungen</button>
          </div>
        </div>
      </div>
    </header>
  );
};

export default MainPage;

```


## SecondPage.js
```
"use client";

import NeuesteSitzung from "./NeuesteSitzung";

const SecondPage = ({ data }) => {
  return (
    <div className="bg-white w-full ">
      <div className="relative max-w-6xl mx-auto pt-20 sm:pt-24 lg:pt-32 border border-red-200">
        <div className="flex flex-row  justify-center  ">
          <div className="flex flex-col items-center border border-red-200 w-full mt-64">
            <h2 className="text-3xl font-semibold">Aktuellste Tagung</h2>
            <p className="text-zinc-400 text-lg">
              {data[data.length - 1].sitzung.datum}
            </p>

            <div className="mt-16 w-full aspect-video">
              <iframe
                className="w-full h-full rounded-2xl"
                src="http://m7k.ltsh.de/486x374/2024-07-19T09.59.23.932P02.00.mp4#t=0"
                title="Letzte Tagung Video"
                frameBorder="0"
                loading="lazy"
                allowFullScreen
                autoPlay={false}
              ></iframe>
            </div>
          </div>
        </div>

        <NeuesteSitzung data={data} />
      </div>
    </div>
  );
};

export default SecondPage;

```

## NeuesteSitzung.js
 ```
"use client";
import { useState } from "react";

const NeuesteSitzung = ({ data }) => {
  const [showDescriptions, setShowDescriptions] = useState({});

  const toggleDescription = (index) => {
    setShowDescriptions((prev) => ({
      ...prev,
      [index]: !prev[index],
    }));
  };

  const newestSitzung =
    data.length > 0
      ? data.reduce((prev, current) =>
          prev.sitzung.number > current.sitzung.number ? prev : current,
        )
      : null;

  return (
    <div className="flex flex-row mt-32 h-screen">
      <div className="w-1/3">
        <h2 className="text-2xl font-semibold">
          Sitzung{" "}
          {data.length > 0
            ? newestSitzung.sitzung.number
            : "Keine Sitzungen verfügbar"}{" "}
          (neu)
        </h2>
      </div>
      <div className="flex flex-col gap-4 w-2/3">
        <table className="w-full">
          <tbody>
            {data.length > 0 &&
              newestSitzung.sitzung.drucksachen.map((item, index) => (
                <tr key={item.id || index}>
                  <td
                    className={`p-4 ${
                      index % 2 === 0 ? "bg-white" : "bg-lapis-100/50"
                    } flex justify-between items-center`}
                  >
                    <div className="flex flex-col w-full">
                      <div className="flex flex-row justify-between items-start">
                        {item.istneu && (
                          <div className="absolute -translate-x-5 -translate-y-5 px-2 font-extrabold uppercase bg-lapis-500 text-white inline-block rounded-full text-xs">
                            Neu
                          </div>
                        )}
                        <h1 className="text-md font-semibold ">{item.titel}</h1>
                        <button
                          onClick={() => toggleDescription(index)}
                          className="transform transition-transform duration-200 hover:scale-110"
                        >
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            strokeWidth="2"
                            stroke="currentColor"
                            className={`w-6 h-6 transition-transform ${
                              showDescriptions[index] ? "rotate-90" : ""
                            }`}
                          >
                            <path
                              strokeLinecap="round"
                              strokeLinejoin="round"
                              d="m8.25 4.5 7.5 7.5-7.5 7.5"
                            />
                          </svg>
                        </button>
                      </div>
                      {/* Content stays mounted, but visibility is controlled via CSS */}
                      <div
                        id={`desc-${index}`}
                        className={`transition-all ease-in-out duration-500 overflow-hidden ${
                          showDescriptions[index]
                            ? "max-h-96 opacity-100"
                            : "max-h-0 opacity-0"
                        }`}
                        style={{
                          maxHeight: showDescriptions[index] ? "200px" : "0px",
                          opacity: showDescriptions[index] ? 1 : 0,
                        }}
                      >
                        <div className="mt-2">
                          <span className="font-semibold"> Hintergrund: </span>
                          {item.hintergrund}
                        </div>
                      </div>
                    </div>
                  </td>
                </tr>
              ))}
          </tbody>
        </table>
      </div>
    </div>
  );
};

export default NeuesteSitzung;


```


# Bachelor Arbeit schreiben
