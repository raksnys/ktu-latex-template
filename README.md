# KTU LaTeX šablonas (2026)

**Neoficialus** LaTeX šablonas Kauno technologijos universiteto (KTU) Informatikos fakulteto
bakalauro baigiamajam projektui, atnaujintas pagal **2026 m.** šabloną
(studijų programa „Programų sistemos“, 6121BX012).

*Unofficial LaTeX template for Kaunas University of Technology (KTU) bachelor's final degree
projects, updated to the 2026 Faculty of Informatics format. English summary at the bottom.*

Pavyzdinis sugeneruotas dokumentas: [`main.pdf`](main.pdf).

## Kas įgyvendinta

- A4, paraštės 30 / 10 / 20 / 20 mm, Times 12 pt, eilučių intervalas 1,15, 10 pt tarpas tarp pastraipų.
- Trys viršeliai: pirmasis viršelis, formalus titulinis su vadovu ir recenzentu, akademinio sąžiningumo deklaracija.
- Santraukos lietuvių ir anglų kalbomis su automatiniu puslapių skaičiumi.
- Turinys, lentelių ir paveikslų sąrašai su taškinėmis linijomis, be poskyrių įtraukos.
- Skyriai pradedami naujame puslapyje, numeracija „1.“, „1.1.“, „1.1.1.“.
- Lentelės 10 pt su pavadinimu viršuje („1.1 lentelė.“), paveikslų pavadinimai apačioje („1.1 pav.“), numeracija pagal skyrių.
- Literatūros sąrašas pagal ISO 690 (`ktu_lt.bst` + `natbib`), įrašai numeruojami „1.“, „2.“…
- `\usecasespec{...}`: panaudojimo atvejo (PA) specifikacijos lentelė.
- `\priedas{...}`: priedų antraštės „N priedas. Pavadinimas“, priedų lentelės ir paveikslai numeruojami „P1“, „P2“…
- Privalomas 2026 m. skyrius „Dirbtinio intelekto naudojimo savirefleksija“.

## Failai

| Failas | Paskirtis |
|---|---|
| `main.tex` | Pagrindinis dokumentas, sujungia visas dalis |
| `variables.tex` | Pavadinimas, autorius, vadovas, recenzentas, raktiniai žodžiai (LT ir EN) |
| `ktu_thesis_style.sty` | Visas maketavimas: šriftai, paraštės, antraštės, lentelės, sąrašai, makrokomandos |
| `ktu_lt.bst` | Literatūros sąrašo stilius (ISO 690) |
| `TitlePage.tex`, `PageSecond.tex`, `PageThird.tex` | Viršeliai ir akademinio sąžiningumo deklaracija |
| `PageSummaryLT.tex`, `PageSummaryEN.tex` | Santraukos |
| `chapters/*.tex` | Skyrių šablonai su pavyzdžiais |
| `references.bib` | Pavyzdiniai literatūros įrašai |

## Naudojimas

1. Nukopijuokite saugyklą (*Use this template*, *fork* arba `git clone`).
2. Užpildykite `variables.tex`.
3. Rašykite tekstą `chapters/` aplanke, šaltinius dėkite į `references.bib`.
4. Pašalinkite `\usepackage{lipsum}` ir `\lipsum[...]` pavyzdinį tekstą.
5. Kompiliuokite: `pdflatex → bibtex → pdflatex → pdflatex`, arba `latexmk -pdf main.tex`.

VS Code + LaTeX Workshop konfigūracija pateikta `.vscode/settings.json`.

### PA specifikacijos pavyzdys

```latex
\usecasespec{
  label=tab:pa-perziureti-irasus,
  pa=Peržiūrėti įrašus,
  tikslas=Atvaizduoti visus naudotojui prieinamus įrašus.,
  aprasymas={Naudotojas pasirenka „Įrašai“. Sistema pateikia sąrašą.},
  pries=Naudotojas prisijungęs prie sistemos.,
  aktoriai={Naudotojas, Administratorius},
  ispleciantys=Peržiūrėti įrašo informaciją,
  apimami=--,
  specializuojami=--,
  po=Naudotojas mato įrašų sąrašą.
}
```

Reikšmes, kuriose yra kablelių, apgaubkite `{...}`.

## English summary

A 2026 update of the unofficial KTU thesis template. Fill in `variables.tex`, write chapters in
`chapters/`, add sources to `references.bib`, and build with `latexmk -pdf main.tex`
(or `pdflatex`, `bibtex`, `pdflatex` ×2). Works with TeX Live and MiKTeX.

## Kilmė ir licencija

Šablonas paremtas [Dominyk4s/KTU-LaTeX](https://github.com/Dominyk4s/KTU-LaTeX) darbu ir platinamas
pagal tą pačią [MIT licenciją](LICENSE). `ktu_lt.bst` remiasi `unsrtnat.bst` (Patrick W. Daly, LPPL).

Šablonas nėra oficialus KTU dokumentas. Prieš pateikdami darbą visada pasitikrinkite einamųjų
metų fakulteto reikalavimus.
