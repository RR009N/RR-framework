# Workbook Architecture (v2.0)

RR-framework v2.0 uses a consolidated **20-tab layered structure**: **9 visible workflow sheets**, **7 hidden data/config/reference sheets**, and **4 very-hidden protected engines**. The layout deliberately separates presentation, data, configuration, and calculation so the user journey stays simple while the model remains fully auditable and extensible.

A strict naming convention encodes the layer of every backend sheet:

- `_DATA_*` — normalized facts and data marts.
- `_ENGINE_*` — calculation engines and libraries.
- `_CONFIG_*` — tunable parameters (single source of truth).
- `_REF_*` — reference content (templates, vocabularies).

## 1. Workflow layer (visible)

The user/consultant journey, in order:

- **① START HERE** — recommended flow, legend, version/build.
- **Release & QA** — release metadata and quality-assurance log.
- **Methodology, Controls & Std** — methodology summary, controls, and standards mapping reference.
- **Company Profile** — company context (industry, size, geography, concentrations). Input.
- **Assessment Questions** — the consolidated 424-question assessment. Primary input.
- **AS-IS Assessment** — current-state view: maturity, gaps, and data-quality signals.
- **Resilience & Risk Scenario** — crisis scenario + severity selection, scenario-adjusted state, and fuzzy resilience posture. Input (scenario + severity).
- **Action Plan & Roadmap** — recommendations, prioritized initiatives (WSJF), and roadmap waves.
- **Model Calibration** — admin/consultant control surface that points to the configuration layer.

## 2. Data layer (hidden)

Normalized backend feeding scoring, engines, and outputs:

- **_DATA_Assessment_Model** — canonical one-row-per-question model with derived scores.
- **_DATA_Dashboard_Facts** — aggregated KPIs / dashboard data mart.
- **_DATA_Mappings** — recommendation vocabulary and question/initiative mappings (contains the `RecommendationMatrixTable`).

## 3. Configuration & reference (hidden)

Tunable inputs and reference data — the single source of truth for calibration:

- **_CONFIG_Model_Settings** — confidence factors, risk appetite, objective/strategic weights, financial anchors, and all calibration parameters.
- **_CONFIG_Risk_Calibration** — per-domain exposure, incident history, evidence uncertainty, dependency/cascade scores, and red-line floors.
- **_REF_Model_Content** — industry templates, strategy/initiative reference content.
- **_ENGINE_Fuzzy_Posture** — fuzzy resilience-posture model (Fragile → Exposed → Adaptive → Resilient → Anti-fragile) feeding strategic weighting.

## 4. Engines (very hidden, protected)

The calculation engines. Do not edit directly:

- **_ENGINE_Risk** — per-question/per-domain risk engine (probability × impact, red-line floors, cascade contribution).
- **_ENGINE_Crisis** — crisis scenario model, severity multipliers, crisis-to-crisis coupling, and cross-domain cascade.
- **_ENGINE_Strategy** — strategy library and scoring (`tblStrategy`).
- **_ENGINE_Initiatives** — initiative catalogue and roadmap engine (`tblInitiatives`).

## Structured tables

Three native Excel Tables provide auto-extending, structured-reference-friendly ranges:

| Table | Sheet | Range | Purpose |
|---|---|---|---|
| `RecommendationMatrixTable` | `_DATA_Mappings` | A4:V411 | Score-based recommendation vocabulary. |
| `tblInitiatives` | `_ENGINE_Initiatives` | A4:BY76 | Initiative catalogue; new initiatives auto-extend column formulas. |
| `tblStrategy` | `_ENGINE_Strategy` | A4:AR18 | Strategy library; new strategies auto-extend column formulas. |

Adding a row directly under a table extends it and copies the column formulas automatically. This is the structural basis for safe list expansion and the upcoming quantitative-modeling work.

## Design principle

```text
Company Profile → Assessment Questions → AS-IS Assessment → Resilience & Risk Scenario → Action Plan & Roadmap
        (input)            (input)            (current state)        (scenario-adjusted)         (what to do)
```

User input, normalized data, configuration, and calculation engines are separated so the visible tab count stays low without losing any logic. Backend and engine sheets stay hidden/very-hidden for transparency without overloading normal users; everything tunable is reachable from **Model Calibration**.

## Migration note (from v1.67)

The v1.67 public release used a 28-tab layout with calculation logic spread across visible sheets (Crisis & Resilience, Strategy Risk Recs, Roadmap & Portfolio, Executive Dashboard, etc.). v2.0 consolidates that logic into the `_ENGINE_*`/`_DATA_*` layers and re-expresses the visible journey as the six-step flow above. The model is equivalent; the structure is cleaner. The refactor was verified to preserve all formulas (zero `#REF!`), tables, validations, conditional formatting, and visuals.
