# Data Dictionary

This document defines key entities and fields used by RR-framework.

## Core entities

| Entity | Description |
|---|---|
| Organization | Company being assessed. |
| Assessment | One assessment instance for an organization and date. |
| Respondent | Person providing assessment answers. |
| Domain | Business area assessed by the workbook. |
| Subdomain | More specific capability group inside a domain. |
| Question | Assessment item with score criteria. |
| Answer | Response selected by the user. |
| Score | Numeric maturity value, usually 0 to 5. |
| Risk | Potential business risk derived from low maturity or weak controls. |
| Recommendation | Next-level improvement action generated from score and gap logic. |
| Strategy Package | Executive-level group of initiatives and recommendations. |
| Initiative | Practical action or project to improve maturity or resilience. |
| Crisis Scenario | Disruption type used for simulation. |

## Question fields

| Field | Description |
|---|---|
| Question ID | Stable unique identifier. |
| Domain | Main assessment domain. |
| Subdomain | Capability area inside the domain. |
| Question text | Closed or scored assessment question. |
| Score | User-selected maturity score. |
| Weight | Importance of the question. |
| Process relevance | Contribution to process maturity. |
| Digital relevance | Contribution to digitalization. |
| Resilience relevance | Contribution to resilience. |
| Evidence confidence | Confidence based on evidence quality. |
| Assessor confidence | Confidence based on assessor certainty. |
| Comment | Optional clarification or evidence note. |

## Score fields

| Field | Description |
|---|---|
| Raw score | Original 0 to 5 user score. |
| Normalized score | Raw score converted to 0 to 100. |
| Confidence factor | Adjustment based on evidence and assessor confidence. |
| Confidence-adjusted score | Normalized score adjusted for confidence. |
| Industry target | Expected maturity for selected industry. |
| Gap | Difference between target and actual score. |
| Criticality multiplier | Importance of the question, domain, or subdomain for the selected industry. |
| Industry-adjusted gap | Gap adjusted for business criticality. |

## Risk fields

| Field | Description |
|---|---|
| Risk category | Risk grouping such as cyber, workforce, supply chain, finance, legal, safety, or operations. |
| Risk event | Business event that may occur. |
| Risk driver | Weakness or gap creating the risk. |
| Likelihood | Estimated probability level. |
| Impact | Estimated business impact level. |
| Risk score | Combined risk priority indicator. |
| Crisis multiplier | Adjustment under selected crisis scenario. |
| Treatment action | Suggested mitigation or control improvement. |

## Strategy package fields

| Field | Description |
|---|---|
| Strategy package | Executive-level improvement theme. |
| Related domains | Business domains affected. |
| Related risks | Risks reduced by the package. |
| Related initiatives | Initiatives included in the package. |
| Priority score | Calculated package priority. |
| Complexity | Estimated difficulty. |
| Suggested wave | Recommended implementation period. |
| Owner role | Typical accountable role. |

## Forms integration fields

If Forms integration is implemented, each response should include:

- Assessment ID.
- Organization ID.
- Respondent email.
- Respondent role.
- Domain.
- Question ID.
- Selected answer.
- Score.
- Confidence.
- Comment.
- Submission timestamp.
