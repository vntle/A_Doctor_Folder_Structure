# 02_Projects — Nhat-Le Vo

## Dual-Axis Design

This folder uses **Option C**: two separate concerns kept clean.

| Sub-folder | Axis | Rule |
|---|---|---|
| `02_Sites/` | Field site | Raw/processed observations live here. **Never duplicated.** |
| `03_PaperProjects/` | Paper | Analysis, figures, scripts scoped to one paper's argument |

Paper projects **reference** site data via relative paths — they never copy raw files.

## Structure

```
02_Projects/
├── 00_Protocols/            # Method-level, shared across all sites
│   ├── Rift2Ridge/
│   ├── Thermodynamics/
│   ├── Photogrammetry/
│   └── MassSpectrometry/
├── 01_Collaborations/
├── 02_Sites/
│   ├── LokisCastle/  (abbreviation: LC)
│   │   ├── 01_Observations/
│   │   │   ├── 01_Raw/       # Never edit raw files
│   │   │   ├── 02_Processed/
│   │   │   └── 03_Metadata/  # Provenance, instrument logs, cruise info
│   │   ├── 02_Modeling/
│   │   │   ├── Rift2Ridge/
│   │   │   └── Thermodynamics/
│   │   └── 03_Results/
│   ├── Jotul/        (abbreviation: JT)
│   └── Aurora/       (abbreviation: AU)
└── 03_PaperProjects/
    ├── P1_LokisCastle_FluidChem/
    ├── P2_FaultControl_Jotul/
    └── P3_Arctic_Comparative/
```

## Site Abbreviations
| Site | Abbreviation | Use in filenames |
|---|---|---|
| Loki’s Castle | `LC` | `YYYYMMDD_LC_descriptor_v01` |
| Jøtul | `JT` | `YYYYMMDD_JT_descriptor_v01` |
| Aurora | `AU` | `YYYYMMDD_AU_descriptor_v01` |
