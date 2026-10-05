# Šablony souborů projektu

Hotové prázdné soubory. **Normálně je nepotřebuješ.** Agent je vytvoří sám z `PROJEKT-START.md`.
Hodí se, když chceš projekt založit ručně, bez kouče, nebo když něco ve složce chybí.

| Složka | Kdy | Soubory |
|---|---|---|
| `1 lehky-projekt/` | víc sezení, jeden člověk | BRIEF, WORKLOG, AGENTS (technický), CLAUDE (pro Claude Code/Cowork) |
| `2 plny-projekt/` | fáze, rozhodnutí, víc lidí | BRIEF, AGENTS, DECISIONS, WORKLOG, NOTES, CLAUDE, `.gemini/settings.json` (pro Gemini CLI) |
| `3 rucni-varianta/` | bez agenta (Claude/ChatGPT Project, Gem, chat) | INSTRUCTIONS (do pole Instructions), STAV-PROJEKTU, BALICEK-PRO-NAVRAT (pro obyčejný chat) |

Ruční založení: zkopíruj obsah složky do prázdné složky projektu, vyplň místa `[…]` a `[DOPLNIT]` v BRIEF a AGENTS a pak udělej test z `00-PRUVODCE.md` (krok 3).
`.gemini` je skrytá složka. Na Macu ji ve Finderu zobrazíš zkratkou Cmd+Shift+tečka.
