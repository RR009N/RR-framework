# Admin Guide

This guide is for consultants, maintainers, and model administrators.

## Maintenance principles

When changing the workbook, preserve:

- Stable Question IDs.
- License and attribution notices.
- The layer separation and naming convention (`_DATA_*`, `_ENGINE_*`, `_CONFIG_*`, `_REF_*`).
- Sheet protection / visibility for backend and engine sheets.
- Workbook formulas, structured tables, and named references.
- Standards mapping.
- Risk and recommendation linkages.
- Version history.

## Where things live (v2.0)

- Tunable parameters: `_CONFIG_Model_Settings`, `_CONFIG_Risk_Calibration` (single source of truth).
- Reference content (industry templates, vocabularies): `_REF_Model_Content`, `_DATA_Mappings`.
- Calculation engines (very hidden): `_ENGINE_Risk`, `_ENGINE_Crisis`, `_ENGINE_Strategy`, `_ENGINE_Initiatives`, plus `_ENGINE_Fuzzy_Posture`.
- Normalized data: `_DATA_Assessment_Model`, `_DATA_Dashboard_Facts`.

## Working with structured tables

The initiative and strategy lists are native Excel Tables (`tblInitiatives` on `_ENGINE_Initiatives`, `tblStrategy` on `_ENGINE_Strategy`). To extend them, type into the row directly beneath the table: Excel grows the table and copies the column formulas automatically. Do not leave a blank row between the table and new data, or the auto-extend breaks.

`_ENGINE_Risk` is not yet a Table (its header row still has unlabeled calculation columns). Define those headers before converting it; until then, extend its ranges manually and check downstream references.

## Adding a question

1. Assign a unique Question ID.
2. Place it in the correct domain and subdomain.
3. Define score criteria.
4. Add standards mapping where applicable.
5. Define process maturity, digitalization, and resilience relevance.
6. Map the question to risk categories.
7. Map score-based recommendations in `_DATA_Mappings`.
8. Check whether it affects strategy packages or initiatives.
9. Update data-quality logic if needed.
10. Document the change in Version History and CHANGELOG.md.

## Adding an industry template

1. Add the industry name to the profile list.
2. Define domain weights.
3. Define target maturity levels.
4. Define criticality multipliers.
5. Define crisis exposure multipliers.
6. Define relevant critical systems.
7. Define preferred strategies.
8. Validate that the AS-IS view and action plan update correctly.

## Adding a crisis scenario

1. Add the scenario to the crisis scenario list in `_ENGINE_Crisis`.
2. Define domain-level impact multipliers.
3. Define crisis-to-crisis coupling where relevant.
4. Map the scenario to risk categories, strategy packages, and initiatives.
5. Test selection on **Resilience & Risk Scenario**.
6. Update CRISIS_SCENARIOS.md.

## Adding a strategy or initiative

1. Add a row directly beneath `tblStrategy` (`_ENGINE_Strategy`) or `tblInitiatives` (`_ENGINE_Initiatives`); the table auto-extends.
2. Assign a unique ID (STR-xx / INI-xx) and complete the row.
3. Confirm linkages to domains, risks, and recommendations.
4. Validate that the action plan and roadmap update correctly.

## Updating risk logic

- Keep risk names clear and executive-readable.
- Link risks to domains and relevant questions.
- Avoid duplicate risk names with slightly different wording.
- Check that low maturity creates a meaningful risk event.
- Ensure treatment actions connect to recommendations or initiatives.

## Updating recommendations

Recommendations should be action-oriented and next-level focused.

Bad example:

> Improve CRM.

Better example:

> Assign a CRM owner, define mandatory pipeline stages, enforce opportunity update rules, and review pipeline hygiene monthly.

## Validation checklist

Before releasing a new version:

- Open the workbook in Microsoft Excel desktop; confirm no repair prompt.
- Check the visible workflow sheets.
- Scan for formula errors (target: zero `#REF!`).
- Test Company Profile dropdowns.
- Test crisis scenario selection on Resilience & Risk Scenario.
- Confirm AS-IS Assessment updates.
- Confirm Action Plan & Roadmap (recommendations, WSJF, waves) updates.
- Confirm the three structured tables (`RecommendationMatrixTable`, `tblInitiatives`, `tblStrategy`) are intact and sized correctly.
- Confirm the workbook still contains attribution metadata.
- Update Version History and CHANGELOG.md.
- Generate a new checksum (`releases/checksums.txt`).
