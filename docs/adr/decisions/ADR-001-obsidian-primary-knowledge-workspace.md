---
document: docs/adr/decisions/ADR-001-obsidian-primary-knowledge-workspace.md
version: 0.1
status: APPROVED
owner: Kamil Běhálek
last_update: 2026-07-19
related:
  - [[docs/adr/README]]
  - [[docs/adr/ADR-INDEX]]
tags:
  - adr
  - obsidian
  - workspace
---

# ADR-001: Obsidian as the Primary Knowledge Workspace

## Základní informace

- **Stav:** Accepted
- **Datum:** 2026-07-19
- **Autor:** Kamil Běhálek / ChatGPT

---

## Kontext
Projekt **AUTEL AI Project Manager – PILOT** vyžaduje robustní znalostní prostředí pro ukládání, propojování a správu projektové dokumentace. Toto prostředí musí splňovat následující klíčové požadavky:
- Vhodné pro efektivní správu a psaní projektové dokumentace.
- Podpora pro obousměrné odkazy (backlinks) a snadné propojování myšlenek.
- Použití otevřeného a standardizovaného formátu Markdown.
- Lokální přístup k souborům (local-first approach) bez závislosti na stálém internetovém připojení.
- Dlouhodobá udržitelnost a nezávislost na konkrétním proprietárním poskytovateli (vendor lock-in).
- Snadná integrace se systémem správy verzí Git.

---

## Rozhodnutí
- **Obsidian** je vybrán jako primární znalostní prostředí (Primary Knowledge Workspace) pro lidské uživatele.
- **GitHub** slouží výhradně jako synchronizační a integrační vrstva (např. pro předávání stavu mezi ChatGPT, Antigravity a dalšími agenty).
- AI asistenti a vývojářské nástroje pracují přímo nad soubory v lokálním Git repozitáři, avšak primárním autorským a čtecím prostředím pro člověka zůstává Obsidian.

---

## Důsledky

### Pozitivní dopady
- **Standardizace:** Veškerá dokumentace je v prostém textu (Markdown), což zaručuje její snadnou čitelnost a přenositelnost.
- **Propojenost:** Využití obousměrných odkazů vytváří srozumitelnou síť souvislostí (znalostní graf).
- **Rychlost:** Lokální přístup (local-first) zajišťuje okamžitou odezvu bez čekání na cloudové API.
- **Verzování:** Markdown soubory lze snadno verzovat v Gitu a provádět nad nimi čisté diffy.

### Negativní dopady
- **Nutnost instalace:** Uživatelé potřebují mít lokálně nainstalovaného klienta Obsidian.
- **Synchronizace:** Změny je nutné ručně commitovat a pushovat, pokud není synchronizace plně automatizována.
- **Kooperace v reálném čase:** Obsidian standardně nepodporuje simultánní úpravy více uživateli najednou (real-time co-authoring) bez dalších doplňků.

---

## Zvažované alternativy

- **SharePoint (pouze):** Zamítnuto z důvodu chybějící nativní podpory obousměrných odkazů, horší práce s Markdownem a složitějšího lokálního zpracování pro AI agenty.
- **GitHub (pouze):** Zamítnuto. Přestože je vhodný pro AI a verzování, postrádá komfortní desktopové rozhraní pro vizualizaci vztahů a grafů pro lidské editory.
- **Plain Markdown bez Obsidianu:** Zamítnuto. Samotný Markdown neposkytuje komfortní funkce pro automatické doplňování odkazů, správu šablon a grafické zobrazení vazeb.

---

## Související ADR

- Žádné.
