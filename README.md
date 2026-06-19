# RR-framework

**RR-framework** is an open, Excel-based business resilience and digital maturity assessment workbook created by Roman Reznikov.

The workbook helps organizations assess how mature, digitalized, and crisis-ready they are across business functions. It combines company context, a consolidated assessment, industry templates, crisis simulation, risk logic, executive strategy packages, recommendations, and implementation roadmaps.

Current version: **v2.0**  
Build ID: **RR-FRAMEWORK-v2.0-20260619**  
License: **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International**  
SPDX License ID: **CC-BY-NC-SA-4.0**  
Copyright: **(C) Roman Reznikov**

## What the workbook does

RR-framework helps assess:

- Process maturity across key organizational domains.
- Digitalization level and technology adoption.
- Organizational resilience under disruption.
- Industry-adjusted maturity gaps.
- Crisis exposure under selected scenarios.
- Key risks created by low maturity or weak controls.
- Executive-level strategy packages.
- Prioritized initiatives and roadmap waves.
- Heatmaps, dashboards, and quality-control indicators.

## What's new in v2.0

v2.0 is a major **architecture refactor and integrity-hardening** release. The calculation model is preserved, but the workbook is rebuilt on a clean, layered structure that is easier to navigate, audit, and extend.

- **Layered architecture (20 tabs).** Consolidated to **9 visible workflow sheets**, **7 hidden data/config sheets**, and **4 very-hidden protected engines**, replacing the previous mixed 28-tab layout. A strict naming convention separates concerns: `_DATA_*` (normalized facts), `_ENGINE_*` (Risk, Crisis, Strategy, Initiatives, Fuzzy posture), `_CONFIG_*` (model settings, risk calibration), `_REF_*` (reference content).
- **Linear workflow.** The visible journey is a clean six-step path: Company Profile -> Assessment Questions -> AS-IS Assessment -> Resilience & Risk Scenario -> Action Plan & Roadmap -> Model Calibration.
- **Single source of truth.** All tunable parameters live in `_CONFIG_Model_Settings` and `_CONFIG_Risk_Calibration`; engines and presentation no longer duplicate calibration.
- **Structured Excel Tables.** The two growth lists - `_ENGINE_Initiatives` (`tblInitiatives`) and `_ENGINE_Strategy` (`tblStrategy`) - are now native Excel Tables, so adding initiatives or strategies auto-extends the column formulas. This is the foundation for the upcoming dynamic-range and quantitative-modeling work.
- **Integrity verified.** 55,096 formulas with **zero `#REF!`** and no broken cross-sheet references after the rename; the original `RecommendationMatrixTable` is preserved; data validations, conditional formatting, the chart, drawings, and comments are intact. The file opens cleanly in Microsoft Excel and LibreOffice with no repair prompt.

See [CHANGELOG.md](CHANGELOG.md) and [RELEASE_NOTES_v2.0.md](RELEASE_NOTES_v2.0.md). Earlier public history is in [RELEASE_NOTES_v1.67.md](RELEASE_NOTES_v1.67.md).

## Who can use it

- CEOs, COOs, CIOs, CTOs, CFOs, and transformation leaders.
- Risk, resilience, continuity, and operations teams.
- Consultants and advisors working on resilience, digital maturity, transformation, and crisis readiness.
- Researchers and educators working with digital transformation, strategic resilience, and organizational maturity models.

## Intended use

The workbook is intended for diagnostic and advisory use. It is not a formal certification, legal audit, financial audit, cybersecurity audit, compliance audit, or substitute for professional judgment.

Typical use flow:

1. Open the workbook in Microsoft Excel desktop.
2. Start on the **① START HERE** sheet and follow the recommended flow.
3. Complete the **Company Profile**.
4. Answer the **Assessment Questions**.
5. Review **AS-IS Assessment** (current-state maturity, gaps, data quality).
6. Select a crisis scenario and severity on **Resilience & Risk Scenario**.
7. Review **Action Plan & Roadmap** for recommendations, prioritized initiatives, and waves.
8. Use the results as a structured input for management discussion and resilience planning.

## Workbook structure

The 20-tab workbook is organized into four logical layers:

| Layer | Visibility | Sheets |
|---|---|---|
| Workflow | Visible (9) | ① START HERE, Release & QA, Methodology Controls & Std, Company Profile, Assessment Questions, AS-IS Assessment, Resilience & Risk Scenario, Action Plan & Roadmap, Model Calibration. |
| Data layer | Hidden | `_DATA_Assessment_Model`, `_DATA_Dashboard_Facts`, `_DATA_Mappings`. |
| Config & reference | Hidden | `_CONFIG_Model_Settings`, `_CONFIG_Risk_Calibration`, `_REF_Model_Content`, `_ENGINE_Fuzzy_Posture`. |
| Engines (protected) | Very hidden | `_ENGINE_Risk`, `_ENGINE_Crisis`, `_ENGINE_Strategy`, `_ENGINE_Initiatives`. |

More details are in [docs/WORKBOOK_ARCHITECTURE.md](docs/WORKBOOK_ARCHITECTURE.md).

## License and attribution

The workbook, methodology, questionnaires, scoring model, risk library, strategy package logic, crisis simulation logic, and documentation are licensed under **CC BY-NC-SA 4.0**.

You may use, share, and adapt this work for non-commercial purposes if you:

- Give appropriate attribution to **Roman Reznikov**.
- Link back to the original repository.
- Indicate whether changes were made.
- Share adaptations under the same license.
- Do not remove attribution notices from workbook copies or derivative documentation.

Commercial use, including paid consulting delivery using this workbook or derivative versions, requires separate written permission from the author.

See [LICENSE.md](LICENSE.md) and [NOTICE.md](NOTICE.md).

## Citation

If you use this workbook or methodology in research, education, consulting materials, or public documentation, please cite it using the metadata in [CITATION.cff](CITATION.cff).

Recommended citation:

> Reznikov, Roman. RR-framework: Business Resilience and Digital Maturity Assessment Workbook. Version 2.0, 2026. https://github.com/RR009N/RR-framework

## Disclaimer

RR-framework is provided "as is". It does not guarantee completeness, accuracy, compliance, certification readiness, financial outcomes, security posture, or crisis survival. Users remain responsible for validating outputs, assumptions, risks, controls, and recommendations in their own organizational context.

See [DISCLAIMER.md](DISCLAIMER.md).

## Repository contents

```text
.
├── README.md
├── LICENSE.md
├── NOTICE.md
├── CITATION.cff
├── CHANGELOG.md
├── DISCLAIMER.md
├── CONTRIBUTING.md
├── SECURITY.md
├── RELEASE_NOTES_v2.0.md
├── RELEASE_NOTES_v1.67.md
├── VERSION
├── workbook/
│   └── RR-framework_v2.0.xlsx
├── releases/
│   └── checksums.txt
└── docs/
    ├── USER_GUIDE.md
    ├── METHODOLOGY.md
    ├── WORKBOOK_ARCHITECTURE.md
    ├── ADMIN_GUIDE.md
    ├── DATA_DICTIONARY.md
    ├── SCORING_LOGIC.md
    ├── CRISIS_SCENARIOS.md
    ├── FORMS_INTEGRATION.md
    ├── RELEASE_CHECKLIST.md
    ├── ROADMAP.md
    └── FAQ.md
```

## Download

Use the workbook from the `workbook/` folder or from the latest GitHub Release.

Always verify that the version, build ID, and checksum match the release documentation.
