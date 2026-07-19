---
document: Folder Map.md
version: 0.2
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - [[README]]
  - [[PROJECT_CONTEXT]]
tags:
  - mapping
  - structure
  - guidance
---

# Folder Map

## Účel dokumentu
Tento dokument popisuje účel a obsah každé složky v projektu **AUTEL AI Project Manager – PILOT**. Pomáhá udržovat pořádek a jasně vymezuje, kam ukládat jednotlivé typy dokumentů.

## Kdy se používá
Při zakládání nového dokumentu, při reorganizaci a pro orientaci nových členů týmu (či AI asistence).

---

## Detailní popis složek

### `00 Administration`
Správní a organizační dokumenty celého projektu.
- **Co sem patří:** Projektové definice, plány, role, zápisy z porad, rozhodnutí a úkoly.
- **Co sem nepatří:** Technické specifikace, zdrojový kód, firemní standardy.
- **Příklady dokumentů:** [[README]], [[PROJECT_CONTEXT]], [[Task List]], [[Kaizen Backlog]].

### `01 AUTEL Knowledge Hub`
Centrální firemní znalostní databáze společnosti AUTEL.
- **Co sem patří:** Metodiky, standardy, osvědčené postupy, seznamy typických chyb a slovník pojmů.
- **Co sem nepatří:** Projektově specifické úkoly, AI prompty.
- **Příklady dokumentů:** Interní směrnice, ISO standardy, Lessons Learned.

### `02 Expert Domains`
Odborné znalosti rozdělené podle jednotlivých profesí a kompetenčních center.
- **Co sem patří:** Znalostní báze pro jednotlivé obory (Projektový management, MaR, Elektro...).
- **Co sem nepatří:** Obecné firemní směrnice, testovací scénáře.
- **Příklady dokumentů:** Specifika projektování v oboru elektro, checklisty pro FAT.

### `03 AI Assets`
Prostředky a konfigurace pro umělou inteligenci a Copilot.
- **Co sem patří:** AI příručky (Playbooks), instrukce pro Copilota, knihovna promptů, persony a šablony.
- **Co sem nepatří:** Obecné firemní metodiky, zápisy z porad.
- **Příklady dokumentů:** Copilot system instructions, Prompt library.

### `04 Shared Templates`
Šablony pro sdílení a opakované použití v rámci projektového řízení.
- **Co sem patří:** Prázdné šablony dokumentů, checklisty.
- **Co sem nepatří:** Vyplněné dokumenty konkrétního projektu.
- **Příklady dokumentů:** Šablona zápisu z jednání, šablona předávacího protokolu.

### `05 Workflows`
Pracovní postupy, procesy a diagramy popisující realizaci projektů.
- **Co sem patří:** Procesní diagramy, popisy workflow, integrace.
- **Co sem nepatří:** Zdroje a konfigurace AI.
- **Příklady dokumentů:** Postup schvalování dokumentace, BPMN diagram.

### `06 Architecture`
Architektonický návrh a specifikace pilotního i cílového řešení.
- **Co sem patří:** Architektonické vrstvy (Business, Information, Application, Technology) a diagramy.
- **Co sem nepatří:** Obecné firemní metodiky.
- **Příklady dokumentů:** Datový model, diagram komponent.

### `07 Testing`
Podklady pro testování a vyhodnocování pilotu.
- **Co sem patří:** Testovací scénáře, výsledky testů, hodnocení pilotu.
- **Co sem nepatří:** Kód, architektonické diagramy.
- **Příklady dokumentů:** Pilot test scenario, Evaluation report.

### `08 Sandbox`
Volný prostor pro bezpečné experimentování a vývoj.
- **Co sem patří:** Pracovní verze dokumentů, testovací výstupy z AI, poznámky.
- **Co sem nepatří:** Finální a schválené verze dokumentů.
- **Příklady dokumentů:** Návrhy promptů, testovací poznámky.

### `99 Archive`
Archiv starých, nahrazených nebo neaktivních verzí dokumentů.
- **Co sem patří:** Historické dokumenty, které mají být zachovány, ale nejsou aktivně používány.
- **Co sem nepatří:** Aktivní úkoly, aktuální standardy.
- **Příklady dokumentů:** Staré verze projektového charteru.

---

## Související dokumenty
- [[README]] – Hlavní rozcestník.
- [[PROJECT_CONTEXT]] – Kontext projektu a cíle.
