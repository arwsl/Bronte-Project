# Bronte-Project
[DE] Rezeptesammlung - vegane Ideen in LaTeX gegossen

Mit Hilfe des <img src="https://latex.codecogs.com/gif.latex?\LaTeX" />-Pakets [`xcookybooky`](https://www.ctan.org/pkg/xcookybooky).

## Inhalte dieser `README.md`
* [Inhalte des Kochbuchs](#Inhalte)
* [Beitrag leisten](#Beitragleisten)
  * [Synopse: `xcookybooky`-Paket](#Synopse)
  * [Rezept einpflegen](#einpflegen)
    * [Ordnerstruktur im Repository](#Ordnerstruktur)
    * [`recipe`-Umgebungen](#recipe-Umgebungen)
    * [`siunitx`-Paket](#siunitx)
    * [Abbildungen](#Abbildungen)
    * [Stichwortverzeichnis](#Stichwortverzeichnis)
    * [Rezept einbinden](#einbinden)
    * [Code-Beispiel](#Code-Beispiel)

---
<a name="Inhalte"></a>
# Inhalte des Kochbuchs

---
<a name="Beitragleisten"></a>
# Beitrag leisten
Für jeden, der sich am Kochbuch beteiligen will - vor allem aber für mich selbst - ist die Zusammenfassung von allen wichtigen Befehlen und Funktionsweisen der LaTeX-Inhalte. Das `xcookybooky`-Paket liefert das Framework und ist selbst in weiten Teilen sehr modular nutzbar. Ich habe aber eine (übersichtliche?) Ordnerstruktur entworfen und eigene `recipe`-Umgebungen definiert, die die eigentliche `xcookybooky`-Umgebung erweitern. Abbildungen und Einträge im Stichwortverzeichnis lassen sich für jedes Rezept hinzufügen.

<a name="Synopse"></a>
## Synopse: [`xcookybooky`](https://www.ctan.org/pkg/xcookybooky)-Paket

<a name="einpflegen"></a>
## Rezept einpflegen

<a name="Ordnerstruktur"></a>
### Ordnerstruktur im Repository

```
│
├── Frühstück
│   └── Zerealien
├── Gebaeck
│   ├── Brote
│   ├── Kekse
│   └── Kuchen
├── Getraenke
│   ├── alkoholische_Getraenke
│   └── nichtalkoholische_Getraenke
├── Hauptgerichte
│   ├── Auflaeufe
│   ├── Fingerfood
│   ├── Nudelgerichte
│   ├── Pfannengerichte
│   └── Suppen_und_Eintoepfe
├── Nachspeisen_und_Snacks
│   ├── Nachspeisen
│   └── Snacks
└── Vorspeisen_und_Beilagen
    ├── Aufstriche_und_Dips
    └── Salate
```

<a name="recipe-Umgebungen"></a>
### `recipe`-Umgebungen

<a name="siunitx"></a>
### [`siunitx`](https://ctan.org/pkg/siunitx)-Paket

<a name="Abbildungen"></a>
### Abbildungen

<a name="Stichwortverzeichnis"></a>
### Stichwortverzeichnis

<a name="einbinden"></a>
### Rezept einbinden

<a name="Code-Beispiel"></a>
### Code-Beispiel

```latex
\begin{RECIPE-UMGEBUNG}
    [
        preparationtime = {\SI{ZEIT}{\minute}},
        bakingtime = {\SI{ZEIT}{\minute} bis \SI{ZEIT}{\minute}},
        bakingtemperature = {\protect\bakingtemperature{fanoven=\SI{TEMPERATUR}{\celsius}}},
        portion = {PORTIONEN/MENGE},
        source = {QUELLE/HERAUSGEBER}
    ]
    {REZEPTNAME}

    \graph
        {
            big=TEIL/KAPITEL/REZEPT/big.jpg,
            small=TEIL/KAPITEL/REZEPT/small.jpg
        }

    \introduction{
        EINLEITUNG
    }

    \ingredients{
        \SI{1}{\ml} & ZUTAT 1 \\
        \SI{2}{\g} & ZUTAT 2 \\
        \\
        \multicolumn{2}{l}{\textbf{ABSCHNITTÜBERSCHRIFT}} \\
        \SI{3}{\EL} & ZUTAT 3 \\
        4 PRISEN & ZUTAT 4
    }

    \preparation{
        \step ANTLEITUNG IN MEHREREN SCHRITTEN
        \step NÄCHSTER SCHRITT...
    }

    \suggestion[TITEL EINES VORSCHLAGS]{
		VORSCHLAG (DURCH HORIZONTALE LINIE VOM REZEPT GETRENNT)
    }

    \hint{
        HINWEIS (IN EINEM KASTEN UNTEN AUF DER SEITE)
    }

\end{RECIPE-UMGEBUNG}
```
