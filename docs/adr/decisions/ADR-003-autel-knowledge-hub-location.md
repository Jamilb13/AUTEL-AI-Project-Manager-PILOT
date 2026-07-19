---
document: docs/adr/decisions/ADR-003-autel-knowledge-hub-location.md
version: 0.1
status: Accepted
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - [[docs/adr/README]]
  - [[docs/adr/ADR-INDEX]]
  - [[docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace]]
  - [[docs/adr/decisions/ADR-002-project-brain-location]]
tags:
  - adr
  - location
  - knowledge-hub
---

# ADR-003: AUTEL Knowledge Hub Location

## Základní informace

- **Stav:** Accepted
- **Datum:** 2026-07-19
- **Autor:** Kamil Běhálek

---

## Kontext
Řešení v rámci projektu rozlišuje mezi dvěma hlavními typy znalostí:
1. **Projektově specifické znalosti:** Patří výhradně k jednotlivým konkrétním projektům.
2. **Celofiremní sdílené znalosti:** Musí existovat nezávisle na jednotlivých projektech a být znovupoužitelné napříč celou organizací.

Sdílené firemní standardy, postupy a know-how nesmí být roztříštěny ani duplikovány uvnitř jednotlivých projektových složek.

---

## Rozhodnutí
- **AUTEL Knowledge Hub** slouží jako centrální a zastřešující úložiště pro celofiremní znalosti.
- Je fyzicky i logicky oddělen od složek jednotlivých projektů.
- **Project Brain** v jednotlivých projektech ukládá výhradně informace specifické pro danou zakázku.
- Všechny sdílené standardy, metodiky, unifikované šablony a opakovaně použitelné know-how patří výhradně do AUTEL Knowledge Hubu.
- AI asistenti a Copilot mohou využívat oba tyto zdroje informací současně, avšak každý z nich plní odlišný účel.

---

## Důsledky

### Pozitivní dopady
- **Jasné oddělení odpovědnosti (Separation of Concerns):** Snazší pochopení a správa toho, co je lokální (projektové) a co globální (firemní).
- **Efektivní znovupoužitelnost:** Jedna verze pravdy pro firemní standardy dostupná pro všechny projekty.
- **Snížení duplicit:** Znalosti se neudržují na mnoha místech současně, což snižuje riziko neaktuálnosti.
- **Snazší údržba:** Celofiremní pravidla lze aktualizovat na jednom centrálním místě.

### Negativní dopady
- **Nutnost správy (Governance):** Vyžaduje aktivní správu a schvalování obsahu v AUTEL Knowledge Hubu, aby nedošlo k jeho znečištění.
- **Proces povyšování znalostí:** Užitečné postupy nalezené v konkrétních projektech musí být občas explicitně vyčištěny a přeneseny (povýšeny) do Knowledge Hubu.

---

## Zvažované alternativy

- **Ukládání všeho uvnitř každého projektu:** Zamítnuto. Způsobovalo by masivní duplicity dokumentace a extrémně ztěžovalo aktualizaci firemních standardů.
- **Ukládání všeho pouze v AUTEL Knowledge Hubu:** Zamítnuto. Projekty by ztratily autonomii a nebylo by možné ukládat specifické detaily, které platí pouze pro konkrétní zakázku.
- **Použití SharePoint knihoven bez logického rozdělení:** Zamítnuto. Způsobovalo by zmatek v oprávněních, navigaci a ztěžovalo by AI agentům určení kontextu dokumentů.

---

## Související ADR

- [[docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace|ADR-001]] – Obsidian as the Primary Knowledge Workspace.
- [[docs/adr/decisions/ADR-002-project-brain-location|ADR-002]] – Project Brain Location.
