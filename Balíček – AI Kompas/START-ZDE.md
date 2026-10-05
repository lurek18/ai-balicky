# AI pracovní kompas: začni tady

**Co to je:** pomocník v Claude, kterému řekneš, co v práci řešíš. Poradí ti, kde má práce „bydlet“ (jednorázový chat, nebo Project se stálými pravidly) a připraví ti hotové nastavení (handoff). Nic se neinstaluje do počítače. Funguje na claude.ai, stačí i free účet.

**Verze:** RC 0.1 · 10/2026

## Co je v balíčku

| Soubor | K čemu | Kam ho dáš |
|---|---|---|
| `START-ZDE.md` | tento návod | nikam, jen čtení |
| `1 Do Instructions/runtime-kernel.md` | krátká pravidla Kompasu | pole **Instructions** v Projectu |
| `2 Do Project knowledge/AI-pracovni-kompas.md` | metodika a šablony | **Project knowledge** |
| `2 Do Project knowledge/product-truth.yaml` | co Claude umí a neumí | **Project knowledge** |
| `balicek.yaml` | popis balíčku (verze, soubory) | nikam |

Názvy složek ti řeknou, kam který soubor patří.

## Instalace (5 minut)

1. Na claude.ai vlevo **Projects → New project**, název „AI pracovní kompas“.
2. V Projectu otevři **Instructions** a vlož **celý obsah** souboru `runtime-kernel.md`. Ulož.
3. **Project knowledge → + → Add text content**, a to dvakrát:
   - Title `AI-pracovni-kompas.md`, Content = celý obsah souboru,
   - Title `product-truth.yaml`, Content = celý obsah souboru.

   Použij „Add text content“, ne „Upload from device“. Text se pak dá upravit.
4. Otevři v Projectu nový chat a napiš: **Začínáme**

> **Nejčastější chyba:** `runtime-kernel.md` skončí jako soubor v knowledge místo v poli **Instructions**. Kompas pak nefunguje jako průvodce.

## Jak ho používat

1. Kdykoli máš nový pracovní problém, otevři Project **AI pracovní kompas** a popiš ho vlastními slovy.
2. Kompas navrhne, kde má práce bydlet (Chat, nebo Project), a dá ti **handoff**: název, instrukce k vložení, první zprávu a kritéria hotovo.
3. Podle handoffu si založ skutečný pracovní chat nebo Project. Práce pak pokračuje **tam**, ne v Kompasu.
4. Na konci ti Kompas nabídne blok **`compass_checkpoint_v1`**. Ulož si ho. Až se ke Kompasu vrátíš, vlož ho jako první zprávu.

## Kdy Kompas nestačí

Když Kompas doporučí **Project** a práce bude trvat týdny, má fáze a rozhodnutí (výzkum, implementace, příprava školení), handoff **nezakládej**. Pokračuj balíčkem **Projektový start** (složka „Balíček – Projektový start“): v novém chatu vlož `01-PRIPRAVA-ZADANI.md` a pod něj Kompasův handoff.

Opakovaná práce se stejnými pravidly (např. měsíční report) Projektový start nepotřebuje. Stačí Kompasův handoff.

## Víc informací

Prezentace s návodem a cvičeními je v balíčku Projektový start: `Prezentace/Projektovy-start-workshop.html`. Otevři ji v prohlížeči a ovládej šipkami. Části 1 a 2 se týkají Kompasu.
