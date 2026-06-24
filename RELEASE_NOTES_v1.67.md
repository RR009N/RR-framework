# Release Notes: RR-framework v1.67

Release date: 2026-06-16

Build ID: RR-FRAMEWORK-v1.67-20260616

## Summary

v1.67 is a structural, correctness, and usability release built on the consolidated 28-tab architecture (11 visible workflow tabs, 13 hidden backend tabs, 4 very-hidden protected libraries). It hardens the calculation engine, fixes risk-prioritization bugs that only surface with real data, and makes the workbook substantially easier to navigate and read.

## Highlights

- **Navigation & readability:** clickable, colour-coded navigation hub on START HERE; uniform header band (purpose + edit guidance + Home link) on every visible sheet.
- **Calibration in one place:** tunable thresholds centralized as `cfg_*` parameters in `_TECH_Scoring_Settings`.
- **Engine cleanup:** strategy scoring refactored to `SUMPRODUCT`; diagnostics rebuilt as `COUNTIFS`; named ranges added on the data layer.
- **Error visibility:** 2,650 single-lookup guards moved from `IFERROR` to `IFNA`.
- **Bug fixes:** crisis multiplier corrected to the numeric SPOF column; WSJF / scenario-adjusted division guards; diagnostics row-range fix; self-reference fix on scenario/severity.

## Compatibility

- Microsoft Excel desktop recommended.
- No macros. The file remains a standard `.xlsx`.

## Verification

Full recalculation audit on a blank template and three filled industry samples; charts, dropdowns, and named ranges verified intact. The only residual cells flagged by the headless recalculator (R16/R61) are a known LibreOffice cross-sheet artifact and resolve correctly in Microsoft Excel.

## License

CC BY-NC-SA 4.0. Copyright (C) Roman Reznikov.

## Checksum

See `releases/checksums.txt`.


---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
