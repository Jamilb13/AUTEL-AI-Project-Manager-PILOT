---
document: docs/standards/README.md
version: 0.1
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

## 1. Purpose
Documentation Standards define consistent rules for creating, maintaining, and reviewing project documentation across the repository. They establish unified metadata conventions, structural guidelines, and quality expectations to ensure long-term maintainability, readability, and machine-processability.

## 2. Scope

### Included
- Markdown document formatting and structure
- YAML frontmatter metadata rules and canonical field ordering
- Metadata consistency across all repository documents
- Obsidian Properties compatibility and wikilink syntax
- AI-generated documentation standards and conventions
- Human-authored documentation standards

### Excluded
- Technical project documentation content and engineering domain standards
- AUTEL engineering document numbering systems
- Source code formatting and programming language style guides
- Automated validation scripts or build pipeline configurations

## 3. Relationship to Foundation
Documentation Standards are a core Foundation work package. They serve as the baseline standard used by all future architecture documents, knowledge hub entries, governance policies, and project specifications. Every new document created in the repository must adhere to the standards defined in this package.

## 4. Relationship to ADR
- **ADR (Architecture Decision Records):** Document specific architectural and technical decisions, their context, alternatives, and consequences.
- **Documentation Standards:** Define general document formatting, structural guidelines, and metadata rules for all Markdown files.
- **Principle:** Documentation Standards support ADRs by ensuring they have consistent metadata, but Documentation Standards must not replace or override architectural decisions.

## 5. Relationship to Knowledge Hub
Documents in the AUTEL Knowledge Hub must strictly follow the Documentation Standards for YAML frontmatter, formatting, and Obsidian compatibility. However, the governance of Knowledge Hub content (ownership, review workflow, lifecycle, and promotion rules) remains defined within the [[docs/knowledge-hub/README|Knowledge Hub Foundation]].

## 6. Key Documents
- [[docs/standards/DOCUMENT-METADATA-STANDARD|Document Metadata Standard]] – Canonical rules for YAML frontmatter and metadata
- [[docs/architecture/ARCHITECTURE-ROADMAP|Architecture Roadmap]] – Central navigation map and implementation status
- [[00 Administration/Project Charter|Project Charter]] – Project scope, objectives, and governance
- [[00 Administration/PROJECT_CONTEXT|Project Context]] – Overall project background and decisions
- [[00 Administration/CHATGPT_ROLE|ChatGPT Role]] – Role definition for AI solution architecture
- [[docs/knowledge-hub/README|Knowledge Hub Foundation]] – Central knowledge repository foundation
- [[docs/adr/README|ADR Foundation]] – Architecture decision records framework
