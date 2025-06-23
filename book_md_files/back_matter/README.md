# Godot Engine – Kommandoreferenz von A bis Z

> **Projektziel:** Eine praxisnahe Referenz für Godot‑Entwickler\:innen (Command‑Line & Workflow) – als Website, PDF und EPUB.

---

## 1 │ Schnellstart

```bash
# Virtuelle Umgebung anlegen
python -m venv .venv && source .venv/bin/activate

# Abhängigkeiten installieren
pip install mkdocs-material pymdown-extensions

# Live‑Server starten
mkdocs serve      # öffnet http://127.0.0.1:8000

# Statisches Build erzeugen
mkdocs build      # Ausgabe liegt in site/
```

---

## 2 │ Vollständige Ordnerstruktur

```
book_md_files/
├── index.md                       # Home‑Seite
├── images/                        # globale Grafiken
│   └── …
├── innere_vorderteile/            # Front Matter
│   ├── schmutztitel.md
│   ├── titelseite.md
│   ├── impressum.md
│   ├── vorwort.md
│   ├── inhaltsverzeichnis.md
│   └── images/                    # Cover‑PNG (front, spine, back)
│       ├── cover_front.png
│       ├── cover_book_spine.png
│       └── cover_back.png
├── hauptteil/
│   ├── einleitung.md
│   └── referenzen/
│       ├── ueberblick.md
│       ├── dateien_verwalten.md
│       ├── godot_engine_ide.md
│       └── kontrollstrukturen/
│           ├── kontrollstrukturen.md
│           ├── bedingte_anweisungen.md
│           ├── schleifen.md
│           └── verzweigungen.md
├── anhaenge/
│   ├── anhang_a.md
│   ├── anhang_b.md
│   ├── glossar.md
│   └── bibliographie.md
├── back_matter/
│   ├── epilog.md
│   └── register.md
├── mkdocs.yml                     # Site‑Konfiguration
└── README.md                      # dieses Dokument
```

---

## 3 │ Markdown‑Konventionen

| Element       | Regel                                                    |
| ------------- | -------------------------------------------------------- |
| Dateinamen    | **kleinbuchstaben**, Unterstriche, keine Umlaute         |
| Überschriften | H1 für Kapitel, max. H3 in Fließtext                     |
| Bilder        | `![alt](path){ width="80%" }` (Attr‑List)                |
| Grid Layout   | `::: columns … :::` (pymdownx.grid) – responsive Spalten |

---

## 4 │ Offene Aufgaben

* [ ] Kapitelinhalte vervollständigen (Platzhalter füllen)
* [ ] Cover‑Feinschliff (Logo, Auflage, Farbverlauf)
* [ ] Klappentext finalisieren
* [ ] Glossar & Register automatisieren (makeindex / plugin)
* [ ] CI‑Workflow (GitHub Actions) für Build & Deploy
* [ ] PDF/EPUB‑Export (mkdocs‑material → print‑theme)

---

## 5 │ Besprochene Notizen

* **Attr‑List** und **pymdownx.grid** sind in `mkdocs.yml` aktiviert → responsive Spalten & Skalierung.
* Bildgrößen direkt per `{ width="…" height="…" }` oder CSS‑Klasse `.spine-img`.
* Drei Cover nebeneinander → Grid‑Snippet:

```markdown

::: columns
::: column
![Front](images/cover_front.png){ width="100%" }
::: column
![Spine](images/cover_book_spine.png){ width="100%" }
::: column
![Back](images/cover_back.png){ width="100%" }
:::
:::

```

* **book spine** = engl. Begriff für „Buchrücken“.
* **TOC** = *Table of Contents* (Inhaltsverzeichnis).

---

## 6 │ Lizenz

*(Platzhalter – z. B. CC BY‑SA für Text, MIT für Code)*
