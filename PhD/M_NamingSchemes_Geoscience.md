# Naming Schemes — Geoscience Edition

Adapted from the original `M_NamingSchemes.md` for a numerical modeling + observational geoscience PhD.

---

## General Rules

- **No spaces** — use underscores `_`
- **No special characters** — no parentheses, colons, umlauts
- **ISO 8601 dates** — always `YYYYMMDD` (compact) or `YYYY-MM-DD` (readable)
- **Leading zeros** for numbered sequences: `v01`, `v02` … `v99`
- **Lowercase preferred** for all folder names; mixed case only for proper site names

---

## Site Abbreviations

| Site | Abbreviation |
|---|---|
| Loki’s Castle | `LC` |
| Jøtul | `JT` |
| Aurora | `AU` |

---

## File Naming Patterns

### Observations / Field Data
```
YYYYMMDD_[SITE]_[instrument]_[descriptor]_v##.ext
```
Examples:
- `20240815_LC_CTD_profile_v01.csv`
- `20240820_AU_fluidchem_raw_v01.xlsx`

### Model Runs (Rift2Ridge)
```
YYYYMMDD_R2R_[SITE]_[descriptor]_v##
```
Examples:
- `20260528_R2R_LC_basalt_noSed_v01/`
- `20260601_R2R_JT_fault60deg_v02/`

### Thermodynamic Model Files
```
YYYYMMDD_TD_[SITE]_[fluidtype]_v##.ext
```
Example:
- `20260610_TD_LC_seawater_350C_v01.inp`

### Figures
```
[P#]_Fig##_[descriptor]_v##.ext
```
Examples:
- `P1_Fig03_LC_tempprofile_v02.pdf`
- `P3_Fig01_comparative_Tmax_v01.png`

### Supervision Meeting Notes
```
YYYY-MM-DD_Supervision_[topic].md
```
Example:
- `2026-05-28_Supervision_Jotul_modeling_update.md`

### Paper Drafts
```
YYYYMMDD_[P#]_[ShortTitle]_v##.docx
```
Example:
- `20260901_P1_LokisCastle_FluidChem_v03.docx`

---

## Archive Rule

Never delete superseded model runs or old data versions.  
Append `_ARCHIVE` to the folder/file name instead:
```
20260528_R2R_LC_v01_ARCHIVE/
20260601_R2R_LC_v02/          ← current
```

---

## Abbreviation Dictionary

| Abbreviation | Full term |
|---|---|
| `R2R` | Rift2Ridge (geodynamic model) |
| `TD` | Thermodynamic |
| `LC` | Loki’s Castle |
| `JT` | Jøtul |
| `AU` | Aurora |
| `CTD` | Conductivity-Temperature-Depth |
| `P1/P2/P3` | Paper 1 / Paper 2 / Paper 3 |
| `v##` | Version number |
