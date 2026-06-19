# Changelog

All notable changes to RR-framework will be documented in this file.

The format is inspired by Keep a Changelog, and this project uses semantic versioning where practical.

Intermediate iterations 1.1 through 1.5 are documented in detail inside the workbook on the **Methodology & Governance** sheet (Version & Release History). They are summarized here under 1.67.

## [2.0] - 2026-06-19

### Changed

- Major architecture refactor: consolidated to a layered 20-tab structure (9 visible workflow sheets, 7 hidden data/config/reference sheets, 4 very-hidden protected engines), replacing the previous mixed 28-tab layout.
- Strict naming convention introduced to separate concerns: `_DATA_*` (normalized facts), `_ENGINE_*` (Risk, Crisis, Strategy, Initiatives, Fuzzy posture), `_CONFIG_*` (model settings, risk calibration), `_REF_*` (reference content).
- Visible journey simplified to a linear six-step workflow: Company Profile -> Assessment Questions -> AS-IS Assessment -> Resilience & Risk Scenario -> Action Plan & Roadmap -> Model Calibration.
- Calibration centralized into a single source of truth (`_CONFIG_Model_Settings`, `_CONFIG_Risk_Calibration`); duplicated parameters removed.

### Added

- Native Excel Tables on the two growth lists: `tblInitiatives` on `_ENGINE_Initiatives` (A4:BY76) and `tblStrategy` on `_ENGINE_Strategy` (A4:AR18), so new rows auto-extend column formulas.

### Verified

- 55,096 formulas with zero `#REF!` and no broken references to former sheet names after the rename.
- Original `RecommendationMatrixTable` preserved; data validations, conditional formatting, chart, drawings, and comments intact.
- Opened and re-saved cleanly by Microsoft Excel and LibreOffice (headless) with no repair prompt; all three tables recognized as valid.

### Notes

- Intermediate internal builds between 1.67 and 2.0 are summarized here and documented inside the workbook on the methodology sheet.

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
