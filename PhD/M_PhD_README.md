# My PhD — Nhat-Le Vo

> *This folder structure is adapted from the PhD Folder Structure template by
> Yasmin Demerdash [![ORCID](https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png)](https://orcid.org/0000-0002-3246-7604),
> Jeanne Wilbrandt [![ORCID](https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png)](https://orcid.org/0000-0002-0363-3837), and
> Ron Dockhorn [![ORCID](https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png)](https://orcid.org/0000-0002-5268-5430).
> Original repository: [github.com/RDMJeanne/FolderStructure](https://github.com/RDMJeanne/FolderStructure).
> Customised for geoscience / numerical modeling.*

---

## About This PhD

| Field | Detail |
|---|---|
| **Researcher** | Nhat-Le Vo |
| **Project title** | Deconstructing Arctic Hydrothermal Systems: A Numerical Modeling Approach |
| **Institution** | MARUM – Center for Marine Environmental Sciences & Faculty of Geosciences, University of Bremen |
| **Cluster** | Excellence Cluster "The Ocean Floor – Earth's Uncharted Interface" |
| **Field sites** | Loki's Castle (LC), Jøtul (JT), Aurora (AU) |
| **Core methods** | Rift2Ridge geodynamic modeling, thermodynamic modeling, photogrammetry, mass spectrometry |
| **ORCID** | *[add your ORCID here]* |
| **Start date** | *[add start date]* |
| **Expected defense** | *[add expected date]* |

---

## Folder Overview

```
PhD/
├── 01_Documents/       Administrative, notes, literature, courses, funding
├── 02_Projects/        Observational data by site + paper-scoped analysis
├── 03_Code/            All scripts, model runs, notebooks — top-level, shared
├── 04_Presentations/   Conference talks, group meetings, posters
├── 05_Publications/    Paper drafts, figures, submissions
└── 06_Thesis/          Chapter-by-chapter thesis writing
```

This structure follows a **dual-axis** design for `02_Projects`:
- `02_Sites/` holds observational truth — raw data is never duplicated.
- `03_PaperProjects/` holds analysis scoped to a specific paper's argument.
- `03_Code/` lives at the top level because Rift2Ridge and thermodynamic scripts
  are reused across all three sites; burying code per-project would cause duplication.

---

## Key Contacts

| Role | Name | Email |
|---|---|---|
| PhD candidate | Nhat-Le Vo | *[add]* |
| Primary supervisor | *[add]* | *[add]* |
| Secondary supervisor | *[add]* | *[add]* |
| MARUM contact | *[add]* | *[add]* |

---

## README Convention

| Prefix | Meaning | Written by |
|---|---|---|
| `G_` | **Guidance** — explains what belongs in a folder, best practices, links | Original template authors (cited above) |
| `M_` | **Metadata** — documents *my actual project*, choices, names, dates | Me (Nhat-Le Vo) |

**Always keep `M_` files up to date.** They are living documents, not one-time forms.

---

*Last updated: 2026-05-28*
