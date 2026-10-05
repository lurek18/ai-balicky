# Projektový start — průvodce (v0.2)

> Pro koho: každý, kdo s AI dělá víc než jednorázový úkol, ať je to vývoj, výzkum, analýza, výběr dodavatele, školení nebo interní proces.

## Obsah složky

| Soubor | Co s ním |
|---|---|
| `00-PRUVODCE.md` | Čteš ho teď. Pojmy a postup podle nástroje. |
| `01-PRIPRAVA-ZADANI.md` | Vložíš do chatu a AI tě dokoučuje k zadání. Výsledek je `PROJEKT-START.md`. |
| `02-PROVOZ-PROJEKTU.md` | Příručka pro běžící projekt: rytmus práce, typické chyby. |

---

## 1. Potřebuju vůbec projekt? (filtr)

| Otázka | Když ANO |
|---|---|
| Zvládnu to v jednom sezení a nebudu se k tomu vracet? | **Chat.** Projekt nezakládej. Stačí dobře napsané zadání. |
| Budu na tom pracovat ve víc sezeních a potřebuju navazovat? | **Lehký projekt** (2 soubory) |
| Má to fáze, rozhodnutí, víc lidí nebo nástrojů, trvá to týdny? | **Plný projekt** (5 souborů) |

Nevíš? Začni lehkým. Na plný se dá kdykoli rozšířit.

**Návaznost na AI pracovní kompas.** Máš Kompas? Začni tam. Nemáš? Začni rovnou `01-PRIPRAVA-ZADANI.md`.
Kompas rozhoduje jen **Chat, nebo Project**. To, jestli jde o dlouhodobý projekt, posoudíš ty podle jeho doporučení:

| Kompas doporučil | Práce je… | Co udělat |
|---|---|---|
| Chat | jednorázovka | použij Kompasův handoff, Projektový start nepotřebuješ |
| Project | opakovaná se stejnými pravidly (např. měsíční report) | použij Kompasův handoff, Projektový start nepotřebuješ |
| Project | s fázemi a rozhodnutími, na týdny | handoff **nezakládej**. Otevři nový chat s `01-PRIPRAVA-ZADANI.md` a vlož do něj Kompasův handoff (přesná věta je na začátku `01`). |

| Balíček | Kam patří | Kdy |
|---|---|---|
| AI Kompas (`runtime-kernel.md` + `AI-pracovni-kompas.md` + `product-truth.yaml`) | vlastní Project „AI pracovní kompas" (kernel do Instructions, další dva do knowledge) | jednou, pak jen aktualizace |
| `01-PRIPRAVA-ZADANI.md` | nový chat | u každého dlouhodobého projektu |
| `PROJEKT-START.md` | prázdná složka v Coworku, nebo nový Project | jednou na projekt |
| `00` a `02` | nikam, ke čtení | když si nevíš rady |

## 2. Proč ne jeden nekonečný chat

Chat **není paměť**. Po desítkách zpráv AI zapomíná zadání, protiřečí si a ty opakuješ kontext. Nikdo jiný (kolega ani nový chat) se v tom nevyzná.

Představ si AI jako **nového kolegu, kterého zaučuješ**. Když mu řekneš jen „udělej to", bude hádat. Když mu dáš zadání, pravidla a lístek „kde jsme skončili", pracuje samostatně.

Projekt proto drží paměť **v souborech, ne v chatu**. Pracuje se takto: **jeden projekt, v něm nový chat na každý úkol.**

## 3. Soubory projektu

**Lehký projekt (začátečníci): dva soubory, které udržuješ**

| Soubor | Lidsky | Co v něm je |
|---|---|---|
| **BRIEF** | Zadání od šéfa | Cíl, pro koho, rozsah, pravidla, co je „hotovo". Na konci přibývají rozhodnutí. |
| **WORKLOG** | Předávací lístek na konci směny | Rozdělané, otevřené otázky, další krok, nápady na později |

V agentních nástrojích vznikne ještě krátký technický soubor `AGENTS.md`. Ten řeší agent, ty ho měnit nemusíš.

**Plný projekt:**

| Soubor | Lidsky | Co v něm je | Mění se |
|---|---|---|---|
| **BRIEF** | Zadání od šéfa | Proč projekt existuje, cíl, rozsah | Skoro nikdy |
| **Pravidla projektu** (`AGENTS.md`) | „Jak to u nás chodí" | Role AI, pravidla, postup | Zřídka |
| **DECISIONS** | Zápis z porad | Co jsme rozhodli a proč | Jen přibývá, nemaže se |
| **WORKLOG** | Předávací lístek | Aktuální stav a další krok | Každé sezení |
| **NOTES** | Šuplík na nápady | Nápady mimo aktuální krok | Průběžně |

**Příklady:**

| | Vývoj aplikace | Výzkum |
|---|---|---|
| BRIEF | „Rezervační appka pro členy klubu" | „Jak konkurence používá AI v podpoře?" |
| Pravidlo | „Kapacita se nesmí přečerpat" | „Jen ověřené zdroje, vždy odkaz a datum" |
| DECISIONS | „Webová appka, ne nativní" | „Zužujeme na trh EU" |
| WORKLOG | „Rozdělaná obrazovka rezervace" | „Zpracované 3 z 8 firem" |
| NOTES | „Nápad: věrnostní body" | „Vedlejší zdroj o legislativě" |

