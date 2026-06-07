# RR-framework
[![DOI](https://zenodo.org/badge/1262222190.svg)](https://doi.org/10.5281/zenodo.20583865)

**RR-framework** is an open, Excel-based business resilience and digital maturity assessment workbook created by Roman Reznikov.

The workbook helps organizations assess how mature, digitalized, and crisis-ready they are across business functions. It combines company context, domain questionnaires, industry templates, crisis simulation, risk logic, executive strategy packages, recommendations, and implementation roadmaps.

Current version: **v1.0**  
Build ID: **RR-FRAMEWORK-v1.0-20260607**  
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
- Heatmaps, spider dashboards, Gantt roadmap, and quality-control indicators.

## Who can use it

The framework is designed for:

- CEOs, COOs, CIOs, CTOs, CFOs, and transformation leaders.
- Risk, resilience, continuity, and operations teams.
- Consultants and advisors working on resilience, digital maturity, transformation, and crisis readiness.
- Researchers and educators working with digital transformation, strategic resilience, and organizational maturity models.

## Intended use

The workbook is intended for diagnostic and advisory use. It is not a formal certification, legal audit, financial audit, cybersecurity audit, compliance audit, or substitute for professional judgment.

Typical use flow:

1. Open the workbook in Microsoft Excel desktop.
2. Complete the Company Profile.
3. Assign or complete domain questionnaires.
4. Select a crisis scenario and severity.
5. Review dashboard outputs, risk summary, strategy packages, heatmaps, spider charts, and roadmap.
6. Use the results as a structured input for management discussion and resilience planning.

## Workbook structure

The workbook has three conceptual layers:

| Layer | Purpose |
|---|---|
| Client value layer | Dashboard, risks, strategies, recommendations, roadmap, simulation, heatmaps. |
| Client input layer | Company profile and domain questionnaires. |
| Technical/admin layer | Scoring logic, risk libraries, recommendation matrices, industry templates, standards mapping, hidden calculations. |

More details are available in [docs/WORKBOOK_ARCHITECTURE.md](docs/WORKBOOK_ARCHITECTURE.md).

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

If you use RR-framework in research, consulting, education, or organizational assessment, please cite it as:

Roman Reznikov. RR-framework: Business Resilience and Digital Maturity Assessment Workbook. Version 1.0. Zenodo. https://doi.org/10.5281/zenodo.20583866

Concept DOI: https://doi.org/10.5281/zenodo.20583865  
Version DOI: https://doi.org/10.5281/zenodo.20583866

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
├── VERSION
├── workbook/
│   └── RR-framework_v1.0.xlsx
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
    └── FAQ.md
```

## Download

Use the workbook from the `workbook/` folder or from the latest GitHub Release.

Always verify that the version, build ID, and checksum match the release documentation.
