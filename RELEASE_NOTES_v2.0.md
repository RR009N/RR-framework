# Release Notes: RR-framework v2.0

Release date: 2026-06-19

Build ID: RR-FRAMEWORK-v2.0-20260619

## Summary

v2.0 is a major **architecture refactor and integrity-hardening** release. The assessment logic, scoring model, risk engine, crisis simulation, and roadmap prioritization are preserved, but the workbook is rebuilt on a clean, layered, strictly named structure that is far easier to navigate, audit, and extend. This release also lays the structural foundation for the planned quantitative-modeling cycle (dynamic ranges, scenario simulation).

## Highlights

- **Layered 20-tab architecture.** 9 visible workflow sheets, 7 hidden data/config/reference sheets, and 4 very-hidden protected engines, replacing the previous mixed 28-tab layout. Concerns are separated by a strict naming convention: `_DATA_*`, `_ENGINE_*`, `_CONFIG_*`, `_REF_*`.
- **Linear six-step workflow.** Company Profile -> Assessment Questions -> AS-IS Assessment -> Resilience & Risk Scenario -> Action Plan & Roadmap -> Model Calibration. Heavy calculation is moved off the visible sheets into the engine layer.
- **Single source of truth for calibration.** All tunable parameters consolidated into `_CONFIG_Model_Settings` and `_CONFIG_Risk_Calibration`; no duplicated calibration across engines and presentation.
- **Structured Excel Tables on growth lists.** `_ENGINE_Initiatives` (`tblInitiatives`, A4:BY76) and `_ENGINE_Strategy` (`tblStrategy`, A4:AR18) are now native Excel Tables, so adding rows auto-extends the column formulas. This prepares the workbook for safe list expansion and the upcoming quantitative logic.
- **Engines isolated and protected.** Risk, Crisis, Strategy, and Initiative engines are very-hidden; the fuzzy-posture engine and reference content sit in the config/reference layer.

## Verification

- 55,096 formulas; **zero `#REF!`**; no broken references to former sheet names after the rename.
- Original `RecommendationMatrixTable` preserved; the two new tables added without disturbing existing logic.
- Data validations, conditional formatting, the chart, drawings, and comments all preserved.
- The file was opened and re-saved cleanly by both Microsoft Excel and LibreOffice (headless) with no repair prompt; all three tables are recognized as valid.

## Known items / next cycle

- `_ENGINE_Risk` is not yet a structured Table: its header row contains unlabeled calculation columns. Defining those headers (the target schema) and converting it is the first task of the next cycle.
- `_DATA_Mappings` currently stacks two datasets (question recommendations, then initiative rows); its table range will be split/extended during data cleanup.
- Planned quantitative modeling (Monte-Carlo loss distribution with VaR/CVaR, Leontief cascade propagation, Markov posture dynamics) is tracked in `docs/ROADMAP.md`.

## Compatibility

- Microsoft Excel desktop recommended.
- No macros. The file remains a standard `.xlsx`.

## License

CC BY-NC-SA 4.0. Copyright (C) Roman Reznikov.

## Checksum

See `releases/checksums.txt`.


---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
