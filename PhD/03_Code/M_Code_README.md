# 03_Code — Nhat-Le Vo

All scripts, model configurations, and notebooks live here.
Code is **site-agnostic** at the top level — site-specific runs are versioned inside subfolders.

## Structure

```
03_Code/
├── 01_Rift2Ridge/
│   ├── configs/       # Parameter files (.json, .cfg, .toml)
│   ├── scripts/       # Core model scripts (version-controlled)
│   └── runs/          # One subfolder per simulation run
│       └── TEMPLATE_YYYYMMDD_site_v00/   # Copy this for each new run
├── 02_Thermodynamics/
│   ├── scripts/
│   ├── inputs/
│   └── outputs/
├── 03_DataProcessing/
│   ├── geochemistry/
│   ├── temperature/
│   └── bathymetry/
├── 04_Visualization/  # Plotting scripts, style files
├── 05_Utils/          # Shared helper functions, converters
└── 06_Notebooks/      # Jupyter/Quarto notebooks (exploratory)
```

## Model Run Naming Convention

All Rift2Ridge runs go in `01_Rift2Ridge/runs/` with this pattern:

```
YYYYMMDD_R2R_[SITE]_v##
```

Examples:
- `20260528_R2R_LC_v01`  ← Loki’s Castle, first run
- `20260601_R2R_JT_v03`  ← Jøtul, third iteration
- `20260715_R2R_AU_v01`  ← Aurora

**Never delete old runs.** Append `_ARCHIVE` to superseded ones.

## Why Code is Top-Level

Rift2Ridge scripts and thermodynamic pipelines are reused across
all three sites. Burying code inside each project folder would cause
duplication and make version control painful.
