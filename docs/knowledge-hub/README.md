---
document: docs/knowledge-hub/README.md
version: 0.1
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - "[[README]]"
  - "[[docs/architecture/ARCHITECTURE-ROADMAP]]"
  - "[[docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace]]"
  - "[[docs/adr/decisions/ADR-002-project-brain-location]]"
  - "[[docs/adr/decisions/ADR-003-autel-knowledge-hub-location]]"
tags:
  - knowledge-hub
  - foundation
  - index
---

# AUTEL Knowledge Hub – Úvod

## Účel Knowledge Hubu
AUTEL Knowledge Hub slouží jako centrální firemní znalostní báze společnosti AUTEL, a.s. Jeho cílem je sjednotit, bezpečně ukládat a zpřístupňovat celofiremní standardy, osvědčené postupy, šablony a odborné know-how jak pro lidské uživatele, tak pro systémy umělé inteligence (např. Microsoft 365 Copilot).

## Rozsah (Scope)
V rozsahu Knowledge Hubu je:
- Celofiremní technická a projektová metodika.
- Firemní standardy kvality a technické standardy.
- Databáze chyb (Lessons Learned) a osvědčených postupů (Best Practices).
- Glosář a slovník pojmů.
- AI Playbooky, knihovny promptů a instrukce pro Copiloty.
- Unifikované šablony dokumentů.

Mimo rozsah jsou specifická data a dokumenty konkrétních projektů.

## Vztah k Project Brain
Vztah je definován jasnou dělicí čarou mezi globálními a lokálními znalostmi:
- **AUTEL Knowledge Hub (globální):** Obsahuje obecně platné firemní standardy a znovupoužitelné šablony nezávislé na konkrétním projektu.
- **Project Brain (lokální):** Obsahuje data platná pouze pro daný konkrétní projekt. Informace se mohou z Project Brainu po ověření a vyčištění povýšit do globálního Knowledge Hubu.

## Křížové odkazy na klíčová rozhodnutí
Architektura a principy Knowledge Hubu přímo vycházejí z následujících architektonických rozhodnutí:
- [[docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace|ADR-001 Obsidian as the Primary Knowledge Workspace]]
- [[docs/adr/decisions/ADR-002-project-brain-location|ADR-002 Project Brain Location]]
- [[docs/adr/decisions/ADR-003-autel-knowledge-hub-location|ADR-003 AUTEL Knowledge Hub Location]]

---

## Související dokumenty
- [[docs/knowledge-hub/HUB-STRUCTURE]] – Logická struktura Knowledge Hubu.
- [[docs/knowledge-hub/GOVERNANCE]] – Pravidla správy a schvalování.
- [[docs/knowledge-hub/CONTENT-LIFECYCLE]] – Životní cyklus obsahu a povyšování znalostí.
