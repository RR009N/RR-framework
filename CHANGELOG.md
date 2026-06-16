# Changelog

All notable changes to RR-framework will be documented in this file.

The format is inspired by Keep a Changelog, and this project uses semantic versioning where practical.

Intermediate iterations 1.1 through 1.5 are documented in detail inside the workbook on the **Methodology & Governance** sheet (Version & Release History). They are summarized here under 1.67.

## [1.67] - 2026-06-16

### Added

- Navigation hub on the START HERE sheet: logically grouped, colour-coded, clickable index of every tab (visible, hidden, and protected) showing the workbook structure.
- Uniform header band on every visible sheet: title, purpose, a short "what you can / cannot edit" note, and a one-click link back to START HERE.
- Centralized calibration parameters (`cfg_*`) consolidated in `_TECH_Scoring_Settings` so tunable thresholds can be reviewed and recalibrated in one place.
- Named ranges (`qn_*`) on the normalized data layer for readability.

### Changed

- Strategy scoring formulas refactored from ~3,000-character manual expansions to compact `SUMPRODUCT` form (identical results, easier to audit).
- Data-quality diagnostics (Scoring & Diagnostics) rebuilt as `COUNTIFS`.
- Error handling tightened: 2,650 single-lookup guards converted from `IFERROR` to `IFNA`, so genuine `#REF!`/`#VALUE!` errors surface instead of being silently hidden.

### Fixed

- Crisis multiplier lookup corrected to read the numeric SPOF column (previously read a text column, breaking the entire WSJF risk ranking once real data was entered).
- WSJF and scenario-adjusted formulas guarded against blank job-size / missing reference rows (no more `#VALUE!` cascades).
- Diagnostics row-block ranges fixed (previously skipped 3+ domains due to stale references).
- Self-referencing "active scenario" / "severity" cells on Crisis & Resilience repointed to the live inputs.

### Verified

- Full recalculation audit on a blank template and three filled industry samples (SaaS, manufacturing, financial services); charts, data-validation dropdowns, and named ranges confirmed intact.

## [1.0] - 2026-06-07

### Added

- Initial public release of RR-framework.
- Excel workbook with company profile, domain assessment, crisis simulator, risk summary, strategy packages, recommendation engine, initiative roadmap, Gantt roadmap, heatmaps, and spider dashboards.
- Closed-answer Company Profile inputs.
- Industry template logic.
- Improved scoring model with confidence adjustment and normalized scores.
- Risk library and executive risk summary.
- Recommendation matrix and executive recommendations.
- Strategy package logic.
- Initiative library and roadmap.
- Crisis scenario logic and resilience stress testing.
- Standards mapping per question.
- Quality Control sheet.
- Workbook footer and metadata for attribution.
- License, notice, citation metadata, and GitHub documentation package.
