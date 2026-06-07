# Admin Guide

This guide is for consultants, maintainers, and model administrators.

## Maintenance principles

When changing the workbook, preserve:

- Stable Question IDs.
- License and attribution notices.
- Sheet protection for technical sheets.
- Workbook formulas and named references.
- Standards mapping.
- Risk and recommendation linkages.
- Version history.

## Adding a question

When adding a new question:

1. Assign a unique Question ID.
2. Place it in the correct domain and subdomain.
3. Define score criteria.
4. Add standards mapping where applicable.
5. Define process maturity, digitalization, and resilience relevance.
6. Map the question to risk categories.
7. Map score-based recommendations.
8. Check whether it affects strategy packages or initiatives.
9. Update quality control logic if needed.
10. Document the change in Version History and CHANGELOG.md.

## Adding an industry template

When adding a new industry:

1. Add the industry name to the profile list.
2. Define domain weights.
3. Define target maturity levels.
4. Define criticality multipliers.
5. Define crisis exposure multipliers.
6. Define relevant critical systems.
7. Define preferred strategies.
8. Validate that dashboard and strategy outputs update correctly.

## Adding a crisis scenario

When adding a new crisis scenario:

1. Add the scenario to the crisis scenario list.
2. Define domain-level impact multipliers.
3. Map the scenario to risk categories.
4. Map the scenario to strategy packages.
5. Map the scenario to initiatives.
6. Test the Crisis Simulator.
7. Update CRISIS_SCENARIOS.md.

## Updating risk logic

When updating the risk library:

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

- Open workbook in Microsoft Excel desktop.
- Check visible output sheets.
- Scan for formula errors.
- Test Company Profile dropdowns.
- Test Crisis Simulator scenario selection.
- Confirm Dashboard updates.
- Confirm Risk Summary updates.
- Confirm Strategy Packages update.
- Confirm Gantt Roadmap remains readable.
- Confirm workbook still contains attribution footer.
- Update Version History.
- Update CHANGELOG.md.
- Generate new checksum.
