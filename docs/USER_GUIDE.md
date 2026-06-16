# User Guide

This guide explains how to use RR-framework as an assessment workbook.

## Recommended software

Use Microsoft Excel desktop for the best experience. Some charts, formulas, and workbook features may not behave identically in online spreadsheet editors.

## Navigation

Open the workbook on the **① START HERE** sheet. It contains a colour-coded navigation hub: click **▶ open** next to any sheet to jump to it. Every visible sheet has a header band with its purpose, a short note on what you can and cannot edit, and a **⌂ START HERE** link to return.

Convention: edit **coloured input cells only**; everything else is formula-driven.

## Assessment workflow

### Step 1: Open the workbook

Open `workbook/RR-framework_v1.67.xlsx` and confirm on START HERE:

- Framework: RR-framework
- Version: 1.67
- Build ID: RR-FRAMEWORK-v1.67-20260616
- License: CC BY-NC-SA 4.0

### Step 2: Complete Company Profile

Fill the **Company Profile** sheet using the dropdowns. Key fields include industry template, ownership type, revenue size band, operating and revenue model, customer/supplier concentration, workforce distribution, critical locations/processes/products, crisis history, and default confidence settings. These influence how the workbook interprets scores, risks, crisis exposure, and strategy packages.

### Step 3: Complete the assessment

Answer on the **Assessment Questions** sheet (the consolidated 424-question surface). Edit only the input columns (answer / coverage / confidence / comment). Each question uses a two-field answer: STAGE (0–5 wording) × COVERAGE (how widely deployed), further adjusted by confidence. Use the scoring guide on Methodology & Governance before answering.

### Step 4: Select a crisis scenario

On **Crisis & Resilience**, select a crisis scenario and severity. This adjusts risk priorities, strategy relevance, and initiative priority via the cascade engine.

### Step 5: Review outputs

- **Scoring & Diagnostics** — maturity, gaps, data-quality flags.
- **Strategy Risk Recs** — risk summary, strategic posture, recommendations.
- **Roadmap & Portfolio** — WSJF prioritization, status, Gantt.
- **Executive Dashboard** — consolidated executive view.
- **Standards & Coverage** — traceability to standards/frameworks.

### Step 6: Interpret the results

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

Where confidence fields are used, select evidence and assessor confidence carefully. High scores without evidence should be treated cautiously (the Scoring & Diagnostics sheet flags these).

## Advanced: calibration

Advanced users/consultants can tune the model in one place: open `_TECH_Scoring_Settings` (unhide it) and adjust the centralized `cfg_*` calibration parameters (crisis-severity cutoffs, industry-priority thresholds, timeline buckets, strategy scaling). Optional pairwise domain weighting is on **AHP Domain Weights**.

## Recommended operating model

1. Assign domain owners.
2. Collect initial responses.
3. Review evidence.
4. Discuss disagreement.
5. Adjust scores only when evidence supports the change.
6. Review dashboard and roadmap with leadership.

## Limitations

The workbook is a decision-support model. It does not replace expert review, formal audit, legal advice, cybersecurity testing, or certified business continuity assessment.
