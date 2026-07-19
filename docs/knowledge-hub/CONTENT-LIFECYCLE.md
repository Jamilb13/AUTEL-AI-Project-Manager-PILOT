---
document: docs/knowledge-hub/CONTENT-LIFECYCLE.md
version: 0.1
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - "[[docs/knowledge-hub/README]]"
tags:
  - knowledge-hub
  - lifecycle
---

# Životní cyklus obsahu a povyšování znalostí

Tento dokument definuje stavy, kterými prochází dokumentace v Knowledge Hubu, a pravidla pro přesun lokálních znalostí z projektů do celofiremního úložiště.

---

## 1. Stavy životního cyklu obsahu

Dokumenty v znalostním systému procházejí následujícími fázemi:

```text
  Draft  ──>  Review  ──>  Approved  ──>  Published  ──>  Archived
```

- **Draft (Rozpracováno):** Dokument je ve fázi tvorby. Může obsahovat neúplné informace a zástupné znaky (TBD). Není závazný.
- **Review (K posouzení):** Dokument je dokončen a čeká na věcné a formální ověření garantem.
- **Approved (Schváleno):** Dokument byl schválen Product Ownerem jako správný a udržitelný, ale ještě nebyl oficiálně vypuštěn do plného firemního užívání.
- **Published (Publikováno):** Dokument je oficiálně uvolněn a je závazný pro všechny relevantní pracovníky a projekty.
- **Archived (Archivováno):** Dokument je zastaralý nebo nahrazený. Je přesunut do složky `99 Archive` pro historické účely, ale nesmí se již aktivně používat.

---

## 2. Pravidla pro povyšování znalostí (Promotion Rules)

Užitečné postupy a znalosti často vznikají přímo při realizaci konkrétních projektů v lokálním Project Brainu. Aby se staly celofiremní hodnotou, procházejí procesem povýšení (promotion):

```text
  Project Brain (Lokální)  ──>  Výběr a očištění  ──>  Review  ──>  Knowledge Hub (Globální)
```

### Postup povýšení:
1. **Identifikace:** Projektový manažer nebo AI asistent identifikuje v lokálním Project Brainu přínosný postup, checklist nebo řešení problému, které by mohlo pomoci i ostatním projektům.
2. **Očištění (Sanitization):** Z dokumentu musí být kompletně odstraněny všechny specifické údaje o daném projektu (jména zákazníků, konkrétní ceny, interní označení apod.) a nahrazeny obecnými šablonami či popisem.
3. **Předložení:** Očištěný dokument je vložen do příslušné složky v Knowledge Hubu ve stavu `Draft`.
4. **Schválení:** Prochází standardním procesem review a schválení (viz [[docs/knowledge-hub/GOVERNANCE|Governance]]), a po schválení se stává součástí celofiremní databáze.
