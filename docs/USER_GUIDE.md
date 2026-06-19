# User Guide

This guide explains how to use RR-framework as an assessment workbook.

## Recommended software

Use Microsoft Excel desktop for the best experience. Some charts, formulas, and workbook features may not behave identically in online spreadsheet editors.

## Navigation

Open the workbook on the **① START HERE** sheet. It shows the recommended flow and the version/build. Work left to right through the visible workflow sheets.

Convention: edit **coloured input cells only**; everything else is formula-driven. Backend sheets (`_DATA_*`, `_CONFIG_*`, `_REF_*`) are hidden and the calculation engines (`_ENGINE_*`) are very hidden and protected.

## Assessment workflow

### Step 1: Open the workbook

Open `workbook/RR-framework_v2.0.xlsx` and confirm on START HERE:

- Framework: RR-framework
- Version: 2.0
- Build ID: RR-FRAMEWORK-v2.0-20260619
- License: CC BY-NC-SA 4.0

### Step 2: Complete Company Profile

Fill the **Company Profile** sheet using the dropdowns. Key fields include industry template, ownership type, revenue size band, operating and revenue model, customer/supplier concentration, workforce distribution, critical locations/processes/products, crisis history, and default confidence settings. These influence how the workbook interprets scores, risks, crisis exposure, and strategy packages.

### Step 3: Complete the assessment

Answer on the **Assessment Questions** sheet (the consolidated 424-question surface). Edit only the input columns (answer / coverage / confidence / comment). Each question uses a two-field answer: STAGE (0–5 wording) × COVERAGE (how widely deployed), further adjusted by confidence. Use the scoring guide on **Methodology, Controls & Std** before answering.

### Step 4: Review the current state

Open **AS-IS Assessment** to see current-state maturity, gaps versus industry targets, and data-quality signals (for example, high scores entered without evidence).

### Step 5: Select a crisis scenario

On **Resilience & Risk Scenario**, select a crisis scenario and severity. This adjusts risk priorities, strategy relevance, initiative priority, and the fuzzy resilience posture via the crisis and cascade engines.

### Step 6: Review the action plan

Open **Action Plan & Roadmap** for recommendations, WSJF-prioritized initiatives, and roadmap waves. Standards/controls traceability is on **Methodology, Controls & Std**.

### Step 7: Interpret the results

Use outputs as a structured management discussion tool. Scores indicate maturity and potential exposure; they are not formal audit results.

## Scoring scale

| Score | Meaning |
|---:|---|
| 0 | Not existing or unknown. |
| 1 | Ad hoc and person-dependent. |
| 2 | Informal or partially present. |
| 3 | Defined but inconsistent or weakly measured. |
| 4 | Managed, measured, and mostly controlled. |
| 5 | Optimized, integrated, evidence-based, and resilient. |

## Evidence and confidence

Where confidence fields are used, select evidence and assessor confidence carefully. High scores without evidence should be treated cautiously (the AS-IS Assessment view flags these).

## Advanced: calibration

Advanced users/consultants tune the model from **Model Calibration**, which points to the configuration layer:

- `_CONFIG_Model_Settings` — confidence factors, risk appetite, objective/strategic weights, financial anchors, and calibration thresholds (crisis-severity cutoffs, industry-priority thresholds, timeline buckets, strategy scaling).
- `_CONFIG_Risk_Calibration` — per-domain exposure, incident history, evidence uncertainty, dependency/cascade scores, and red-line floors.

Unhide these sheets only if you intend to recalibrate.

## Recommended operating model

1. Assign domain owners.
2. Collect initial responses.
3. Review evidence.
4. Discuss disagreement.
5. Adjust scores only when evidence supports the change.
6. Review the action plan and roadmap with leadership.

## Limitations

The workbook is a decision-support model. It does not replace expert review, formal audit, legal advice, cybersecurity testing, or certified business continuity assessment.
