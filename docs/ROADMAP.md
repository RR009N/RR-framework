# Roadmap

This roadmap describes the direction of RR-framework. It is indicative, not a commitment.

## Delivered in v2.0

Focus: architecture refactor and structural foundation.

- Layered 20-tab architecture with strict `_DATA_*` / `_ENGINE_*` / `_CONFIG_*` / `_REF_*` naming.
- Linear six-step visible workflow.
- Single source of truth for calibration.
- Native Excel Tables on the initiative and strategy lists (auto-extending).
- Full integrity verification (zero `#REF!`; tables, validations, visuals preserved).

## Next: content & dynamic-range cycle

Focus: make the model safely extensible, then grow it.

- Define headers/target schema for `_ENGINE_Risk` and convert it to a structured Table.
- Split and re-scope the `_DATA_Mappings` table (separate question-recommendation and initiative datasets).
- Convert remaining engine input ranges to Tables or dynamic named ranges so downstream formulas auto-pick-up new rows.
- Expand the risk, initiative, and strategy libraries (broader scenarios and sectors).
- Add more industry templates and sample anonymized assessment data.

## Then: quantitative modeling cycle

Focus: move from point estimates to distributions and network propagation, kept in native Excel where practical.

- **Monte-Carlo crisis simulation** over the crisis engine: replace point multipliers with distributions and output a loss distribution with **VaR / CVaR** (tail risk) instead of a single peak value.
- **Leontief cascade** (`(I − βM)^-1`) over the cross-domain dependency matrix for full multi-hop propagation, plus largest-eigenvalue (systemic-amplification) analysis.
- **Markov posture dynamics**: model transitions across fuzzy resilience states over the course of a crisis and recovery.
- **Constrained portfolio optimization** of initiatives (budget and change-capacity limits) via Solver, complementing WSJF ranking.
- Global sensitivity (tornado / variance-based) on key drivers.

## Later: collection and application

Focus: controlled data collection and, eventually, application architecture.

- Google Forms / Microsoft Forms integration, respondent assignment, multi-respondent aggregation, disagreement and evidence-gap flags.
- Client Edition and Consultant Edition separation.
- Possible web-based assessment interface, database-backed storage, role-based access, automated dashboards, and an export/calculation API.

## Not planned for the core public workbook

- Commercial consulting templates.
- Client-specific benchmarks.
- Confidential assessment datasets.
- Formal certification workflows.
- Investment-grade valuation logic.
