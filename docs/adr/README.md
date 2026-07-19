---
document: docs/adr/README.md
version: 0.1
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - [[README]]
  - [[Folder Map]]
tags:
  - adr
  - index
  - architecture
---

# ADR (Architecture Decision Records) – Úvod

## Účel ADR
Architecture Decision Records (ADR) slouží k dokumentování klíčových technických a architektonických rozhodnutí v projektu. Umožňuje sledovat kontext rozhodnutí, zvolené varianty a jejich důsledky v průběhu času.

## Kdy se ADR vytváří
ADR se zakládá vždy, když:
- Dochází k zásadní změně architektury systému.
- Je vybrána nová technologie nebo framework.
- Se definuje klíčový standard (např. struktura dat, komunikační protokol, bezpečnostní politika).
- Je potřeba vyřešit technický problém s více možnými alternativami.

## Životní cyklus ADR
ADR prochází následujícími stavy:
1. **Proposed (Navrženo):** Rozhodnutí je navrženo k diskusi a posouzení.
2. **Accepted (Přijato):** Rozhodnutí bylo schváleno Product Ownerem a je platné.
3. **Superseded (Nahrazeno):** Rozhodnutí bylo nahrazeno novějším ADR (přidá se odkaz na nové ADR).
4. **Deprecated (Zastaralé):** Rozhodnutí již není platné a nebylo nahrazeno žádným novým rozhodnutím.

## Číslovací konvence
ADR jsou číslována vzestupně v třímístném formátu:
- `ADR-001`, `ADR-002`, `ADR-003` atd.
- Soubory jsou ukládány do složky `docs/adr/decisions/` pod názvem `ADR-xxx-nazev-rozhodnuti.md`.

---

## Související dokumenty
- [[docs/adr/ADR-INDEX]] – Seznam všech architektonických rozhodnutí.
- [[docs/adr/ADR-TEMPLATE]] – Šablona pro zakládání nových ADR.
- [[Folder Map]] – Mapa složek projektu.
