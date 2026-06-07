# Scoring Logic

RR-framework uses a structured scoring model to translate questionnaire responses into maturity, digitalization, resilience, risk, and strategy outputs.

## Base score

Most questions use a 0 to 5 score.

| Score | Interpretation |
|---:|---|
| 0 | Not existing, unknown, or not applicable without evidence. |
| 1 | Ad hoc, informal, person-dependent. |
| 2 | Partially present, inconsistent, weakly documented. |
| 3 | Defined, but not fully measured, controlled, or integrated. |
| 4 | Managed, measured, reviewed, and mostly controlled. |
| 5 | Optimized, integrated, evidence-based, resilient, and continuously improved. |

## Normalized score

Raw scores can be converted to a 0 to 100 scale.

```text
Normalized Score = Raw Score / 5 * 100
```

## Confidence adjustment

When evidence confidence and assessor confidence are used, the model can adjust scores.

```text
Confidence Factor = Evidence Factor * Assessor Factor
Confidence-Adjusted Score = Normalized Score * Confidence Factor
```

The purpose is to reduce overconfidence where high scores are not supported by evidence.

## Domain score

Domain scores are calculated using question weights.

```text
Domain Score = SUM(Question Score * Question Weight) / SUM(Question Weights)
```

If normalized values are used:

```text
Domain Score 0-100 = SUM(Normalized Score * Weight) / SUM(Weights)
```

## Horizontal metrics

The workbook tracks three horizontal metrics:

- Process Maturity.
- Digitalization.
- Resilience.

A question can contribute to one or more metrics using relevance weights.

```text
Metric Score = SUM(Question Score * Question Weight * Metric Relevance) / SUM(Question Weight * Metric Relevance)
```

## Industry target and gap

Each industry can have different target maturity levels.

```text
Gap = MAX(0, Industry Target - Current Score)
```

For 0 to 100 scoring:

```text
Gap 0-100 = MAX(0, Industry Target 0-100 - Current Score 0-100)
```

## Industry-adjusted gap priority

Gaps become more important when they affect critical industry capabilities.

```text
Industry-Adjusted Gap Priority = Gap * Industry Criticality Multiplier
```

## Risk score

Risk scores are derived from maturity gaps, likelihood, impact, crisis scenario relevance, and control weakness.

Conceptual formula:

```text
Risk Score = Likelihood * Impact * Control Weakness * Crisis Multiplier * Criticality Multiplier
```

The workbook may use simplified scoring values to keep the model usable in Excel.

## Crisis-adjusted risk

When a crisis scenario is selected, affected domains and risks receive scenario multipliers.

```text
Crisis-Adjusted Risk = Base Risk Score * Scenario Multiplier * Severity Factor
```

## WSJF prioritization

WSJF ranks recommendations and initiatives.

```text
Cost of Delay = Business Value + Time Criticality + Risk Reduction + Opportunity Enablement
WSJF = Cost of Delay / Job Size
```

Higher WSJF indicates higher priority.

## Interpretation bands

Suggested score interpretation:

| Score range | Level | Interpretation |
|---:|---|---|
| 0-30 | Critical | High exposure and weak control. |
| 31-50 | Fragile | Some practices exist, but may fail under stress. |
| 51-70 | Managed | Basic control exists, but gaps remain. |
| 71-85 | Resilient | Strong capabilities in most cases. |
| 86-100 | Adaptive | Integrated, data-driven, optimized, and scenario-ready. |

## Important limitation

Scores are decision-support indicators. They should be reviewed with evidence, context, and professional judgment.
