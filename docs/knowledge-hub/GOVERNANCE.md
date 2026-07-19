---
document: docs/knowledge-hub/GOVERNANCE.md
version: 0.1
status: DRAFT
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - "[[docs/knowledge-hub/README]]"
tags:
  - knowledge-hub
  - governance
---

# Zásady správy (Governance) Knowledge Hubu

Tento dokument definuje základní pravidla správy, údržby a kvality obsahu v AUTEL Knowledge Hubu.

---

## 1. Vlastnictví (Ownership)
- **Celkový garant:** Znalostní bázi jako celek vlastní a spravuje Product Owner (Kamil Běhálek).
- **Garant oblasti (Owner):** Každý dokument v Knowledge Hubu musí mít v YAML hlavičce jasně definovaného vlastníka (Owner), který zodpovídá za jeho věcnou správnost a aktuálnost.
- **Příspěvky:** Kdokoliv z týmu může navrhnout úpravu nebo vytvoření nového dokumentu, ale schválení podléhá PO.

## 2. Proces revize (Review Process)
- Změny a nové dokumenty jsou nejprve vytvářeny ve stavu `DRAFT`.
- Každý dokument ve stavu `DRAFT` musí projít lidskou kontrolou a revizí (Review), kterou provádí vlastník dokumentu nebo určený odborný garant.
- Během review se kontroluje věcná správnost, srozumitelnost, struktura metadat a přítomnost křížových odkazů.

## 3. Schvalovací proces (Approval Process)
- Konečné schválení a povýšení dokumentu do stavu `APPROVED` (nebo `Published`) provádí výhradně Product Owner.
- Žádný dokument nesmí být považován za závazný firemní standard, pokud jeho status v YAML front matter není změněn na `APPROVED` (nebo `Published`).

## 4. Principy verzování (Versioning Principles)
- Dokumenty v Knowledge Hubu používají jednoduché verzování (např. `0.1` pro první rozpracovaný draft, `1.0` pro první schválené vydání).
- Při každé změně obsahu se:
  - Zvyšuje verze o minoritní (např. `1.0` -> `1.1` pro drobné úpravy) nebo majoritní krok (`1.0` -> `2.0` pro zásadní přepracování).
  - Aktualizuje datum `last_update` v YAML hlavičce.
  - Zaznamenává stručný popis změny do historie verzí (pokud je pro danou oblast zavedena).
