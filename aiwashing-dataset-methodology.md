# AI-washing dataset: methodology

Reviewed October 18, 2026. Version 2.0. Contains 30 company or business-operation records.

## Purpose and selection

This dataset supports the stock-market and cross-industry research in `aiwashinginfo.html`. It is a purposive sample of documented claims, not a random sample, prevalence estimate, investment recommendation, or list of 30 proven frauds.

A record is included when a source identifies a concrete claim about AI use, autonomy, performance, or an AI-linked business outcome and supplies evidence that the claim was false, misleading, overstated, or unsupported. Product shortcomings, poor investment returns, layoffs, an AI-themed name, or bankruptcy alone are insufficient.

The broad definition includes unsupported earnings promises associated with purported AI-powered services. Those cases need not establish that AI technology was absent. The `limitations` field preserves that distinction.

## Evidence and uncertainty

- Regulatory findings / settlement: an agency order records findings; parties may settle without admitting or denying them.
- Criminal guilty plea / sentencing: an individual pleaded guilty and was sentenced. This does not establish liability of every employee or affiliate.
- Regulatory settlement: an agreement addresses agency allegations; settlement is not a trial verdict.
- Proposed regulatory settlement: the cited source describes proposed terms, not proof of subsequent court entry.
- Regulatory or criminal allegations: a complaint or indictment provides specific allegations that remain allegations in this dataset.
- Court default judgment: a court entered findings against a defendant who defaulted; this is not a contested trial verdict.
- Advertising self-regulation: an industry body evaluated advertising. This is not a government enforcement ruling. Apple's entry concerns historical availability claims, not a conclusion that its AI does not exist.
- Reported / disputed: journalism supports a plausible pattern, with management's response included. Builder.ai and ScaleFactor are included on this basis.

Assessment labels describe the basis for inclusion, not numerical probabilities. All “why AI washing” explanations are editorial synthesis of the linked sources. Sources include SEC, FTC, DOJ, CFTC, Montana securities-regulator documents, and a BBB National Programs advertising decision. Builder.ai uses Rest of World reporting and ScaleFactor uses Forbes reporting, with management's responses retained.

Dates describe the cited event or publication. They do not necessarily describe when the conduct occurred. `reviewed_on` records when sources were examined, not certification that every possible subsequent court filing was searched. For Click Profit the source event has month precision (`2025-08`); other dates use day precision. The CSV preserves dates as text.

## Unit of analysis and deduplication

Each record is a company/operation, rather than a lawsuit, individual defendant, or news story. Delphia and Global Predictions have separate records because they are separate firms with separate orders. Rimar's related entities are grouped. FBA Machine and Passive Scaling are one operation. Builder.ai and Engineer.ai are one operation. Automators, its former Empire Ecommerce name, and Onyx Distribution are grouped; Ecommerce Empire Builders is a different operation.

Cryptoaiml and TSAI Pro are separate operations charged in separate complaints in one September 2026 announcement. Each operation's related entities remain grouped. Destiny Robotics' company and CEO, and Mirror Trading International and its CEO, each form one record.

## Fields

| Field | Meaning |
| --- | --- |
| id | Stable identifier AW001–AW030 |
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
| chart | Structured quantitative evidence for the case: title, metric_type, unit, axis_max, points, headline, interpretation, caveat, source_date, sources |

Market categories are analytical groupings for this dataset, not current exchange-listing certifications. “Public issuer” refers to the relevant historical context. “Investment” identifies advisory/trading services, not necessarily exchange-listed firms. “Private fundraising” covers the fundraising context of the identified case. “Other” does not assert that a company has never raised capital.

JSON stores sources as objects. CSV flattens them into a single field separated by ` | `. Both files contain the same 30 records and fields. The HTML displays these records without requiring a server; JavaScript only adds filtering and expansion controls. Downloads always contain the full dataset.

## Quantitative panels and exports

Every case has a sourced panel. The 30 panels contain 39 numeric observations. These are selected available measurements, not a standardized severity score.

- JSON preserves the `chart` object. The main case CSV serializes it as JSON in a quoted `chart` field.
- `aiwashing-case-metrics.csv` has one observation per row, linked by `case_id`. It includes label, numeric value, display text, qualifier, unit, axis maximum, source date, evidence status, caveat, and direct source URL.
- `value` is the number used to draw the bar. `qualifier` is `exact`, `rounded`, `approximate`, `at_least`, or `greater_than`. A lower-bound bar plots the stated bound, not an invented exact total; its visible label retains the inequality.
- All bars use linear scales beginning at zero. Axis maxima vary and are displayed. Blue and green distinguish rows, not favorable and unfavorable outcomes. Values remain readable without color or JavaScript.
- Currency is nominal USD as stated in the source. No inflation adjustment or contemporary bitcoin conversion is performed. Funding, revenue, losses, penalties, restitution, and judgments must not be summed or treated as interchangeable.
- Suspended judgments are labeled as such. An order requiring payment does not establish collection or recovery.
- Claim-only data are labeled explicitly. Builder.ai's 80% is an advertised claim; its comparable measured rate is unknown. Unknown values are never encoded as zero.
- Workado's 45-percentage-point gap is 98 minus 53. YieldTrust's 2× lockup is 30 divided by 15. Rimar's combined penalties sum to $310,000; NGL's components sum to $5 million; the two Mirror Trading components sum to $3,467,676,744, displayed as $3.47 billion.
- Presto's observations concern different product versions and periods. Evolv's false-alarm observation concerns one school and setting. Click Profit's store restrictions are business outcomes, not model accuracy.
- Apple's 5 and 3 are editorial counts of explicitly named feature examples in the cited NAD announcement, not a vendor-wide failure rate. The five examples are Priority Notifications, Image Playground, Genmoji, Image Wand, and ChatGPT integration. The three Siri capabilities are onscreen awareness, personal context, and cross-app actions.
- `chart.source_date` identifies the numerical source event, which may differ from the case's later settlement date. Status labels summarize the cited record; the dataset does not certify every later docket development.

The selected cases are not statistically representative. Neither chart lengths nor the number of records per sector establish prevalence or relative societal harm.

## Exclusions and limits

Innodata is discussed as an exclusion in the page. The April 27, 2026 court opinion dismissed the operative complaint and noted closure of SEC and DOJ investigations without enforcement action. The allegation alone is not an adequate basis to list it as likely misconduct. Source: https://law.justia.com/cases/federal/district-courts/new-jersey/njdce/2:2024cv00971/540684/58/

Amazon Just Walk Out is not included: acknowledged human review does not itself substantiate the viral claim that the technology was fake. General AI harms and misconduct not involving a misleading AI claim are also outside this selection.

The sample overrepresents U.S. enforcement and e-commerce business opportunities because those have accessible primary records. It cannot establish which industries have the most AI washing. It contains historical records plus 2026 developments; it is not a 2026-only dataset.

## Updating

For consumer-service claims, review the FTC Legal Library and news feeds. For public-company claims, compare EDGAR filings with SEC enforcement records. Preserve the exact claim and source date, check for later orders or corrections, retain counterevidence, and update an existing record instead of counting a settlement as a new case. Keep the JSON, case CSV, metric CSV, and HTML records synchronized.
