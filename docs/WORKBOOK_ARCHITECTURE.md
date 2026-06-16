# Workbook Architecture (v1.67)

RR-framework v1.67 uses a consolidated 28-tab structure: **11 visible workflow tabs**, **13 hidden backend tabs**, and **4 very-hidden protected libraries**. The separation keeps the user journey simple while preserving the full calculation model. The START HERE sheet exposes this structure as a clickable navigation hub.

## 1. Workflow layer (visible)

The user/consultant journey, in order:

- **① START HERE** — navigation hub, recommended workflow, colour legend, version/build.
- **Company Profile** — company context (industry, size, geography, concentrations). Input.
- **Assessment Questions** — the consolidated 424-question assessment. Primary input.
- **Scoring & Diagnostics** — maturity, confidence-adjusted scores, gaps, data-quality checks.
- **AHP Domain Weights** — optional pairwise weight calibration (advanced).
- **Crisis & Resilience** — crisis scenario, cascade logic, stress testing. Input (scenario + severity).
- **Strategy Risk Recs** — risk summary, strategic posture, recommendations.
- **Roadmap & Portfolio** — initiative prioritization (WSJF), economics, status, Gantt.
- **Executive Dashboard** — consolidated executive view: maturity, risk, benchmarks, financial resilience.
- **Standards & Coverage** — standards / framework mapping and traceability.
- **Methodology & Governance** — methodology, scoring guide, version history, cascade logic, data-model change log.

## 2. Data layer (hidden)

Normalized backend feeding scoring, engines, and outputs:

- **_DATA_Questions_Normalized** — canonical one-row-per-question table.
- **_DATA_Executive_Dashboard** — dashboard data mart / aggregated KPIs.

## 3. Configuration & assumptions (hidden)

Tunable inputs and reference data:

- **_TECH_Scoring_Settings** — confidence factors, risk appetite, and centralized calibration parameters (`cfg_*`).
- **_TECH_Industry_Templates** — per-industry target maturities.
- **_TECH_Industry_Strategy_Fit** — industry-to-strategy fit weighting.
- **_TECH_Profile_Lists** — dropdown / picklist source values.
- **_TECH_Benchmarks** — seed peer benchmarks.
- **_TECH_Financial_Anchors** — financial anchors & monetization mapping.

## 4. Engines & libraries (hidden / very-hidden, protected)

The calculation engines and vocabularies. Do not edit:

- **_TECH_Crisis_Model**, **_TECH_Cascade_Engine**, **_TECH_Crisis_Links**, **_TECH_Dependency_Map** — resilience / cascade engine.
- **Recommendation Matrix**, **Risk Library**, **_TECH_Strategy_Library**, **_TECH_Strategy_Packages** — risk & strategy logic.
- **_TECH_Initiative_Library** — initiative catalogue / roadmap engine.

## Named ranges and parameters

- `qn_*` — named ranges over the normalized question columns (data layer), used by diagnostics.
- `cfg_*` — centralized calibration thresholds in `_TECH_Scoring_Settings` (e.g. crisis-severity cutoffs, industry-priority thresholds, timeline buckets, strategy scaling). Recalibrate here in one place.

## Recommended editions

| Edition | Purpose | Visible sheets |
|---|---|---|
| Client Edition | Workshops and results review. | Workflow layer. |
| Consultant Edition | Methodology review and configuration. | All sheets (unhide backend). |
| Public Demo Edition | GitHub release and learning. | Workflow layer + protected technical logic. |

## Design principle

```text
START HERE → Company Profile → Assessment Questions → Crisis & Resilience → Scoring & Diagnostics → Strategy Risk Recs → Roadmap & Portfolio → Executive Dashboard
```

User input, normalized data, calculation engines, and executive outputs are separated to reduce tab count without losing logic. Backend and engine sheets stay hidden/very-hidden for transparency without overloading normal users.