**Pravidlo pořádku:** každá informace má **jedno místo**. Nápad → NOTES → dostane zadání → WORKLOG → rozhodnuto → DECISIONS, nebo dokončeno → výstup.
Mazat se smí jen z NOTES a WORKLOG. BRIEF a DECISIONS se nemažou.

> `AGENTS.md` je společný název pro „pravidla projektu" v AI nástrojích. V Claude nebo ChatGPT Projectu žádný soubor nepotřebuješ. Pravidla vložíš do pole **instrukcí projektu**.

## 4. Postup

1. **Připrav zadání.** Otevři chat, vlož `01-PRIPRAVA-ZADANI.md`, napiš „Začínáme". AI určí režim (chat / lehký / plný) a provede tě. Na konci dostaneš `PROJEKT-START.md`.
2. **Založ projekt** v nástroji podle tabulky níže.
3. **Ověř, že to funguje.** Zakládací chat **zavři**. Otevři nový chat ve stejné složce nebo Projectu a zeptej se: *„Jaký je cíl projektu, hlavní pravidlo a další krok?"* Odpověď porovnej s BRIEF a WORKLOG. Když nesedí: zkontroluj, že jsi ve správné složce nebo Projectu a že tam soubory jsou. Pak napiš *„Přečti AGENTS.md a WORKLOG.md"* a test zopakuj. Když teď sedí, začínej touhle větou každou práci.
4. **Pracuj v rytmu** podle `02-PROVOZ-PROJEKTU.md`: „pokračujeme" na začátku, „zapiš stav" na konci.

## 5. Založení podle nástroje

### Agent zakládá soubory sám (doporučeno)

Vždy: **prázdná složka → ulož do ní jen `PROJEKT-START.md` → otevři v nástroji právě tuto složku → napiš:** *Přečti PROJEKT-START.md a proveď část A.*

| Nástroj | Jak otevřít složku | Poznámka |
|---|---|---|
| **Claude Code** | Terminál: `cd "cesta/ke/složce"` a `claude`, nebo záložka Code v desktop appce | Pravidla se načítají přes `CLAUDE.md` → `@AGENTS.md` |
| **Codex** | Terminál `codex` ve složce, nebo složka jako workspace v appce/IDE | Čte `AGENTS.md` ve složce, ve které je spuštěný |
| **Claude Cowork** | Desktop appka → Add folder → vyber složku | Načítání pravidel ověř testem z kroku 3 |
| **Gemini CLI** | Terminál `gemini` ve složce | Agent nastaví `.gemini/settings.json`, jinak Gemini čte jen `GEMINI.md` |
| **Antigravity** | Otevři složku jako workspace | Novější verze čtou `AGENTS.md`. Limit asi 12 000 znaků na soubor pravidel |

### Ruční varianta (Claude Project, ChatGPT Project, Gemini Gem, obyčejný chat)

1. Založ projekt (nebo Gem), vlož `PROJEKT-START.md` a napiš: *Přečti PROJEKT-START.md a proveď část A v ruční variantě.*
2. AI vypíše **Pravidla a zadání**. Ty vlož do pole instrukcí projektu nebo Gemu.
3. AI vypíše **STAV PROJEKTU**, krátký blok o tom, kde jsi. Ulož si ho do poznámky a vlož ho na začátek každého nového chatu v projektu. **V obyčejném chatu bez instrukcí** vkládej celý **balíček pro návrat** (pravidla + zadání + stav), jinak chat ztratí pravidla.
4. Na konci práce: „zapiš stav". Dostaneš nový STAV PROJEKTU a starý nahradíš.

Ruční varianta je dobrý start. Když tě kopírování stavu začne obtěžovat, je čas přejít na Cowork nebo Claude Code. **Systém je stejný, jen stav zapisuje agent místo tebe.**

## 6. Kterou cestu zvolit

- **Znám jen chat:** příprava v chatu → ruční varianta v Claude Projectu → časem Cowork.
- **Používám projekty nebo Cowork:** příprava v chatu → Cowork.
- **Pracuju v terminálu nebo s kódem:** Claude Code, Codex, Gemini CLI.

## 7. Mapa stavových bloků (kam co patří)

| Blok | Odkud | Kam ho vložíš |
|---|---|---|
| `compass_checkpoint_v1` | AI Kompas | zpátky do **Kompasu**, když se k němu vracíš |
| `PRIPRAVA_CHECKPOINT` | přerušená příprava zadání | do nového chatu s `01-PRIPRAVA-ZADANI.md` |
| `STAV PROJEKTU` | ruční varianta projektu | na začátek nového chatu v **pracovním** projektu |
| balíček pro návrat | ruční varianta v obyčejném chatu | na začátek nového obyčejného chatu |

„Pokračujeme" piš v **pracovním projektu**. V Kompasu ta věta spouští jiný režim (návrat přes checkpoint).

## 8. Bezpečnost

- Do přípravy zadání nepiš hesla, osobní údaje ani citlivá data.
- Firemní data patří do firemních účtů (Team/Enterprise), ne do osobních free účtů.
- Agentovi dej vlastní složku, ne celý disk.

## 9. Co je ověřené

Postup pro Codex, Gemini CLI a Antigravity vychází z jejich dokumentace. Načítání pravidel v Claude Code (`@AGENTS.md`) a v Coworku zatím ověřuje test z kroku 3. Neber ho jako samozřejmost.
