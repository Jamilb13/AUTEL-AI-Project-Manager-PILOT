---
document: docs/adr/decisions/ADR-002-project-brain-location.md
version: 0.1
status: Accepted
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - [[docs/adr/README]]
  - [[docs/adr/ADR-INDEX]]
  - [[docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace]]
tags:
  - adr
  - location
  - project-brain
---

# ADR-002: Project Brain Location

## Základní informace

- **Stav:** Accepted
- **Datum:** 2026-07-19
- **Autor:** Kamil Běhálek

---

## Kontext
Projekt vyžaduje konzistentní a předvídatelné umístění pro veškeré specifické znalosti umělé inteligence a související dokumentaci v rámci jednotlivých projektů. Společnost AUTEL již definuje standardní skupinu dokumentů **P90 – Vedení projektu (Project Management)**, což z ní činí vhodné umístění pro tyto potřeby bez nutnosti zavádění paralelních složkových struktur.

---

## Rozhodnutí
- Každý projekt obsahuje právě jeden **Project Brain**.
- Project Brain bude uložen v adresáři spojeném s oblastí **P90 – Vedení projektu** (Project Management) daného projektu.
- Project Brain obsahuje výhradně znalosti a specifikace související s umělou inteligencí.
- Standardní technická projektová dokumentace zůstává uložena v běžných dokumentových skupinách společnosti AUTEL.
- Toto umístění a struktura jsou identické pro každý projekt.

---

## Důsledky

### Pozitivní dopady
- **Standardizované umístění:** Všichni členové týmu i AI asistenti vědí, kde přesně Project Brain hledat.
- **Snazší automatizace:** Jednotná cesta zjednodušuje automatické skenování a indexaci obsahu AI agenty.
- **Předvídatelná navigace:** Rychlá orientace v projektu a konzistentní složková struktura napříč všemi zakázkami.

### Negativní dopady
- **Zatížení oblasti P90:** Složka P90 se stává ústředním místem i pro AI dokumentaci.
- **Nutnost pochopení rozdílu:** Členové týmu musí jasně rozumět rozdílu mezi standardní technickou dokumentací projektu a specifickým AI obsahem v Project Brain.

---

## Zvažované alternativy

- **Ukládání Project Brain v kořenu projektu:** Zamítnuto z důvodu zbytečného znečišťování kořenové složky projektu pomocnými a konfiguračními AI soubory.
- **Ukládání Project Brain pouze v SharePointu:** Zamítnuto. Neumožňuje čisté lokální verzování a ztěžuje přístup pro offline nástroje typu Obsidian.
- **Ukládání Project Brain mimo jednotlivé projekty:** Zamítnuto. Znesnadňuje to přenositelnost a zálohování projektu jako celku (složka projektu by nebyla kompletní a soběstačná).

---

## Související ADR

- [[docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace|ADR-001]] – Obsidian as the Primary Knowledge Workspace.
