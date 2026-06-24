# Workbook Architecture (v3.0)

RR-framework v3.0 uses a 43-sheet architecture:

| Layer | Purpose |
|---|---|
| Visible workflow | User-facing profile, questions, assessment, scenario and roadmap outputs. |
| `_DATA_*` | Normalized data and dashboard facts. |
| `_ENGINE_*` | Scoring, risk, crisis, strategy, initiative, relevance, simulation and Monte Carlo logic. |
| `_CONFIG_*` | Model settings and risk calibration. |
| `_REF_*` | Dropdowns, aliases, dictionaries, taxonomies, mappings and backend reference tables. |
| `_API_*` | Backend import contract. |
| `_README`, `_DOC`, `_LINT` | Internal documentation and audit layer. |

## Visible workflow sheets

1. Guidelines
2. Company Profile
3. Assessment Questions
4. AS-IS Assessment
5. Resilience & Risk Scenario
6. Action Plan & Roadmap

## Current scale

| Metric | Value |
|---|---:|
| Sheets | 43 |
| Visible sheets | 6 |
| Hidden sheets | 37 |
| Formulas | 90,275 |
| Named ranges | 121 |
| Data validations | 51 |
| Charts | 6 |



---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
