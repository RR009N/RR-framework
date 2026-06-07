# Workbook Architecture

RR-framework is organized into client-facing, input, admin, and technical layers.

## Client value layer

These sheets deliver management value and should usually remain visible in a client edition:

- Start Here
- Company Profile
- Crisis Simulator
- Dashboard
- Executive Strategy Packages
- Executive Recommendations
- Risk Summary
- Initiatives Roadmap
- Gantt Roadmap
- Heatmaps
- Spider Dashboards
- Scoring Guide

## Client input layer

These sheets collect assessment information:

- Strategy GTM
- Governance Crisis
- HR Workforce
- Finance Procurement
- Legal Risk
- Physical Safety
- Delivery Ops
- Supply Chain
- Manufacturing MES
- Sales CRM
- Marketing Comms
- IT Cloud DR
- Business Systems
- Data BI AI
- Cyber Privacy
- Quality Portfolio
- Company Geography

## Consultant and admin layer

These sheets support model review, scoring audit, methodology review, quality control, and calibration.

Examples:

- Improved Scoring Model
- Scoring Model v2
- AHP Domain Weights
- Quality Control
- Standards Map
- Standards per Question
- Methodology and Logic
- Cascade Engine Methodology

## Technical engine layer

These sheets should normally be hidden or very hidden in a client edition:

- Risk Library
- Recommendation Matrix
- Industry Templates
- Scoring Settings
- Crisis Model
- Strategy Library
- Strategy Packages
- Initiative Library
- Profile Lists
- Dependency Map
- Cascade Engine

## Recommended editions

| Edition | Purpose | Visible sheets |
|---|---|---|
| Client Edition | For client workshops and results review. | Client value layer and input layer. |
| Consultant Edition | For methodology review and model configuration. | All sheets. |
| Public Demo Edition | For GitHub release and learning. | Client value layer, input layer, documentation sheets, protected technical logic. |

## Design principle

The client should see a simple journey:

```text
Profile → Assessment → Crisis Simulation → Results → Strategy Packages → Roadmap
```

The technical model should remain available for transparency, but it should not overload normal users.
