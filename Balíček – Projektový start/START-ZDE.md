# Projektový start: začni tady

**Co to je:** postup, jak s AI vést delší projekt (vývoj, výzkum, analýzu, školení, interní proces), aby se neztratil směr. Paměť projektu držíš v souborech, ne v jednom nekonečném chatu. AI tě dokoučuje k jasnému zadání a agent ti z něj založí celý projekt.

**Verze:** v0.3 · 10/2026

> **Nejjednodušší cesta:** otevři **https://lurek18.github.io/ai-balicky/**. Tam je celý návod krok za krokem a u každého textu tlačítko **Kopírovat**, takže nemusíš nic stahovat ani otevírat soubory. Tenhle balíček je pro ty, kdo chtějí soubory u sebe.

## Co je v balíčku

| Soubor | K čemu |
|---|---|
| `START-ZDE.md` | tento návod |
| `01-PRIPRAVA-ZADANI.md` | **hlavní soubor.** Vložíš do chatu a AI tě provede přípravou zadání. Výsledek je `PROJEKT-START.md`. |
| `00-PRUVODCE.md` | pojmy, kdy jaký režim, postup podle nástroje (Cowork, Claude Code, Codex, Project, Gemini) |
| `02-PROVOZ-PROJEKTU.md` | jak pracovat v běžícím projektu: rytmus, typické chyby |
| `Prezentace/Projektovy-start-workshop.html` | workshop, návod a tahák v jednom (otevři v prohlížeči, ovládání šipkami) |
| `sablony/` | prázdné soubory projektu (BRIEF, AGENTS, WORKLOG, DECISIONS, NOTES, INSTRUCTIONS…) pro ruční založení, viz `sablony/README.md` |
| `priklady/PROJEKT-START-vzor-vyzkum.md` | ukázka, jak vypadá hotový PROJEKT-START.md |
| `balicek.yaml` | popis balíčku (verze, soubory) |

## Potřebuju to?

- **Zvládnu to za jedno sezení** → stačí chat (nebo AI Kompas). Tenhle balíček nepotřebuješ.
- **Víc sezení, potřebuju navazovat** → lehký projekt (2 soubory).
- **Fáze, rozhodnutí, víc lidí, týdny** → plný projekt (5 souborů).

Máš **AI Kompas**? Začni v něm. Když doporučí Project a práce má fáze a potrvá týdny, pokračuj sem a jeho handoff vlož do kroku 1.

## Tři kroky

**1. Připrav zadání (20–30 min).** Otevři nový chat v Claude, ChatGPT nebo Gemini, vlož nebo nahraj `01-PRIPRAVA-ZADANI.md` a napiš:
- `Začínáme`, nebo
- když přicházíš z Kompasu: *„Tady je handoff z AI Kompasu. Práce bude mít fáze a rozhodnutí, proto jdu přes Projektový start. Převezmi, co už je známé, a doptej se jen na zbytek.“* a pod to celý handoff.

Na konci dostaneš blok textu **PROJEKT-START**. Zkopíruj ho (u bloku je tlačítko Copy). Pro Cowork si ho ulož jako soubor `PROJEKT-START.md`.

**2. Založ projekt (5–10 min).**
- **Claude Project (nejjednodušší, bez souborů):** v Claude **Projects → New project**. Do chatu projektu vlož zkopírovaný PROJEKT-START a pod něj napiš: *Proveď část A v ruční variantě.* Blok **Pravidla a zadání** vlož do **Instructions**, blok **STAV PROJEKTU** si ulož do poznámek.
- **Cowork (pro pokročilé, stav zapisuje agent sám):** vytvoř na disku prázdnou složku a ulož do ní **jen** `PROJEKT-START.md`. V Coworku **Add folder** → tato složka. Napiš: *Přečti PROJEKT-START.md a proveď část A.*
- Další nástroje (Claude Code, Codex, Gemini) najdeš v `00-PRUVODCE.md`, kapitola 5.
- Bez kouče, ručně: zkopíruj obsah `sablony/1 lehky-projekt/` (nebo `2 plny-projekt/`) do prázdné složky a vyplň BRIEF.

**3. Ověř a pracuj.** Zakládací chat **zavři**. Otevři nový ve stejném Projectu (nebo složce v Coworku), v Projectu nejdřív vlož STAV PROJEKTU, a zeptej se: *„Jaký je cíl projektu, hlavní pravidlo a další krok?“* Když odpověď sedí, můžeš pracovat. Když ne, postup je v `00-PRUVODCE.md`, krok 3.

## Každý den

| Kdy | Napiš |
|---|---|
| začátek | „Pokračujeme.“ |
| nápad mimo úkol | „Zapiš do poznámek.“ |
| rozhodnutí | „Zapiš rozhodnutí.“ |
| konec | „Zapiš stav.“ |
| AI neví, kde jste | „Přečti AGENTS.md a WORKLOG.md.“ |

**Jeden projekt, v něm nový chat na každý úkol.** Dlouhý chat nezachraňuj. Zapiš stav a otevři nový.

## Bezpečnost

Do přípravy zadání nepiš hesla, osobní údaje ani citlivá data. Firemní data patří do firemních účtů, ne do osobních free účtů.
