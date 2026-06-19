# Methodology

RR-framework is designed as a practical business resilience and digital maturity assessment model. It combines structured company profiling, domain questionnaires, maturity scoring, industry-specific interpretation, risk logic, crisis simulation, recommendation logic, strategy packages, and roadmap prioritization.

> **Where this lives in v2.0:** the conceptual flow below is implemented across the layered workbook — inputs on Company Profile and Assessment Questions; current state on AS-IS Assessment; scenario adjustment and fuzzy posture on Resilience & Risk Scenario; recommendations, strategy packages, and initiatives on Action Plan & Roadmap. The calculation itself runs in the protected `_ENGINE_*` sheets, with parameters in `_CONFIG_*`. See WORKBOOK_ARCHITECTURE.md.

## Core logic

The model follows this flow:

```text
Company Profile
→ Domain Questionnaires
→ Scoring and Confidence Adjustment
→ Industry Target and Gap Logic
→ Risk Engine
→ Crisis Scenario Adjustment
→ Recommendation Engine
→ Strategy Packages
→ Initiative Roadmap
→ Executive Outputs
```

## Assessment dimensions

Each organization is assessed across three horizontal dimensions:

| Dimension | Meaning |
|---|---|
| Process Maturity | How formalized, owned, measured, and repeatable the organization's processes are. |
| Digitalization | How well the organization uses systems, data, workflows, automation, analytics, and digital technologies. |
| Resilience | How ready the organization is to continue, recover, or adapt during disruption. |

A single question may contribute to one or more dimensions.

## Domain model

The questionnaire is organized by business domains, because organizations usually manage maturity and resilience through functions.

Examples:

- Strategy and GTM.
- Governance and crisis management.
- HR and workforce.
- Finance and procurement.
- Legal and risk.
- Physical safety.
- Delivery and operations.
- Supply chain.
- Manufacturing and MES.
- Sales and CRM.
- Marketing and communication.
- IT, cloud, and disaster recovery.
- Business systems.
- Data, BI, and AI.
- Cybersecurity and privacy.
- Quality and portfolio management.
- Company geography.

## Company Profile logic

The Company Profile adjusts how the model interprets the organization.

Profile parameters include:

- Industry.
- Size.
- Operating model.
- Revenue model.
- Customer concentration.
- Supplier concentration.
- Workforce distribution.
- Critical locations.
- Critical processes.
- Critical products and services.
- Crisis history.

The same score can mean different risk levels depending on these parameters.

Example: weak MES maturity is highly material for manufacturing, but usually irrelevant for a professional services company.

## Industry templates

Industry templates act as interpretation modifiers. They do not replace the questionnaire. They change the meaning and priority of results.

Industry templates may influence:

- Domain weights.
- Target maturity.
- Criticality multipliers.
- Crisis exposure.
- Strategy package relevance.
- Initiative priority.
- Red-line controls.

## Risk logic

Risk is derived from the combination of:

- Low maturity.
- High business criticality.
- Industry relevance.
- Crisis scenario relevance.
- Weak confidence or lack of evidence.
- Critical control breaches.

The risk model is designed to identify where weak organizational capabilities may become material business exposure.

## Crisis simulation logic

The Crisis Simulator allows the user to select a crisis scenario and severity level.

The selected crisis scenario modifies domain exposure, risk priorities, strategy package ranking, and initiative priority.

Examples:

- Cyberattack increases the relevance of cybersecurity, backups, access management, incident response, and data protection.
- Energy crisis increases the relevance of production continuity, backup power, facility resilience, and operational scheduling.
- Supply chain disruption increases the relevance of supplier diversification, inventory visibility, logistics alternatives, and procurement governance.

## Recommendation logic

Recommendations are generated based on maturity gaps and current score levels.

The core principle is:

```text
Current score → Next maturity level → Recommended action
```

Recommendations are then grouped into executive-level strategy packages and implementation initiatives.

## Strategy package logic

A strategy package is a grouped set of related initiatives and recommendations. It is designed to be understandable to executives.

Strategy package ranking can depend on:

- Domain gaps.
- Active risks.
- Industry profile.
- Revenue model.
- Crisis scenario.
- Initiative priority.
- Roadmap feasibility.

## WSJF prioritization

WSJF is used to rank initiatives and recommendations.

Formula:

```text
Cost of Delay = Business Value + Time Criticality + Risk Reduction + Opportunity Enablement
WSJF = Cost of Delay / Job Size
```

Higher WSJF means higher priority.

## Standards and best-practice mapping

Questions and logic are informed by recognized standards and frameworks, including ISO, NIST, COSO, COBIT, ITIL, APQC, SCOR, and related management practices.

The workbook is not a certification or formal audit tool.
