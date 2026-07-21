---
document: docs/standards/README.md
version: "0.1"
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-21
related:
  - "[[README]]"
  - "[[docs/architecture/ARCHITECTURE-ROADMAP]]"
  - "[[00 Administration/Project Charter]]"
  - "[[00 Administration/PROJECT_CONTEXT]]"
  - "[[00 Administration/CHATGPT_ROLE]]"
  - "[[docs/knowledge-hub/README]]"
  - "[[docs/adr/README]]"
tags:
  - documentation
  - standards
  - foundation
  - index
---

# Documentation Standards Foundation

## 1. Účel
Standardy dokumentace definují jednotná pravidla pro tvorbu, správu a revizi projektové dokumentace napříč celým repozitářem. Stanovují unifikované konvence pro metadata, strukturální pokyny a kvalitativní očekávání s cílem zajistit dlouhodobou udržitelnost, čitelnost a strojové zpracování.

## 2. Rozsah

### Zahrnuto
- Formátování a struktura Markdown dokumentů
- Pravidla pro YAML frontmatter metadata a kanonické pořadí polí
- Konzistence metadat napříč všemi dokumenty repozitáře
- Kompatibilita s Obsidian Properties a syntaxí wiki-odkazů
- Standardy a konvence pro dokumentaci generovanou AI
- Standardy pro dokumentaci psanou lidmi

### Vyloučeno
- Obsah technické projektové dokumentace a oborové inženýrské standardy
- Číslovací systémy inženýrských dokumentů AUTEL
- Formátování zdrojového kódu a pravidla stylu programovacích jazyků
- Automatizované validační skripty nebo konfigurace sestavovacích pipelines

## 3. Vztah k Foundation
Standardy dokumentace představují klíčový balíček fáze Foundation. Slouží jako základní standard používaný všemi budoucími architektonickými dokumenty, zápisy v Knowledge Hubu, zásadami governance a projektovými specifikacemi. Každý nový dokument vytvořený v repozitáři musí odpovídat standardům definovaným v tomto balíčku.

## 4. Vztah k ADR
- **ADR (Architecture Decision Records):** Dokumentují konkrétní architektonická a technická rozhodnutí, jejich kontext, alternativy a důsledky.
- **Standardy dokumentace:** Definují obecné formátování dokumentů, strukturální pokyny a pravidla pro metadata všech Markdown souborů.
- **Princip:** Standardy dokumentace podporují ADR zajištěním konzistentních metadat, ale nesmí nahrazovat ani měnit architektonická rozhodnutí.

## 5. Vztah k Knowledge Hub
Dokumenty v AUTEL Knowledge Hubu musí striktně dodržovat Standardy dokumentace pro YAML frontmatter, formátování a kompatibilitu s Obsidianem. Nicméně správa obsahu Knowledge Hubu (vlastnictví, proces review, životní cyklus a pravidla povyšování) zůstává definována v rámci [[docs/knowledge-hub/README|Knowledge Hub Foundation]].

## 6. Klíčové dokumenty
- [[docs/standards/DOCUMENT-METADATA-STANDARD|Document Metadata Standard]] – Kanonická pravidla pro YAML frontmatter a metadata
- [[docs/architecture/ARCHITECTURE-ROADMAP|Architecture Roadmap]] – Centrální navigační mapa a stav implementace
- [[00 Administration/Project Charter|Project Charter]] – Rozsah projektu, cíle a governance
- [[00 Administration/PROJECT_CONTEXT|Project Context]] – Celkový kontext projektu a rozhodnutí
- [[00 Administration/CHATGPT_ROLE|ChatGPT Role]] – Definice role pro AI architekturu řešení
- [[docs/knowledge-hub/README|Knowledge Hub Foundation]] – Základ celofiremního úložiště znalostí
- [[docs/adr/README|ADR Foundation]] – Rámec pro záznamy architektonických rozhodnutí
