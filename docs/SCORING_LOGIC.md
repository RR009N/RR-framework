# Scoring Logic

RR-framework uses a 0–5 maturity scoring model. Scores are interpreted through evidence confidence, industry target gaps, relevance, crisis scenario exposure, and roadmap prioritization.

## Base score

| Score | Interpretation |
|---:|---|
| 0 | Not existing, unknown, or not applicable without evidence. |
| 1 | Ad hoc, informal, person-dependent. |
| 2 | Partially present, inconsistent, weakly documented. |
| 3 | Defined, but not fully measured, controlled, or integrated. |
| 4 | Managed, measured, reviewed, and mostly controlled. |
| 5 | Optimized, integrated, evidence-based, resilient, and continuously improved. |

## Core calculations

```text
Normalized Score = Raw Score / 5 * 100
Domain Score = SUM(Question Score × Weight) / SUM(Weight)
Gap = MAX(0, Industry Target - Current Score)
Industry-Adjusted Gap Priority = Gap × Industry Criticality Multiplier
```

## Confidence adjustment

Evidence confidence and assessor confidence reduce overconfident scores when evidence is weak.

```text
Confidence Factor = Evidence Factor × Assessor Factor
Confidence-Adjusted Score = Score × Confidence Factor
```

## Risk logic

Risk is driven by maturity gaps, scenario relevance, crisis multipliers, control weakness, industry criticality, and capability relevance.

## Initiative logic

Initiative priority uses a WSJF-style scoring approach:

```text
WSJF ≈ (Business Value + Time Criticality + Risk Reduction + Opportunity Enablement) / Job Size
```

The workbook adjusts prioritization through relevance, crisis, industry wording, and capability mapping.



---

**Attribution:** RR-framework v3.0 — Copyright (C) 2026 Roman Reznikov.  
**Author:** Roman Reznikov. ORCID: https://orcid.org/0000-0001-5581-5651.  
**DOI:** 10.5281/zenodo.20583866. Concept DOI: 10.5281/zenodo.20583865.  
**License:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC-BY-NC-SA-4.0). Commercial use requires separate written permission.
