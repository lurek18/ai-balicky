<!-- VZOR: takhle vypadá hotový PROJEKT-START.md, který vytvoří kouč zadání (01-PRIPRAVA-ZADANI.md). Slouží jako ukázka, nezakládej podle něj vlastní projekt. -->

# PROJEKT-START: Výzkum AI v zákaznické podpoře (vzor)

> Režim: plný · Úroveň: pokročilý · Nástroj: Cowork

---

## A) POKYNY PRO AGENTA — proveď v tomto pořadí

Zakládáš nový projekt. Tento soubor je tvoje jediné zadání. Samotnou práci na projektu nezačínej, jen ho připrav.

### Krok 1 — Prostředí
- Umíš vytvářet soubory ve složce? Ano → **plná varianta** (Krok 2). Ne → **ruční varianta** (Krok 2b).
- Složka má obsahovat jen `PROJEKT-START.md`. Když v ní je cokoli dalšího, nic nepřepisuj. Vypiš obsah a zeptej se, jak pokračovat.

### Krok 2 — Vytvoř soubory (plná varianta)
Obsah ber z části B a šablon z části C. Nic si nevymýšlej. Co v části B chybí, zapiš jako otevřenou otázku.

**Lehký projekt:**
1. `BRIEF.md` = celá část B.
2. `WORKLOG.md` podle šablony. Aktuální krok = první krok z části B. Otevřené otázky převezmi z části B.
3. `AGENTS.md` podle **lehké** šablony (technický soubor, uživatel ho nemusí řešit).

**Plný projekt:**
1. `BRIEF.md` = celá část B.
2. `AGENTS.md` podle **plné** šablony. Doplň role AI, pravidla a fáze z části B.
3. `DECISIONS.md`: zapiš „Už rozhodnuté věci" z části B jako D-001, D-002…
4. `WORKLOG.md`: aktuální fáze = fáze 1, další krok = její první krok, otevřené otázky z části B.
5. `NOTES.md` podle šablony.

**Navíc podle nástroje** (aby se pravidla načítala sama):
- **Claude Code / Cowork:** `CLAUDE.md` s jediným řádkem `@AGENTS.md`.
- **Codex:** nic. Čte `AGENTS.md` ve složce, ve které je spuštěný.
- **Gemini CLI:** `.gemini/settings.json` s obsahem `{"context": {"fileName": ["AGENTS.md", "GEMINI.md"]}}`.
- **Antigravity:** nic. Pokud verze `AGENTS.md` nečte, vytvoř `GEMINI.md` s textem „Řiď se souborem AGENTS.md."

Git: navrhni `git init` a první commit, proveď ho až po souhlasu.

### Krok 2b — Ruční varianta (Project / Gem / chat)
1. Vypiš **Pravidla a zadání** jako jeden blok kódu: obsah lehké nebo plné šablony AGENTS a pod ním celá část B.
   - **Claude/ChatGPT Project, Gem:** vloží se jednou do pole **instrukcí** (Instructions). Pak v každém novém chatu stačí STAV PROJEKTU.
   - **Obyčejný chat bez instrukcí:** spoj Pravidla a zadání se STAVEM PROJEKTU do jednoho **BALÍČKU PRO NÁVRAT**, který se vkládá na začátek každého nového chatu. Bez pravidel by chat ztratil rozsah a mantinely.
2. Vypiš **STAV PROJEKTU** (formát v části C). Řekni uživateli, ať si ho uloží (poznámka, dokument) a vloží ho na začátek každého nového chatu.
3. Vysvětli rytmus ruční varianty: *„Na konci práce napiš ‚zapiš stav'. Vypíšu nový STAV PROJEKTU a ty si starý nahradíš. V novém chatu ho vložíš jako první zprávu."*

### Krok 3 — Ověřovací test (povinné)
Ověř, že pravidla opravdu fungují:
- Řekni uživateli, ať **tento chat zavře** a otevře **nový chat ve stejné složce** (plná varianta) nebo **ve stejném Projectu** (ruční, po vložení STAVU nebo balíčku pro návrat). Teprve tam napíše: *„Jaký je cíl projektu, hlavní pravidlo a další krok?"* V tomhle chatu test nedělej, tady odpovídáš z konverzace, ne ze souborů.
- **Očekávaná odpověď:** cíl z BRIEF, první pravidlo ze sekce pravidel, další krok z WORKLOG. Vypiš je uživateli předem, aby měl s čím porovnat.
- **Když nesedí, diagnostika v tomto pořadí:**
  1. Je nový chat opravdu ve stejné složce nebo Projectu?
  2. Jsou ve složce soubory `AGENTS.md`, `BRIEF.md`, `WORKLOG.md` (a u Claude Code/Coworku `CLAUDE.md`)?
  3. Zkus *„Přečti AGENTS.md a WORKLOG.md"* a test zopakuj. Když teď sedí, nástroj soubory nečte sám. Pak touhle větou začínej každou práci.
  4. Ruční varianta: jsou pravidla v Instructions, nebo jsi vložil celý balíček pro návrat?

