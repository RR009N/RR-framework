# Forms Integration

RR-framework can be extended into a survey-driven workflow using Google Forms, Microsoft Forms, or a custom web application.

## Recommended MVP architecture

```text
Client Admin Setup
→ Domain Forms
→ Response Collection
→ Raw Response Table
→ Normalized Response Table
→ Excel Calculation Workbook
→ Executive Outputs
```

## Recommended form structure

Do not use one huge form for all questions. Use domain-specific forms.

Recommended approach:

- One form per domain.
- One respondent assignment list.
- One normalized response table.
- One final aggregation layer.

## Required response fields

Each form response should include:

- Assessment ID.
- Organization name or ID.
- Respondent email.
- Respondent role.
- Domain.
- Question ID.
- Selected answer.
- Numeric score.
- Evidence confidence, if used.
- Assessor confidence, if used.
- Comment or evidence note.
- Timestamp.

## Question ID principle

Every question must have a stable Question ID. The Question ID connects:

- Workbook question.
- Form question.
- Raw response.
- Normalized response.
- Risk library.
- Recommendation matrix.
- Standards mapping.
- Dashboard calculations.

Example format:

```text
ITCLOUD_Q001
HRWORK_Q014
SUPPLY_Q009
```

## Multiple respondents per domain

If several people answer the same domain, use aggregation logic.

Suggested approach:

```text
Final Question Score = Domain Owner Score * 0.60 + Average Supporting Respondent Score * 0.40
```

For critical controls, use a more conservative rule:

```text
Final Critical Score = MIN(Domain Owner Score, Supporting Average Score)
```

## Disagreement flag

If responses differ significantly, trigger a disagreement flag.

Example:

```text
Disagreement Flag = TRUE if MAX(Responses) - MIN(Responses) >= 2
```

This means the topic should be reviewed in a workshop.

## Evidence gap flag

If a high score is selected but evidence confidence is low, trigger an evidence gap.

Example:

```text
Evidence Gap = TRUE if Score >= 4 and Evidence Confidence = Low
```

## Suggested data tabs for Excel integration

If Forms integration is implemented, add these staging sheets:

- `_DATA_Raw_Responses`
- `_DATA_Normalized_Responses`
- `_DATA_Respondents`
- `_DATA_Assignments`
- `_MAP_Question_Form`
- `_CALC_Response_Aggregation`
- `_CALC_Assessment_Status`

## Microsoft Forms path

Suggested Microsoft-first MVP:

```text
Microsoft Forms → Power Automate → SharePoint List or Dataverse → Excel Power Query → RR-framework outputs
```

## Google Forms path

Suggested Google-first MVP:

```text
Google Forms → Google Sheets or Forms API → normalized CSV/export → Excel import → RR-framework outputs
```

## Product architecture path

For a full application:

```text
Web App → Survey Module → Database → Calculation Engine → Dashboard → Excel/PDF Export
```

Excel can remain a reference model while the calculation engine is migrated to backend services.
