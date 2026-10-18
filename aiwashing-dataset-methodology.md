# AI-washing dataset: methodology

Reviewed October 18, 2026. Version 1.0. Contains 20 company or business-operation records.

## Purpose and selection

This dataset supports the stock-market and cross-industry research in `aiwashinginfo.html`. It is a purposive sample of documented claims, not a random sample, prevalence estimate, investment recommendation, or list of 20 proven frauds.

A record is included when a source identifies a concrete claim about AI use, autonomy, performance, or an AI-linked business outcome and supplies evidence that the claim was false, misleading, overstated, or unsupported. Product shortcomings, poor investment returns, layoffs, an AI-themed name, or bankruptcy alone are insufficient.

The broad definition includes unsupported earnings promises associated with purported AI-powered services. Those cases need not establish that AI technology was absent. The `limitations` field preserves that distinction.

## Evidence and uncertainty

- Regulatory findings / settlement: an agency order records findings; parties may settle without admitting or denying them.
- Criminal guilty plea / sentencing: an individual pleaded guilty and was sentenced. This does not establish liability of every employee or affiliate.
- Regulatory settlement: an agreement addresses agency allegations; settlement is not a trial verdict.
- Proposed regulatory settlement: the cited source describes proposed terms, not proof of subsequent court entry.
- Regulatory or criminal allegations: a complaint or indictment provides specific allegations that remain allegations in this dataset.
- Reported / disputed: journalism supports a plausible pattern, with management's response included. Builder.ai is the sole entry in this category.

Assessment labels describe the basis for inclusion, not numerical probabilities. All “why AI washing” explanations are editorial synthesis of the linked sources. Sources are primarily SEC, FTC, and DOJ documents; Builder.ai uses original reporting by Rest of World, including former-employee interviews and management's denial.

Dates describe the cited event or publication. They do not necessarily describe when the conduct occurred. `reviewed_on` records when sources were examined, not certification that every possible subsequent court filing was searched. For Click Profit the source event has month precision (`2025-08`); other dates use day precision. The CSV preserves dates as text.

## Unit of analysis and deduplication

Each record is a company/operation, rather than a lawsuit, individual defendant, or news story. Delphia and Global Predictions have separate records because they are separate firms with separate orders. Rimar's related entities are grouped. FBA Machine and Passive Scaling are one operation. Builder.ai and Engineer.ai are one operation. Automators, its former Empire Ecommerce name, and Onyx Distribution are grouped; Ecommerce Empire Builders is a different operation.

## Fields

| Field | Meaning |
| --- | --- |
| id | Stable identifier AW001–AW020 |
| reviewed_on | Research review date |
| company | Entity, grouped operation, or trading name |
| industry | Relevant business sector |
| market_category | Public issuer, Investment, Private fundraising, or Other |
| business_summary | What the business offered in the relevant period |
| ai_claim | Specific AI representation under examination |
| why_ai_washing | Evidence-based rationale for inclusion |
| evidence_status | Type of evidence/procedural posture in the cited record |
| source_event_date | Date of the cited event/publication; not necessarily conduct date |
| assessment | Qualitative strength and conditional nature of the rationale |
| stock_market_connection | Explanation of the connection to securities or fundraising |
| limitations | Qualifications, counterevidence, or management's response |
| sources | Source titles and direct URLs |

Market categories are analytical groupings for this dataset, not current exchange-listing certifications. “Public issuer” refers to the relevant historical context. “Investment” identifies advisory/trading services, not necessarily exchange-listed firms. “Private fundraising” covers the fundraising context of the identified case. “Other” does not assert that a company has never raised capital.

JSON stores sources as objects. CSV flattens them into a single field separated by ` | `. Both files contain the same 20 records and fields. The HTML displays these records without requiring a server; JavaScript only adds filtering and expansion controls. Downloads always contain the full dataset.

## Exclusions and limits

Innodata is discussed as an exclusion in the page. The April 27, 2026 court opinion dismissed the operative complaint and noted closure of SEC and DOJ investigations without enforcement action. The allegation alone is not an adequate basis to list it as likely misconduct. Source: https://law.justia.com/cases/federal/district-courts/new-jersey/njdce/2:2024cv00971/540684/58/

Amazon Just Walk Out is not included: acknowledged human review does not itself substantiate the viral claim that the technology was fake. General AI harms and misconduct not involving a misleading AI claim are also outside this selection.

The sample overrepresents U.S. enforcement and e-commerce business opportunities because those have accessible primary records. It cannot establish which industries have the most AI washing. It contains historical records plus 2026 developments; it is not a 2026-only dataset.

## Updating

For consumer-service claims, review the FTC Legal Library and news feeds. For public-company claims, compare EDGAR filings with SEC enforcement records. Preserve the exact claim and source date, check for later orders or corrections, retain counterevidence, and update an existing record instead of counting a settlement as a new case. Keep the JSON, CSV, and HTML records synchronized.
