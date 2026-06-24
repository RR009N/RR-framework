# Changelog

All notable changes to RR-framework are documented in this file.

## [3.0] - 2026-06-24

### Changed

- Rounded the late v2.9.46 calibration safety branch into stable public release **v3.0**.
- Synchronized workbook version metadata across visible guidance, hidden config/docs, LINT, core properties, and custom document properties.
- Updated build ID to `RR-FRAMEWORK-v3.0-20260624`.
- Updated package documentation for GitHub/Zenodo-style release distribution.

### Added

- ORCID attribution: `https://orcid.org/0000-0001-5581-5651`.
- DOI metadata: `10.5281/zenodo.20583866`.
- Concept DOI metadata: `10.5281/zenodo.20583865`.
- Visible workbook citation block on `Guidelines`.
- Hidden release metadata blocks on `_README` and `_DOC`.
- New `RELEASE_NOTES_v3.0.md`.
- New `docs/RELEASE_AUDIT_v3.0.md`.

### Preserved

- 43 sheets, including 6 visible workflow sheets and 37 hidden backend/model sheets.
- 424 assessment questions, 72 initiatives, 14 strategies, 12 crisis scenarios.
- 90,275 formulas, 121 named ranges, 51 data validations, 37 conditional formatting blocks, 6 charts.
- No external links and no VBA/macros.

### Verified

- Formula error-token scan in workbook XML: 0.
- Excel error cells in workbook XML: 0.
- Custom properties include version, build ID, DOI, Concept DOI, ORCID, copyright, author, license, and commercial-use rule.

## [2.0] - 2026-06-19

### Changed

- Major architecture refactor and integrity-hardening release.
- Layered workbook structure introduced with visible workflow, hidden data/config/reference, and protected engine layers.
- Calibration moved toward a single source of truth.
- Structured release documentation package introduced.

## [1.67] - 2026-06-16

### Changed

- Navigation, workbook structure, release polish, visible guidance, and workbook integrity updates.

## [1.0] - 2026-06-07

### Added

- Initial public package baseline for RR-framework workbook and documentation.



---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
