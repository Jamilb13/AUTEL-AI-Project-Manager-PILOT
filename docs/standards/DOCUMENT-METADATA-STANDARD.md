---
document: docs/standards/DOCUMENT-METADATA-STANDARD.md
version: "0.1"
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-21
related:
  - "[[docs/standards/README]]"
  - "[[docs/architecture/ARCHITECTURE-ROADMAP]]"
  - "[[00 Administration/PROJECT_CONTEXT]]"
  - "[[docs/knowledge-hub/README]]"
  - "[[docs/adr/README]]"
tags:
  - documentation
  - metadata
  - standards
  - foundation
---

# Document Metadata Standard

## 1. Účel
Tento standard formalizuje kanonický formát YAML frontmatteru pro všechny Markdown dokumenty v repozitáři. Zajistí, že metadata budou konzistentní, strojově čitelná, přívětivá pro lidské uživatele a plně kompatibilní s Obsidian Properties.

## 2. Filosofie metadat
Schéma metadat se řídí následujícími principy:
- **Jednoduchost (Simple):** Minimální mentální zátěž pro autory a správce.
- **Lidská čitelnost (Human-readable):** Jasné, transparentní dvojice klíč-hodnota formátované v běžném textu.
- **Strojová čitelnost (Machine-readable):** Deterministická struktura snadno zpracovatelná AI agenty a skripty.
- **Kompatibilita s Obsidianem (Obsidian-compatible):** Navrženo pro bezproblémové vykreslování v Obsidian Properties bez chyb při zpracování.
- **Konzistence (Consistent):** Jednotné pojmenování polí, pořadí a formáty hodnot napříč všemi soubory.
- **Minimalismus (Minimal):** Standardizuje pouze nezbytná pole již používaná v repozitáři bez zbytečného balastu.
- **Rozšiřitelnost pouze schváleným rozhodnutím:** Nové klíče metadat vyžadují výslovné schválení.

## 3. Povinná pole
Následujících sedm polí je povinných ve všech YAML frontmatterech v repozitáři:
- `document`
- `version`
- `status`
- `owner`
- `last_update`
- `related`
- `tags`

## 4. Volitelná pole
V současnosti nejsou standardizována žádná další volitelná pole metadat. Všechny dokumenty musí používat pouze sedm standardizovaných povinných polí.

## 5. Kanonické pořadí polí
Každý YAML frontmatter Markdown dokumentu musí uvádět klíče přesně v tomto pořadí:

```yaml
document: <path>
version: "<version>"
status: <status>
owner: <owner>
last_update: <date>
related:
  - "<wikilink>"
tags:
  - <tag>
```

## 6. Datové typy
- **document:** `string` – Cesta k Markdown souboru relativně k repozitáři (např. `docs/standards/DOCUMENT-METADATA-STANDARD.md`).
- **version:** `string` – Sémantická verze dokumentu, např. `"0.1"` nebo `"1.0"`. Hodnoty verze musí být uzavřeny v uvozovkách, aby se zabránilo YAML parserům v jejich interpretaci jako číselných hodnot.
- **status:** `string` – Hodnota životního cyklu odpovídající specifickému kontextu dokumentu.
- **owner:** `string` – Odpovědný lidský vlastník (např. `Kamil Běhálek`).
- **last_update:** `date` – Datum ve formátu `YYYY-MM-DD`.
- **related:** `list of strings` – YAML seznam uvozovaných řetězců Obsidian wiki-odkazů (např. `"[[README]]"`).
- **tags:** `list of strings` – YAML seznam jednotlivých hodnot textu psaných malými písmeny.

## 7. Hodnoty stavu (Status Values)
Hodnoty stavu jsou kategorizovány podle jejich konkrétního kontextu životního cyklu a nesmí se míchat:

### Obecné dokumenty Foundation
- `DRAFT` – Dokument je ve fázi aktivní tvorby nebo revize.
- `APPROVED` – Dokument byl formálně schválen Product Ownerem.

### Záznamy architektonických rozhodnutí (ADR)
- `Proposed` – Architektonické rozhodnutí předložené k přezkoumání.
- `Accepted` – Architektonické rozhodnutí schválené a aktivní.
- `Superseded` – Rozhodnutí nahrazené novějším ADR.
- `Deprecated` – Rozhodnutí vyřazené bez náhrady.

### Stavy pracovních balíčků Architektonické roadmapy
- `Planned` – Pracovní balíček identifikován, ale dosud nezahájen.
- `In Progress` – Pracovní balíček je aktuálně aktivní.
- `Completed` – Pracovní balíček je dokončen.

### Životní cyklus obsahu v Knowledge Hubu
- `Draft` – Obsah v počátečním stavu návrhu.
- `Review` – Obsah prochází technickým/edičním review.
- `Approved` – Obsah schválen pro publikaci.
- `Published` – Obsah je živý a aktivní v Knowledge Hubu.
- `Archived` – Stažený nebo zastaralý obsah.

*Pravidlo:* Hodnoty stavu nesmí být míchány mezi jednotlivými kontexty životního cyklu bez schválené změny.

## 8. Verzování
- `0.x` se používá pro rozpracované a vyvíjející se dokumenty Foundation (např. `"0.1"`, `"0.2"`).
- `1.0` se používá pro první schválené stabilní vydání dokumentu (např. `"1.0"`).
- Hodnoty verze musí být uzavřeny v uvozovkách, aby se zabránilo YAML parserům v jejich interpretaci jako číselných hodnot.
- **Minoritní navýšení (Minor increment):** Používá se pro kompatibilní změny obsahu (např. `"1.0"` -> `"1.1"`).
- **Majoritní navýšení (Major increment):** Používá se pro zásadní restrukturalizaci nebo breaking changes (např. `"1.0"` -> `"2.0"`).
- Změny verze aktualizují metadata, ale nenahrazují historii v Gitu.
- Automatické změny verzí nejsou vynucovány.

