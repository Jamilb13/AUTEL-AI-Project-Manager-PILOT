---
document: docs/standards/DOCUMENT-METADATA-STANDARD.md
version: 0.1
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

## 1. Purpose
This standard formalizes the canonical YAML frontmatter format for all Markdown documents in the repository. It ensures that metadata is consistent, machine-readable, human-friendly, and fully compatible with Obsidian Properties.

## 2. Metadata Philosophy
The metadata schema adheres to the following principles:
- **Simple:** Minimal cognitive overhead for authors and maintainers.
- **Human-readable:** Clear, transparent key-value pairs formatted in standard text.
- **Machine-readable:** Deterministic structure easily parsed by AI agents and scripts.
- **Obsidian-compatible:** Designed to render seamlessly in Obsidian Properties without parsing errors.
- **Consistent:** Uniform field naming, order, and value formats across all files.
- **Minimal:** Standardizes only essential fields already used in the repository without unnecessary clutter.
- **Extensible only by approved decision:** New metadata keys require explicit approval.

## 3. Required Fields
The following seven fields are mandatory in all repository Markdown frontmatters:
- `document`
- `version`
- `status`
- `owner`
- `last_update`
- `related`
- `tags`

## 4. Optional Fields
No additional optional metadata fields are currently standardized. All documents must use only the seven standardized required fields.

## 5. Canonical Field Order
Every Markdown document YAML frontmatter must present keys in exactly this order:

```yaml
document: <path>
version: <version>
status: <status>
owner: <owner>
last_update: <date>
related:
  - "<wikilink>"
tags:
  - <tag>
```

## 6. Data Types
- **document:** `string` – Repository-relative Markdown file path (e.g. `docs/standards/DOCUMENT-METADATA-STANDARD.md`).
- **version:** `string` – Semantic document version such as `0.1` or `1.0`.
- **status:** `string` – Lifecycle value relevant to the specific document context.
- **owner:** `string` – Accountable human owner (e.g. `Kamil Běhálek`).
- **last_update:** `date` – Date in `YYYY-MM-DD` format.
- **related:** `list of strings` – YAML list of quoted Obsidian wikilink strings (e.g. `"[[README]]"`).
- **tags:** `list of strings` – YAML list of individual lowercase text values.

## 7. Status Values
Status values are categorized by their specific lifecycle context and must not be mixed:

### General Foundation Documents
- `DRAFT` – Document is under active creation or review.
- `APPROVED` – Document has been formally approved by Product Owner.

### ADR Documents
- `Proposed` – Architecture decision proposed for review.
- `Accepted` – Architecture decision approved and active.
- `Superseded` – Decision replaced by a newer ADR.
- `Deprecated` – Decision retired without replacement.

### Architecture Roadmap Work Package States
- `Planned` – Work package identified but not started.
- `In Progress` – Work package currently active.
- `Completed` – Work package finished.

### Knowledge Hub Content Lifecycle
- `Draft` – Content in initial draft state.
- `Review` – Content under technical/editorial review.
- `Approved` – Content approved for publication.
- `Published` – Content live and active in Knowledge Hub.
- `Archived` – Retracted or obsolete content.

*Rule:* Status values must not be mixed between lifecycle contexts without an approved change.

## 8. Versioning
- `0.x` is used for draft and evolving Foundation documents (e.g. `0.1`, `0.2`).
- `1.0` is used for the first approved stable release of a document.
- **Minor increment:** Used for compatible content changes (e.g. `1.0` -> `1.1`).
- **Major increment:** Used for significant restructuring or breaking changes (e.g. `1.0` -> `2.0`).
- Version changes update metadata but do not replace Git commit history.
- Automatic version changes are not imposed.

## 9. Date Format
All dates must use the ISO 8601 calendar date format:
`YYYY-MM-DD`

Locale-specific date formats (e.g. `19.07.2026` or `07/19/2026`) are strictly forbidden.

## 10. Tags
- Must be formatted as a YAML list.
- One tag per list item.
- All characters must be lowercase.
- Multiple words must be separated by hyphens (`-`).
- No `#` prefix (e.g. use `foundation`, not `#foundation`).
- No nested arrays or comma-separated single strings.

Example:
```yaml
tags:
  - documentation
  - metadata
  - foundation
```

## 11. Related Links
Canonical format requirements for the `related` field:

```yaml
related:
  - "[[README]]"
  - "[[docs/architecture/ARCHITECTURE-ROADMAP]]"
```

### Rules
- Every item must be a quoted YAML string (surrounded by double quotes `"..."`).
- Every item must contain exactly one Obsidian wikilink.
- Wikilink display aliases are permitted.

Alias Example:
```yaml
related:
  - "[[docs/adr/ADR-INDEX|ADR Index]]"
```

### Forbidden Examples
```yaml
# Forbidden: Unquoted double brackets (parsed as nested flow sequences in YAML)
related:
  - [[README]]

# Forbidden: Single concatenated string
related: "[[README]], [[docs/adr/README]]"

# Forbidden: Explicit nested array
related:
  - [["README"]]
```

*Explanation:* Unquoted double brackets `[[...]]` are parsed by standard YAML as nested flow sequences (`[["README"]]`), which breaks Obsidian Properties parsing and displays links as malformed array strings.

## 12. Examples

### A. Minimal Valid Example
```yaml
---
document: 00 Administration/README.md
version: 0.1
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-21
related:
  - "[[README]]"
tags:
  - administration
---
```

### B. ADR Example
```yaml
---
document: docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace.md
version: 0.1
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

### C. Foundation Document Example
```yaml
---
document: docs/standards/DOCUMENT-METADATA-STANDARD.md
version: 0.1
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

### D. Invalid Examples

```yaml
# Invalid Example 1: Missing quotes on wikilinks
related:
  - [[README]]
# Explanation: Parses as nested array [['README']], breaking Obsidian Properties.

# Invalid Example 2: Incorrect field order
status: DRAFT
document: docs/standards/README.md
# Explanation: Fields must follow canonical order (document, version, status, owner, last_update, related, tags).

# Invalid Example 3: Tag with # prefix and uppercase
tags:
  - #Documentation
# Explanation: Tags must be lowercase without # prefix.
```

## 13. Validation Rules
Manual validation checklist for authors and reviewers:
1. Frontmatter begins and ends with exactly `---`.
2. No duplicate keys exist.
3. Canonical field order is strictly maintained.
4. Date format matches `YYYY-MM-DD`.
5. `related` is a YAML list of double-quoted wikilink strings.
6. `tags` is a YAML list of individual lowercase text values.
7. `status` value belongs to the appropriate lifecycle context.
8. `document` path matches the file's repository-relative location.
9. YAML indentation uses exactly two spaces per level.
10. No tab characters are used in YAML.

*Constraint:* Do not create validation scripts or automated build checkers in this work package.

## 14. Future Extensibility
- New metadata fields require explicit proposal and Product Owner approval.
- Significant metadata schema changes may require a dedicated ADR.
- Automated validation scripts or CI pipeline checkers may be introduced in a separate future work package.
- Backward compatibility with existing repository documents must be preserved wherever practical.