### Krok 4 — Rekapitulace (povinné)
1. Vypiš vytvořené soubory a jednou větou, k čemu který je.
2. Shrň projekt do 5 bodů: cíl, pro koho, první výstup, hlavní pravidlo, další krok.
3. Polož **3 kontrolní otázky** na nejslabší místa zadání (zejména otevřené otázky).
4. Navrhni **první malý úkol** (do jednoho sezení) a zeptej se, jestli začít.
5. Vysvětli rytmus: *„Na začátku řekni ‚pokračujeme'. Na konci řekni ‚zapiš stav'. Nápady mimo úkol: ‚zapiš do poznámek'."*

---

## B) ZADÁNÍ PROJEKTU

### Cíl (jedna věta)
Zmapovat, jak 8 vybraných firem v EU používá AI v zákaznické podpoře, a připravit doporučení pro náš tým podpory.

### Problém / příležitost
Vedení zvažuje AI v podpoře, ale nemáme ověřený přehled, co konkurence skutečně nasadila a co je jen marketing.

### Pro koho a k čemu
Vedoucí zákaznické podpory a vedení firmy. Podklad pro rozhodnutí, jestli a kde AI pilotovat.

### Typ projektu
výzkum/analýza

### Věcná podstata
- Otázka: Jaké AI nástroje 8 firem v EU reálně používá v podpoře, v jakých kanálech a s jakým doloženým výsledkem?
- Jednotka zkoumání: firma (8 firem ze seznamu, který dodá vedoucí podpory).
- Zdroje: veřejné weby firem, případové studie dodavatelů, odborné články, výroční zprávy. Ne fóra a anonymní recenze.
- Citace: každé tvrzení s odkazem a datem přístupu.
- Fakt vs. odhad: u každého zjištění štítek ověřeno / tvrzení firmy / odhad.

### Jak vypadá hotovo
- Celý projekt: tabulka 8 firem + 2stránkové doporučení se 3 variantami pilotu.
- První použitelný výstup: tabulka pro 3 firmy se všemi sloupci a zdroji.

### Rozsah
**V rozsahu:** veřejně dostupné informace, kanály e-mail, chat, telefon; období posledních 2 let.
**Mimo rozsah:** výběr konkrétního dodavatele, cenové nabídky, kontaktování firem, firmy mimo EU.

### Omezení
3 týdny, 1 člověk zhruba 4 hodiny týdně, jen veřejné zdroje.

### Pravidla, která platí vždy
- Jen ověřitelné zdroje s odkazem a datem přístupu.
- Každé zjištění má štítek ověřeno / tvrzení firmy / odhad.
- Žádná interní data naší firmy do AI.

### Postup / fáze
| # | Fáze nebo krok | První konkrétní krok | Hotovo, když… |
|---|---|---|---|
| 1 | Metodika a seznam firem | potvrdit seznam 8 firem a sloupce tabulky | seznam a sloupce schválil vedoucí podpory |
| 2 | Sběr zdrojů | zpracovat první 3 firmy | 3 firmy mají vyplněné všechny sloupce se zdroji |
| 3 | Dokončení sběru | zpracovat zbylých 5 firem | 8 firem v tabulce |
| 4 | Analýza a doporučení | najít opakující se vzorce | 2 strany s 3 variantami pilotu |
| 5 | Předání | prezentace vedení | vedení rozhodlo o pilotu, nebo ho vědomě odložilo |

### Už rozhodnuté věci
| Rozhodnutí | Proč |
|---|---|
| Jen firmy v EU | srovnatelná regulace (GDPR, AI Act) |
| Výstup jako tabulka + krátké doporučení | vedení nechce dlouhý report |

### Otevřené otázky
- Konečný seznam 8 firem (kdo/kdy rozhodne: vedoucí podpory, do konce 1. týdne)
- Hodnotíme i interní AI (asistence agentům), nebo jen zákaznickou? (vedoucí podpory, fáze 1)

### Rizika
- O části firem nebude dost veřejných informací. V tom případě zapsat jako nález a nahradit jinou firmou po dohodě.

### Role AI
- Dělá: hledá a shrnuje zdroje, vyplňuje tabulku, navrhuje vzorce, oponuje závěrům.
- Nedělá: nevymýšlí údaje, nevybírá firmy ani dodavatele, nerozhoduje o metodice.

---

## C) ŠABLONY SOUBORŮ

### Lehká šablona `AGENTS.md`

