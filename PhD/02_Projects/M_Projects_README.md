# 02_Projects — Nhat-Le Vo

> *Structure adapted from the PhD Folder Structure template by Demerdash, Wilbrandt & Dockhorn.
> Original: [github.com/RDMJeanne/FolderStructure](https://github.com/RDMJeanne/FolderStructure)*

My research has two overlapping axes that don't map cleanly onto each other:
observations are tied to **field sites**, while analysis and writing are tied to **papers**.
This folder therefore uses a dual-axis design rather than the generic `ProjectX` template.

---

## Dual-Axis Design

| Sub-folder | Axis | Rule |
|---|---|---|
| `02_Sites/` | Field site | Observational truth. Raw data lives here and is **never duplicated**. |
| `03_PaperProjects/` | Paper | Analysis, figures, and model runs scoped to one paper's argument. |

Paper projects **reference** site data via relative paths — they never copy raw files.

---

## My Structure

```
02_Projects/
├── 00_Protocols/                   Method-level protocols, shared across all sites
│   ├── Rift2Ridge/
│   ├── Thermodynamics/
│   ├── Photogrammetry/
│   └── MassSpectrometry/
├── 01_Collaborations/              External partner data and joint work
├── 02_Sites/
│   ├── LokisCastle/   (abbrev: LC) Mohns/Knipovich Ridge, ~73°N
│   │   ├── 01_Observations/
│   │   │   ├── 01_Raw/             NEVER edit — immutable original files
│   │   │   ├── 02_Processed/       Working copies derived from raw
│   │   │   └── 03_Metadata/        Cruise IDs, instrument logs, provenance
│   │   ├── 02_Modeling/
│   │   │   ├── Rift2Ridge/         Site-specific model config references
│   │   │   └── Thermodynamics/
│   │   └── 03_Results/
│   │       ├── Figures/
│   │       ├── Tables/
│   │       └── Reports/
│   ├── Jotul/         (abbrev: JT) Arctic vent field
│   └── Aurora/        (abbrev: AU) Gakkel Ridge, ~85°N
└── 03_PaperProjects/
    ├── P1_LokisCastle_FluidChem/   Paper 1 — fluid chemistry controls at LC
    │   ├── Analysis/
    │   └── Figures/
    ├── P2_FaultControl_Jotul/      Paper 2 — fault structure controls at JT
    └── P3_Arctic_Comparative/      Paper 3 — comparative cross-site synthesis
```

---

## Site Abbreviations

| Site | Abbreviation | Geographic context |
|---|---|---|
| Loki's Castle | `LC` | Mohns/Knipovich Ridge, ~73°N |
| Jøtul | `JT` | Arctic vent field |
| Aurora | `AU` | Gakkel Ridge, ~85°N |

Use these abbreviations consistently in all file names:
`YYYYMMDD_[LC|JT|AU]_descriptor_v##.ext`

---

## Why "Observations" not "Experiments"

The original template uses `YYYY-MM-DD_ExperimentX` as its base unit, which reflects a
wet-lab life-science workflow. My work is **observational and numerical**: I do not design
controlled experiments. Data comes from oceanographic cruises and published archives.
The `01_Observations/` unit replaces `ExperimentX` for this reason.

---

## Cross-Reference Map

| Paper | Primary site data | Model runs | Thesis chapter |
|---|---|---|---|
| P1 | `02_Sites/LokisCastle/` | `03_Code/01_Rift2Ridge/runs/*LC*` | `06_Thesis/03_Chapter_LokisCastle/` |
| P2 | `02_Sites/Jotul/` | `03_Code/01_Rift2Ridge/runs/*JT*` | `06_Thesis/04_Chapter_Jotul/` |
| P3 | `02_Sites/*/` | `03_Code/03_DataProcessing/` | `06_Thesis/06_Chapter_Comparative/` |

---

*Last updated: 2026-05-28*
