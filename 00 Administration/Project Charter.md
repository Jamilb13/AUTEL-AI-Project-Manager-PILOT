---
document: Project Charter.md
version: 0.1
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - [[README]]
  - [[PROJECT_CONTEXT]]
  - [[CHATGPT_ROLE]]
  - [[Task List]]
  - [[Kaizen Backlog]]
  - [[Folder Map]]
tags:
  - charter
  - governance
  - foundation
---

# Project Charter

## 1. Základní informace

- **Název projektu:** AUTEL AI Project Manager – PILOT
- **Slogan:** Každý projekt si zaslouží vlastní mozek.
- **Product Owner:** Kamil Běhálek
- **Aktuální fáze:** Foundation
- **Stav dokumentu:** DRAFT

## 2. Účel projektu

Projekt vzniká za účelem vytvoření podnikového znalostního systému pro společnost AUTEL, a.s. Ten nahradí roztříštěné toky informací a vytvoří jednotné, strukturované znalostní prostředí. Slouží k efektivnější správě a vyhledávání informací jak pro lidi, tak pro systémy umělé inteligence.

## 3. Cíl projektu

Cílem projektu je vybudovat a pilotně ověřit digitálního asistenta (Project Brain), který bude integrovat projektové a firemní znalosti s nástroji jako Microsoft 365 Copilot, SharePoint, OneDrive a Obsidian. Asistent má projektovým manažerům a projektantům zjednodušit vyhledávání standardů, postupů a správu dokumentace bez rizika neautorizovaných změn.

## 4. Kontext a výchozí stav

Projekt se aktuálně nachází na svém počátku ve fázi **Foundation** (architektura, pravidla, základní dokumentace). Pilotní řešení bude nejprve nasazeno a ověřeno v osobním prostředí Product Ownera. Širší firemní nasazení je uvažováno až jako následný krok po plném ověření a vyhodnocení výsledků tohoto pilotu.

## 5. Rozsah pilotu

### V rozsahu
- Tvorba základní projektové dokumentace (Foundation).
- Návrh architektury řešení.
- Znalostní systém s využitím Obsidianu jako znalostní vrstvy.
- Struktura a správa obsahu v [[01 AUTEL Knowledge Hub]].
- Struktura a správa obsahu v [[02 Expert Domains]].
- Příprava a správa AI postupů v [[03 AI Assets/AI Playbooks]].
- Příprava a konfigurace pilotního prostředí.

### Mimo rozsah
- Produkční firemní nasazení řešení.
- Vývoj vlastní softwarové aplikace na míru.
- Automatické a nekontrolované provádění změn v projektové dokumentaci bez výslovného schválení uživatelem.
- Jakékoliv integrace a automatizační skripty, které nebyly předem schváleny Product Ownerem.

## 6. Hlavní principy

- **Metoda Kaizen:** Postupný vývoj po malých, stabilních a dokončených krocích, kde každé zlepšení přináší okamžitou praktickou hodnotu.
- **Jednoduchost:** Preferujeme jednoduchá a přímočará řešení před složitými systémy (princip „Lepší horší plán teď než skvělý pozdě“).
- **Rozšiřitelnost:** Struktura a pravidla jsou navrženy tak, aby umožnily plynulý rozvoj a integraci budoucích AI agentů.
- **Respektování architektonických rozhodnutí (ADR):** Všechna schválená architektonická pravidla jsou pro vývoj závazná.
- **Řízení rozsahu:** Rozsah a priority určuje výhradně Product Owner.
- **Bezpečnost dokumentace:** AI nikdy nesmí měnit dokumentaci ani zdrojové soubory bez potvrzení uživatelem.

## 7. Klíčové výstupy fáze Foundation

- Schválený [[Project Charter]].
- Základní projektová dokumentace (např. [[PROJECT_CONTEXT]], [[CHATGPT_ROLE]], [[Folder Map]], [[README]]).
- Definovaná informační architektura.
- Připravená pilotní složková struktura na disku.
- Základní pravidla spolupráce člověka a AI.

## 8. Role a odpovědnosti

### Product Owner
- **Jméno:** Kamil Běhálek
- **Odpovědnost:** Rozhoduje o prioritách úkolů, rozsahu projektu, schvaluje architekturu, změny v dokumentech a rozhoduje o přechodu do dalších fází projektu.

### ChatGPT
- **Role:** Enterprise Solution Architect.
- **Odpovědnost:** Pomáhá navrhovat architekturu, udržovat konzistenci dokumentace, připravovat finální verze dokumentů, upozorňovat na architektonická rizika a navrhovat jednoduchá řešení. ChatGPT není rozhodovací autorita.

### Antigravity
- **Role:** Technická role pro správu souborů a verzování.
- **Odpovědnost:** Zodpovídá za provádění schválených změn v lokální pracovní kopii repozitáře, kontrolu lokálního diffu, provádění lokálních commitů a následný push do vzdáleného repozitáře. Antigravity není rozhodovací autorita.

## 9. Omezení a předpoklady

- **Místo provozu:** Pilot probíhá výhradně v osobním prostředí Product Ownera.
- **Využívané nástroje:** Projekt využívá stávající dostupné nástroje (M365 Copilot, SharePoint, OneDrive, Obsidian, ChatGPT).
- **Změny rozsahu:** Rozsah a priority nelze rozšiřovat bez výslovného souhlasu Product Ownera.
- **Rozpočet:** TBD – rozhodne Product Owner
- **Termíny milníků:** TBD – rozhodne Product Owner
- **Ostatní členové týmu:** TBD – rozhodne Product Owner
- **Kvantitativní KPI:** TBD – rozhodne Product Owner

## 10. Rizika

| Riziko | Dopad | Opatření k minimalizaci |
| :--- | :--- | :--- |
| Nekontrolované rozšiřování rozsahu projektu | Vysoký | Všechny nové nápady a požadavky zapisovat do [[Kaizen Backlog]], o zařazení do realizace rozhoduje výhradně PO. |
| Nekonzistence projektové dokumentace | Střední | AI asistent provádí pravidelnou kontrolu a sjednocení struktury a metadat. |
| Neověřená kvalita a chyby v AI výstupech | Vysoký | Každý výstup vygenerovaný AI podléhá lidské kontrole a explicitnímu schválení PO před commitováním. |
| Práce s citlivými firemními informacemi | Vysoký | Striktní dodržování bezpečnostních pravidel a provoz pouze v chráněném osobním/firemním prostředí (viz [[AI Policies]]). |
| Příliš komplexní řešení bez praktického užitku | Střední | Důsledné dodržování principů jednoduchosti a metody Kaizen. |

## 11. Kritéria úspěchu pilotu

- Projektová dokumentace je konzistentní a sjednocená.
- Potřebné informace lze ve struktuře snadno a rychle vyhledat.
- AI asistenti plně respektují schválená pravidla a role.
- Systém reálně pomáhá projektovým manažerům při každodenní práci s informacemi.
- Product Owner vyhodnotí pilot jako přínosný a rozhodne o pokračování vývoje.

## 12. Schválení

| Role | Jméno | Stav | Datum |
| :--- | :--- | :--- | :--- |
| Product Owner | Kamil Běhálek | Ke schválení | TBD |

## 13. Související dokumenty

- [[README]]
- [[PROJECT_CONTEXT]]
- [[CHATGPT_ROLE]]
- [[Task List]]
- [[Kaizen Backlog]]
- [[Folder Map]]