```markdown
# Pravidla projektu — [NÁZEV]

Na začátku každé práce přečti `BRIEF.md` (zadání) a `WORKLOG.md` (kde jsme).
- Drž se pravidel a rozsahu v BRIEF. Když požadavek koliduje, upozorni dřív, než ho provedeš.
- Nejasné věci se zeptej, nehádej. Nevymýšlej údaje.
- Na začátku práce navrhni další krok podle WORKLOG a počkej na potvrzení.
- Dělej malé kroky. Žádná „vylepšení mimochodem".
- Rozhodnutí zapiš do BRIEF do sekce „Rozhodnutí během projektu" (jen přidávej, s datem). Když se rozhodnutí mění, nemaž staré. Přidej nové s poznámkou „nahrazuje: …".
- Když uživatel řekne „zapiš stav", přepiš WORKLOG.md (rozdělané, otevřené otázky, další krok).
- Nápady mimo aktuální úkol zapiš na konec WORKLOG do sekce „Nápady na později".
```

### Plná šablona `AGENTS.md`

```markdown
# Pravidla projektu (AGENTS.md) — [NÁZEV]

> Návod pro každého, kdo do projektu vstupuje: AI agenta i člověka.

## 1. Tvoje role
Jsi spolupracovník, ne jen vykonavatel.
- Když požadavek koliduje s pravidlem (sekce 3) nebo rozhodnutím v DECISIONS, **upozorni dřív, než ho provedeš**.
- Nejasné věci se zeptej, nehádej. Nevymýšlej údaje.
- O pravidlech a zapsaných rozhodnutích nerozhoduješ sám. Ve WORKLOG je tvůj názor vítaný.
- Role AI: [DOPLNIT]

## 2. Soubory
| Soubor | K čemu | Jak se mění |
|---|---|---|
| BRIEF.md | Původní zadání | Skoro nikdy. Změna jen vědomě, se záznamem v DECISIONS. |
| AGENTS.md | Tato pravidla | Zřídka a záměrně |
| DECISIONS.md | Rozhodnutí a proč | **Jen se přidává, nikdy nemaže** |
| WORKLOG.md | Aktuální stav a další krok | Přepisuje se každou session |
| NOTES.md | Nápady mimo aktuální krok | Průběžně |

**Životní cyklus (mazat se smí jen z NOTES a WORKLOG):**
nápad → NOTES → dostane zadání → WORKLOG (smaž z NOTES) → rozhodnuto → DECISIONS / dokončeno → výstup (smaž z WORKLOG).

## 3. Pravidla, která platí vždy
[DOPLNIT]
Když si dvě pravidla odporují, zastav se a zeptej. Pořadí nerozhoduj sám.

## 4. Fáze
[DOPLNIT tabulku]
Další fáze začíná, až je splněné „hotovo" předchozí.

## 5. Postup pro každý úkol
1. Přečti WORKLOG, podle potřeby BRIEF a DECISIONS.
2. Posuď úkol proti pravidlům a rozhodnutím.
3. Urči nejmenší rozsah a řekni ho jednou větou. Žádná „vylepšení mimochodem".
4. Proveď a ověř podle „hotovo".
5. Shrň změnu v 1–2 větách.
6. Zapiš: rozhodnutí do DECISIONS, nápady do NOTES, stav do WORKLOG.
7. Když práce není hotová, vždy aktualizuj WORKLOG, než skončíš.

## 6. Chaty
Jeden projekt, v něm nový chat na každý úkol. Kontinuitu drží WORKLOG.
Volitelně (pokročilí): rozhodovací prostor (směr, varianty → DECISIONS) a prováděcí prostor (práce podle DECISIONS). Když prováděcí práce narazí na rozpor se zadáním: **zastav dotčený krok**, zapiš ho do WORKLOG jako „Nález k rozhodnutí" a pokračuj jen v tom, čeho se rozpor netýká.
```

### Šablona `WORKLOG.md`

```markdown
# WORKLOG — [NÁZEV]
**Aktualizováno:** [DATUM] · **Fáze/krok:** [DOPLNIT]

## Rozdělané
- …
## Otevřené otázky
- …
## Nálezy k rozhodnutí
- (zatím nic)
## Další krok
[jeden konkrétní úkol pro příští sezení]
## Nápady na později (jen lehký projekt)
- …
```

### Šablona `DECISIONS.md`

```markdown
# DECISIONS — [NÁZEV]
> Jen se přidává. Změněné rozhodnutí neměň. Přidej nové a u starého napiš „nahrazeno D-00X".

| ID | Datum | Rozhodnutí | Proč | Kdo | Stav |
|---|---|---|---|---|---|
| D-001 | | | | | platí |
```

### Šablona `NOTES.md`

```markdown
# NOTES — [NÁZEV]
> Nápady mimo aktuální krok. Nejsou to úkoly ani rozhodnutí. Když nápad dostane zadání, přesuň ho do WORKLOG a tady ho smaž.
```

### Formát `STAV PROJEKTU` (ruční varianta)

```
STAV PROJEKTU — [NÁZEV] — [DATUM]
Fáze/krok: …
Hotovo naposledy: …
Rozdělané: …
Rozhodnuto (nové): …
Otevřené otázky: …
Nápady na později: …
Další krok: …
```