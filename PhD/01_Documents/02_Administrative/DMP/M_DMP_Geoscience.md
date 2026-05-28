# Data Management Plan — Nhat-Le Vo
**Project:** Deconstructing Arctic Hydrothermal Systems: A Numerical Modeling Approach  
**Institution:** MARUM – Center for Marine Environmental Sciences & Faculty of Geosciences, University of Bremen  
**Cluster:** Excellence Cluster "The Ocean Floor – Earth's Uncharted Interface"  
**Last updated:** 2026-05-28  

---

## 1. Project Overview

| Field | Detail |
|---|---|
| **Researcher** | Nhat-Le Vo |
| **Supervisor(s)** | TBD – update here |
| **Duration** | TBD (typical: 3–4 years) |
| **Field sites** | Loki's Castle (LC), Jøtul (JT), Aurora (AU) — Arctic Mid-Ocean Ridges |
| **Core methods** | Rift2Ridge geodynamic modeling, thermodynamic modeling, photogrammetry, mass spectrometry |
| **Funding** | Excellence Cluster "The Ocean Floor" (DFG) |

---

## 2. Data Types and Sources

| Data type | Format(s) | Source | Volume (est.) | Folder |
|---|---|---|---|---|
| Vent fluid chemistry (observational) | `.csv`, `.xlsx` | Published datasets / cruise archives | ~100 MB | `02_Sites/[SITE]/01_Observations/01_Raw/` |
| Temperature–depth profiles | `.csv`, `.nc` | CTD casts, published | ~50 MB | `02_Sites/[SITE]/01_Observations/01_Raw/` |
| Bathymetry / structural maps | `.grd`, `.nc`, `.tif` | Cruise data, GEBCO | ~500 MB | `02_Sites/[SITE]/01_Observations/01_Raw/` |
| Photogrammetry outputs | `.obj`, `.ply`, `.tif` | Own acquisition | ~2–10 GB | `02_Sites/[SITE]/01_Observations/02_Processed/` |
| Mass spectrometry data | `.csv`, proprietary | Own acquisition | ~500 MB | `02_Sites/[SITE]/01_Observations/02_Processed/` |
| Rift2Ridge model inputs | `.json`, `.cfg`, `.toml` | Self-generated | ~50 MB | `03_Code/01_Rift2Ridge/configs/` |
| Rift2Ridge model outputs | `.nc`, `.csv`, binary | Self-generated | ~5–50 GB | `03_Code/01_Rift2Ridge/runs/` |
| Thermodynamic model I/O | `.inp`, `.out`, `.csv` | Self-generated | ~1 GB | `03_Code/02_Thermodynamics/` |
| Analysis scripts | `.py`, `.sh`, `.ipynb` | Self-written | ~100 MB | `03_Code/` |
| Processed figures | `.pdf`, `.png`, `.svg` | Self-generated | ~500 MB | `02_Sites/[SITE]/03_Results/Figures/` |

---

## 3. FAIR Principles — How This Project Implements Them

### Findable
- All datasets assigned persistent identifiers (DOI) upon publication via PANGAEA or Zenodo
- Metadata files (`03_Metadata/`) document instrument type, cruise ID, collection date, operators
- This folder structure itself is version-controlled on GitHub

### Accessible
- Raw observational data stored on MARUM/UniBremen institutional servers (backed up)
- Published datasets deposited in **PANGAEA** (marine geoscience standard repository)
- Model code published on **GitHub** + archived on **Zenodo** at time of publication

### Interoperable
- Preferred formats: `.csv`, `.nc` (NetCDF), `.pdf` — all open, widely used in geoscience
- Proprietary formats (mass spec, photogrammetry) exported to open equivalents before archiving
- Metadata follows CF Conventions (NetCDF) and PANGAEA metadata schema

### Reusable
- All datasets published with **CC BY 4.0** license
- All code published with **MIT** or **GPL-3.0** license
- READMEs in every folder describe contents, units, coordinate systems
- Naming convention documented in `M_NamingSchemes_Geoscience.md`

---

## 4. Storage and Backup

| Copy | Location | Sync frequency |
|---|---|---|
| **Working copy** | Local laptop | Continuous |
| **Backup 1** | MARUM / UniBremen server (institutional) | Daily (automated) |
| **Backup 2** | External SSD (encrypted) | Weekly |
| **Archive** | PANGAEA / Zenodo | At publication |

**Rule:** 3-2-1 backup strategy (3 copies, 2 different media, 1 off-site).  
**Raw data is never edited in place** — always work on `02_Processed/` copies.

---

## 5. File Naming and Versioning

See `PhD/M_NamingSchemes_Geoscience.md` for the full convention. Summary:

- Dates: `YYYYMMDD` (ISO 8601)
- Site tags: `LC`, `JT`, `AU`
- Versions: `_v01`, `_v02` — never overwrite, never delete
- Superseded runs: append `_ARCHIVE` (do not delete)
- Model run pattern: `YYYYMMDD_R2R_[SITE]_v##`

---

## 6. Sensitive and Restricted Data

| Data type | Sensitivity | Handling |
|---|---|---|
| Raw cruise data (pre-publication) | Embargo possible | Store locally + institutional server; do not share until PI approval |
| Collaboration partner data | May be restricted | Check agreement in `02_Projects/01_Collaborations/` before sharing |
| Personal data | None expected | This project does not involve human subjects |

---

## 7. Data Sharing and Publication

| Output type | Target repository | Timing |
|---|---|---|
| Observational datasets | [PANGAEA](https://www.pangaea.de/) | At or before paper submission |
| Model code (Rift2Ridge configs + scripts) | GitHub + [Zenodo](https://zenodo.org/) | At paper submission |
| Thermodynamic model I/O | Zenodo (supplementary) | At paper submission |
| Thesis datasets | UniBremen institutional repository | At thesis submission |

**PANGAEA** is the primary repository — it is the international standard for marine and geoscience data and is endorsed by the Excellence Cluster.

---

## 8. Responsibilities

| Task | Responsible |
|---|---|
| Daily data management | Nhat-Le Vo |
| DMP review & update | Nhat-Le Vo + supervisor (each 6 months) |
| Final data deposition | Nhat-Le Vo (before thesis defense) |
| Code archiving | Nhat-Le Vo (at each paper submission) |

---

## 9. Applicable Policies and Resources

- **DFG Guidelines on the Handling of Research Data:** https://www.dfg.de/en/research_funding/principles_dfg_funding/research_data/
- **DFG Checklist (Research Data):** https://www.dfg.de/resource/blob/174736/92691e48e89bf4ac88c8eb91b8f783b0/forschungsdaten-checkliste-en-data.pdf
- **Excellence Cluster RDM policy:** store in `01_Documents/02_Administrative/ExcellenceCluster/`
- **PANGAEA submission guide:** https://www.pangaea.de/submit/
- **Turing Way (Reproducible Research):** https://book.the-turing-way.org/
- **DMPonline tool:** https://dmponline.dcc.ac.uk/

---

## 10. Version History of this DMP

| Date | Version | Change |
|---|---|---|
| 2026-05-28 | v01 | Initial draft |
| | v02 | |
