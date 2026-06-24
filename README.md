# RR-framework

**RR-framework** is an open, Excel-based business resilience and digital maturity assessment workbook created by **Roman Reznikov**.

It helps organizations assess process maturity, digitalization, and resilience across business functions, then translate the assessment into crisis exposure, risk themes, strategy packages, prioritized initiatives, and roadmap waves.

Current version: **v3.0**  
Build ID: **RR-FRAMEWORK-v3.0-20260624**  
Release date: **2026-06-24**  
Author ORCID: **https://orcid.org/0000-0001-5581-5651**  
DOI: **10.5281/zenodo.20583866**  
Concept DOI: **10.5281/zenodo.20583865**  
License: **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International**  
SPDX License ID: **CC-BY-NC-SA-4.0**  
Copyright: **Copyright (C) 2026 Roman Reznikov**

## What's new in v3.0

v3.0 is a stable public release based on the calibrated v2.9.46 workbook. It rounds the late 2.9.x calibration/safety branch into a cleaner release line and synchronizes workbook metadata, release documentation, DOI/ORCID attribution, and package structure.

### Main changes

- Consolidated the v2.9.46 **calibration safety fixes** into public version **v3.0**.
- Updated workbook version metadata in visible guidance, hidden config/docs, LINT, core properties, and custom document properties.
- Added DOI, Concept DOI, ORCID, copyright, license, attribution, and commercial-use metadata to the workbook.
- Added a visible attribution/citation block to **Guidelines** and matching metadata blocks to hidden `_README` and `_DOC`.
- Preserved the current 43-sheet model architecture, formula graph, charts, validations, named ranges, and no-macro `.xlsx` format.
- Added a new GitHub/Zenodo-style document package with release notes, changelog, citation file, methodology, architecture, scoring logic, roadmap, data dictionary, admin guide, and release audit.

## Workbook metrics

| Metric | Value |
|---|---:|
| Workbook sheets | 43 |
| Visible sheets | 6 |
| Hidden sheets | 37 |
| XML cell records | 173,829 |
| Formulas | 90,275 |
| Named ranges | 121 |
| Data validations | 51 |
| Conditional formatting blocks | 37 |
| Charts | 6 |
| Formula error tokens in XML | 0 |
| Excel error cells in XML | 0 |
| External links | 0 |
| Macros / VBA | 0 |

## Model content summary

| Content area | Count |
|---|---:|
| Assessment questions | 424 |
| Business domains | 17 |
| Subdomains | 76 |
| Risk-library rows | 424 |
| Score-specific risk statements | 2,544 |
| Score-specific treatment statements | 2,544 |
| Initiatives | 72 |
| Strategies | 14 |
| Crisis scenarios | 12 |
| Crisis × domain multiplier rows | 204 |
| Industry templates | 10 |
| Industry aliases | 42 |
| Capability taxonomy items | 37 |
| Capability bridge rows | 98 |
| Risk → initiative mapping rows | 424 |
| Backend data dictionary fields | 310 |
| Monte Carlo iterations | 2,000 |

## Repository package

- `workbook/RR-framework_v3.0.xlsx` — public workbook.
- `README.md` — overview and release summary.
- `RELEASE_NOTES_v3.0.md` — release details.
- `CHANGELOG.md` — version history.
- `CITATION.cff` — machine-readable citation metadata.
- `LICENSE.md`, `NOTICE.md`, `DISCLAIMER.md`, `AUTHORS.md` — legal and attribution documents.
- `docs/` — user, methodology, scoring, architecture, data dictionary and admin documentation.
- `releases/checksums.txt` — SHA-256 checksums for release artifacts.

## Recommended use

1. Open the workbook in Microsoft Excel desktop.
2. Start on **Guidelines**.
3. Fill **Company Profile**.
4. Complete **Assessment Questions**.
5. Select crisis scenario and severity in **Resilience & Risk Scenario**.
6. Review **AS-IS Assessment** and **Action Plan & Roadmap**.
7. Recalculate before formal export: Excel → Formulas → Calculation Options → Automatic, then `Ctrl+Alt+F9`, save.

## License and commercial-use note

RR-framework is licensed under **CC BY-NC-SA 4.0**. Non-commercial use, review, adaptation, and sharing are allowed under the license terms and attribution requirements. Commercial delivery, resale, white-labeling, or integration into commercial products requires separate written permission from Roman Reznikov.



---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
