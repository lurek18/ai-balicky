# Provoz projektu — jak pracovat, aby se neztratil fokus (v0.2)

> Pro projekt založený přes `PROJEKT-START.md`. Platí pro lehký i plný projekt. Co je jen pro plný, je označeno.

## 1. Tři věty, které jsou celý návyk

| Kdy | Co napíšeš | Co se stane |
|---|---|---|
| Začátek práce | **„Pokračujeme."** | AI přečte WORKLOG (a zadání) a navrhne další krok. V ruční variantě nejdřív vlož STAV PROJEKTU, v obyčejném chatu celý balíček pro návrat. Píše se v pracovním projektu, ne v Kompasu. |
| Během práce | **„Zapiš do poznámek."** / **„Zapiš rozhodnutí."** | Nápad nebo rozhodnutí jde na své místo a ty pokračuješ v úkolu. |
| Konec práce | **„Zapiš stav."** | AI přepíše WORKLOG. V ruční variantě vypíše nový STAV PROJEKTU, který si uložíš. |

**Jeden projekt, v něm nový chat na každý úkol.** Dlouhý chat nezachraňuj. Zapiš stav a otevři nový.

Když AI v novém chatu neví, kde jste, napiš: *„Přečti AGENTS.md a WORKLOG.md."* (v ruční variantě vlož STAV PROJEKTU).

## 2. Kam co patří

| Situace | Lehký projekt | Plný projekt |
|---|---|---|
| Směr a cíl projektu | BRIEF | BRIEF (změna jen vědomě a se záznamem v DECISIONS) |
| „Tohle vždy dodržuj / nikdy nedělej" | BRIEF: pravidla | Pravidla projektu (AGENTS) |
| „Rozhodli jsme X, protože Y" | BRIEF: rozhodnutí během projektu | DECISIONS |
| „Na tomhle se dělá / tohle čeká" | WORKLOG | WORKLOG |
| „Možná by bylo fajn…" | WORKLOG: nápady na později | NOTES |
| Hotová práce | výstupní soubory | výstupní soubory |

Mazat se smí jen z WORKLOG a NOTES. Rozhodnutí se nemažou. Když se změní, přidá se nové.

**Ruční varianta:** rozhodnutí se drží ve STAVU PROJEKTU. Na konci každé fáze je přepiš do instrukcí projektu (v obyčejném chatu do balíčku pro návrat), aby nezmizela.

## 3. Fáze a kontrola

- Projekt jde po krocích nebo fázích z BRIEF. Každý má „hotovo" a první konkrétní krok.
- Na konci fáze napiš: *„Shrň fázi: co je hotovo, co jsme rozhodli, co zůstává otevřené."*
- Když chceš přeskočit, AI na to upozorní. Přeskočit můžeš, ale vědomě.

## 4. Kdy lehký projekt rozšířit na plný

- Rozhodnutí v BRIEF je tolik, že se v nich ztrácíš.
- Na projektu začne pracovat další člověk nebo další nástroj.
- Objeví se fáze, které na sebe navazují.

Řekni: *„Rozšiř projekt na plný."* AI vytvoří DECISIONS, NOTES a plná pravidla a přesune do nich obsah.

## 5. Dva prostory: rozhodovací a prováděcí (plný projekt, volitelné)

Jen když vidíš signály:
- v jednom chatu se střídá „o čem přemýšlíme" a „co přesně děláme",
- opakovaně se vracíte k uzavřené diskusi,
- provádění je dlouhé a mechanické a diskuse ho ruší.

| | Rozhodovací | Prováděcí |
|---|---|---|
| Účel | směr, varianty, oponentura | práce podle zadání |
| Zapisuje | DECISIONS, NOTES | WORKLOG, výstupy |
| Při rozporu | rozhodne a zapíše | **zastaví dotčený krok**, zapíše „Nález k rozhodnutí", pokračuje jen v tom, čeho se rozpor netýká |

Spojují je **soubory, ne kopírování chatu**.

Příklady: vývoj (návrh × implementace), výzkum (otázka a metodika × sběr a zpracování zdrojů), školení (osnova × psaní lekcí).

## 6. Typické chyby

| Příznak | Oprava |
|---|---|
| AI neví, kde jsme | Chybí „zapiš stav" na konci. V novém chatu: „Přečti AGENTS.md a WORKLOG.md." |
| AI zjevně nečte pravidla | Test: „Jaký je cíl, hlavní pravidlo a další krok?" Když nesedí, začínej každou práci výzvou ke čtení souborů. |
| AI znovu otevírá rozhodnuté věci | Rozhodnutí nejsou zapsaná. „Zapiš rozhodnutí." |
| AI „vylepšuje", co nechceš | Doplň pravidlo („žádná vylepšení mimochodem") |
| Projekt se rozrůstá | Doplň „mimo rozsah" v BRIEF, nápady odkládej |
| Chat je pomalý a zmatený | Zapiš stav, otevři nový chat |
| Zadání přestalo platit | Vědomě uprav BRIEF a zapiš rozhodnutí, nebo připrav nové zadání přes `01-PRIPRAVA-ZADANI.md` |

## 7. Úrovně

- **Začátečník:** lehký projekt, tři věty z kapitoly 1, ruční varianta nebo Cowork.
- **Pokročilý začátečník:** plný projekt, aktivně udržovaná pravidla a rozhodnutí, rozšíření podle kapitoly 4.
- **Pokročilý:** dva prostory, víc nástrojů nad stejnými soubory (např. návrh v Claude, realizace v Codexu), soubory v gitu.
