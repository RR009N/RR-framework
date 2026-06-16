# RR-framework

**RR-framework** is an open, Excel-based business resilience and digital maturity assessment workbook created by Roman Reznikov.

The workbook helps organizations assess how mature, digitalized, and crisis-ready they are across business functions. It combines company context, a consolidated assessment, industry templates, crisis simulation, risk logic, executive strategy packages, recommendations, and implementation roadmaps.

Current version: **v1.67**  
Build ID: **RR-FRAMEWORK-v1.67-20260616**  
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
- Heatmaps, dashboards, Gantt roadmap, and quality-control indicators.

## What's new in v1.67

- **Navigation hub** on the START HERE sheet: a grouped, colour-coded, clickable index of every tab.
- **Uniform headers** on every visible sheet: purpose, edit guidance, and a one-click link back to START HERE.
- **Centralized calibration** (`cfg_*` parameters) and **named ranges** (`qn_*`) for transparency and easier tuning.
- **Engine cleanup**: strategy scoring refactored to `SUMPRODUCT`, diagnostics rebuilt as `COUNTIFS`.
- **Tighter error handling**: 2,650 lookup guards moved from `IFERROR` to `IFNA`.
- **Bug fixes** in the risk-prioritization layer (crisis multiplier, WSJF division guards, diagnostics ranges, self-references), verified by a full recalculation audit on a blank template and three filled industry samples.

See [CHANGELOG.md](CHANGELOG.md) and [RELEASE_NOTES_v1.67.md](RELEASE_NOTES_v1.67.md).

## Who can use it

- CEOs, COOs, CIOs, CTOs, CFOs, and transformation leaders.
- Risk, resilience, continuity, and operations teams.
- Consultants and advisors working on resilience, digital maturity, transformation, and crisis readiness.
- Researchers and educators working with digital transformation, strategic resilience, and organizational maturity models.

## Intended use

The workbook is intended for diagnostic and advisory use. It is not a formal certification, legal audit, financial audit, cybersecurity audit, compliance audit, or substitute for professional judgment.

Typical use flow:

1. Open the workbook in Microsoft Excel desktop.
2. Start on the **START HERE** sheet and use the navigation hub.
3. Complete the **Company Profile**.
4. Answer the **Assessment Questions**.
5. Select a crisis scenario and severity on **Crisis & Resilience**.
6. Review **Scoring & Diagnostics**, **Strategy Risk Recs**, **Roadmap & Portfolio**, and the **Executive Dashboard**.
7. Use the results as a structured input for management discussion and resilience planning.

## Workbook structure

The 28-tab workbook is organized into four logical layers (visible on the START HERE navigation hub):

| Layer | Purpose |
|---|---|
| Workflow (visible) | START HERE, Company Profile, Assessment Questions, Scoring & Diagnostics, AHP Domain Weights, Crisis & Resilience, Strategy Risk Recs, Roadmap & Portfolio, Executive Dashboard, Standards & Coverage, Methodology & Governance. |
| Data layer (hidden) | Normalized question table and dashboard data mart. |
| Config & assumptions (hidden) | Scoring settings, calibration parameters, industry templates, benchmarks, financial anchors, picklists. |
| Engines & libraries (protected) | Crisis/cascade model, risk and strategy libraries, recommendation matrix, initiative library. |

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

> Reznikov, Roman. RR-framework: Business Resilience and Digital Maturity Assessment Workbook. Version 1.67, 2026.

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
├── RELEASE_NOTES_v1.67.md
├── VERSION
├── workbook/
│   └── RR-framework_v1.67.xlsx
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