## 9. Formát data
Všechna data musí používat kalendářní formát data podle ISO 8601:
`YYYY-MM-DD`

Lokální formáty data (např. `19.07.2026` nebo `07/19/2026`) jsou přísně zakázány.

## 10. Tagy
- Musí být formátovány jako YAML seznam.
- Jeden tag na položku seznamu.
- Všechny znaky musí být malá písmena.
- Víceslovné tagy musí být odděleny pomlčkami (`-`).
- Bez předpony `#` (např. použijte `foundation`, nikoli `#foundation`).
- Žádná vnořená pole ani samostatné řetězce oddělené čárkami.

Příklad:
```yaml
tags:
  - documentation
  - metadata
  - foundation
```

## 11. Související odkazy (Related Links)
Požadavky na kanonický formát pro pole `related`:

```yaml
related:
  - "[[README]]"
  - "[[docs/architecture/ARCHITECTURE-ROADMAP]]"
```

### Pravidla
- Každá položka musí být uvozovaný YAML řetězec (uzavřený v dvojitých uvozovkách `"..."`).
- Každá položka musí obsahovat přesně jeden Obsidian wiki-odkaz.
- Zobrazované aliasy wiki-odkazů jsou povoleny.

Příklad aliasu:
```yaml
related:
  - "[[docs/adr/ADR-INDEX|ADR Index]]"
```

### Zakázané příklady
```yaml
# Zakázáno: Neuvozované dvojité závorky (v YAML interpretováno jako vnořená pole)
related:
  - [[README]]

# Zakázáno: Samostatný řetězec spojený čárkami
related: "[[README]], [[docs/adr/README]]"

# Zakázáno: Explicitní vnořené pole
related:
  - [["README"]]
```

*Vysvětlení:* Neuvozované dvojité závorky `[[...]]` jsou standardním YAML parserem vyhodnoceny jako vnořená pole (flow sequences) (`[["README"]]`), což narušuje zpracování v Obsidian Properties a zobrazuje odkazy jako chybné řetězce polí.

## 12. Příklady (Examples)

### A. Minimální platný příklad
```yaml
---
document: 00 Administration/README.md
version: "0.1"
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-21
related:
  - "[[README]]"
tags:
  - administration
---
```

### B. Příklad pro ADR
```yaml
---
document: docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace.md
version: "0.1"
status: Accepted
owner: Kamil Běhálek
last_update: 2026-07-21
related:
  - "[[docs/adr/README]]"
  - "[[docs/adr/ADR-INDEX]]"
tags:
  - adr
  - obsidian
---
```

### C. Příklad pro dokument Foundation
```yaml
---
document: docs/standards/DOCUMENT-METADATA-STANDARD.md
version: "0.1"
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-21
related:
  - "[[docs/standards/README]]"
  - "[[docs/architecture/ARCHITECTURE-ROADMAP]]"
tags:
  - documentation
  - metadata
  - standards
  - foundation
---
```

### D. Neplatné příklady

```yaml
# Neplatný příklad 1: Chybějící uvozovky u wiki-odkazů
related:
  - [[README]]
# Vysvětlení: Interpretuje se jako vnořené pole [['README']], což narušuje Obsidian Properties.

# Neplatný příklad 2: Nesprávné pořadí polí
status: DRAFT
document: docs/standards/README.md
# Vysvětlení: Pole musí následovat v kanonickém pořadí (document, version, status, owner, last_update, related, tags).

# Neplatný příklad 3: Tag s předponou # a velkými písmeny
tags:
  - #Documentation
# Vysvětlení: Tagy musí být malými písmeny bez předpony #.

# Neplatný příklad 4: Neuvozované číslo verze
version: 0.1
# Vysvětlení: Neuvozovaná hodnota může být interpretována jako číslo místo řetězce.
```

## 13. Pravidla pro validaci (Validation Rules)
Kontrolní seznam pro ruční validaci autory a přezkoumávajícími:
1. Frontmatter začíná a končí přesně znaky `---`.
2. Neexistují žádné duplicitní klíče.
3. Kanonické pořadí polí je striktně dodrženo.
4. Formát data odpovídá `YYYY-MM-DD`.
5. `related` je YAML seznam uvozovaných řetězců wiki-odkazů v dvojitých uvozovkách.
6. `tags` je YAML seznam jednotlivých hodnot textu psaných malými písmeny.
7. Hodnota `status` patří do odpovídajícího kontextu životního cyklu.
8. Cesta `document` odpovídá umístění souboru relativně k repozitáři.
9. Odsazení YAML používá přesně dvě mezery na úroveň.
10. V YAML nejsou použity žádné tabulátory.

*Omezení:* V tomto pracovním balíčku nevytvářejte validační skripty ani automatizované nástroje pro kontrolu.

## 14. Budoucí rozšiřitelnost (Future Extensibility)
- Nová pole metadat vyžadují výslovný návrh a schválení Product Ownerem.
- Významné změny schématu metadat mohou vyžadovat samostatné ADR.
- Automatizované validační skripty nebo kontroly v CI pipeline mohou být zavedeny v samostatném budoucím pracovním balíčku.
- Zpětná kompatibilita ze stávajícími dokumenty v repozitáři by měla být zachována, kdekoliv je to praktické.
