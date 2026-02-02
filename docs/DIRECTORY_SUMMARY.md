# FWI Deck Directory Summary

This directory contains all assets for the **Frictionless Workforce Initiative (FWI)** presentation deck for Walker SCM's 2026 AI strategy.

---

## 📁 Directory Structure

```
fwi-deck/
├── FWI-Deck-2026.pdf               # Final exported PDF of the presentation
├── frictionless-workforce-initiative.md  # Core FWI concept document
├── fwi-presentation-combined.html  # Combined HTML version of all slides
├── slides/                         # Individual HTML slides (52 slides)
│   ├── 01-title.html through 52-demo-intro.html
│   ├── archived-slides/            # Deprecated/removed slides
│   ├── slide-styles.css            # Master stylesheet for all slides
│   ├── index.html                  # Slide navigation/preview page
│   └── print-all-slides.html       # Print-ready combined view
├── pdf/                            # PDF exports and review documents
│   ├── fwi-presentation-combined-all-pages.pdf
│   ├── SLIDE_REVIEW_30-SLIDE-CUT.md   # Review doc for 30-slide version
│   └── SLIDE_REVIEW_30-SLIDE-CUT.docx
├── scripts/
│   └── build-deck.sh               # Shell script to combine slides into HTML
├── slides-backup-20251213/         # Backup of slides from Dec 13, 2025
└── png/                            # PNG exports of slides
```

---

## 📄 Key Files

| File | Description |
|------|-------------|
| `FWI-Deck-2026.pdf` | Final 5.2MB PDF version of the deck |
| `frictionless-workforce-initiative.md` | Core philosophy document defining what FWI is and the Three Pillars framework |
| `fwi-presentation-combined.html` | Single HTML file with all slides for web viewing |
| `slides/slide-styles.css` | Master CSS with Walker SCM branding and slide layouts |
| `scripts/build-deck.sh` | Build script that combines individual slides into a single HTML file |

---

## 🎯 Presentation Overview

The FWI deck presents Walker SCM's AI workforce strategy built on **Three Pillars**:

1. **AI Literacy + Psychological Safety** — Training cohorts from Cabinet to org-wide
2. **Workflow Mapping + Friction Removal** — Identifying and automating friction points
3. **Org-wide AI Pilots + Integration** — Department-specific AI solutions

---

## 📊 Slide Structure (52 slides total)

| Section | Slides | Description |
|---------|--------|-------------|
| Opening | 1-3 | Title, Agenda, Objectives |
| Context | 4-9 | Why AI Now, Hype vs Reality, Culture-First |
| FWI Definition | 10-16 | What is FWI, Paradigm Shift, Core Philosophy |
| Three Pillars | 17-43 | Training Cohorts, Agentic Solutions, Vendor Integration |
| Measurement | 44-47 | Success Metrics, Proof Points |
| Closing | 48-52 | Roadmap, Next Steps, Demo |

> **Note:** A 30-slide cut version is documented in `pdf/SLIDE_REVIEW_30-SLIDE-CUT.md`

---

## 🛠️ Build Process

To regenerate the combined HTML:
```bash
cd slides
bash ../scripts/build-deck.sh
```

This produces `fwi-deck-combined.html` containing all slides in a single printable document.

---

## 📅 Last Updated
December 2025
