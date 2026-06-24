# Release Notes: RR-framework v3.0

Release date: **2026-06-24**  
Build ID: **RR-FRAMEWORK-v3.0-20260624**  
DOI: **10.5281/zenodo.20583866**  
Concept DOI: **10.5281/zenodo.20583865**  
ORCID: **https://orcid.org/0000-0001-5581-5651**

## Summary

RR-framework **v3.0** is the fourth public-style release package and the first rounded **3.x** version line. It is based on the latest v2.9.46 calibration safety workbook, but cleans the release identity, workbook metadata, and documentation package so the artifact can be treated as a stable baseline rather than another late-stage 2.9.x calibration build.

## Why this release exists

The 2.9.x line accumulated many important model-hardening changes: profile-vector normalization, relevance logic, capability bridge, maturity-aware treatment library, industry wording, backend dictionary, LINT checks, Monte Carlo layer, and calibration fixes. The v2.9.46 file was technically strong enough to become a clean public baseline, but the versioning, metadata, and documentation still looked like a calibration/hotfix branch.

v3.0 solves that by making the release identity consistent.

## Workbook changes

### Changed

- Version rolled from **v2.9.46** to **v3.0**.
- Build ID synchronized to **RR-FRAMEWORK-v3.0-20260624**.
- Core workbook properties updated: title, subject, description, author, modified timestamp.
- Custom workbook properties updated: Version, BuildID, ReleaseDate, Copyright, DOI, ConceptDOI, License, SPDX, ORCID, TemplateState, Description.
- Visible **Guidelines** sheet updated with a release attribution/citation block.
- Hidden `_README` and `_DOC` sheets updated with release metadata.
- `_CONFIG_Model_Settings`, `_LINT`, `_ENGINE_MonteCarlo`, dropdown/version markers, and workbook documentation markers aligned to v3.0.

### Preserved

- 43-sheet architecture.
- 90,275 formulas.
- 424-question assessment model.
- 72 initiatives.
- 14 strategies.
- 12 crisis scenarios.
- 2,000-row Monte Carlo engine.
- 121 named ranges.
- 51 data validations.
- 37 conditional formatting blocks.
- 6 charts.
- No VBA/macros.
- No external links.

## Methodological state

v3.0 keeps the current canonical model chain:

```text
Company Profile
→ _ENGINE_Profile_Vector
→ _DATA_Assessment_Model
→ _ENGINE_Relevance
→ _REF_Capability_Bridge
→ _REF_Treatment_Library / _REF_Industry_Wording
→ _ENGINE_Risk
→ _ENGINE_Crisis / _ENGINE_Fuzzy_Posture
→ _ENGINE_Strategy
→ _ENGINE_Initiatives
→ AS-IS / Scenario / Roadmap outputs
```

## Verification

Static OOXML verification completed after packaging:

| Check | Result |
|---|---:|
| Workbook opens as valid ZIP/OOXML package | PASS |
| Sheet count | 43 |
| Formula count | 90,275 |
| Formula error tokens in XML | 0 |
| Excel error cells in XML | 0 |
| External links | 0 |
| Macros/VBA | 0 |
| DOI custom property present | PASS |
| ORCID custom property present | PASS |
| v3.0 markers present in workbook XML | PASS |

## Known limitation

The workbook has `fullCalcOnLoad` / force recalculation semantics. Microsoft Excel desktop should be used for final recalculation and saved output before distributing a filled assessment. This is expected for a formula-heavy workbook with cached outputs.

## Recommended release tag

`v3.0`



---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
