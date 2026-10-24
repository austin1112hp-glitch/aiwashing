# AI-washing dataset: methodology

Expanded October 24, 2026. Version 3.2. Contains 100 company, operation, or specified enforcement-example records. AW001–AW060 retain their original contents and review dates. AW061–AW100 were reviewed October 24.

## Purpose and selection

This dataset supports the stock-market and cross-industry research in `aiwashinginfo.html`, with the full case library in `aiwashingcases.html`. It is a purposive sample of documented claims, not a random sample, prevalence estimate, investment recommendation, or list of 100 proven frauds.

A record is included when a source identifies a concrete claim about AI use, autonomy, performance, or an AI-linked business outcome and supplies evidence that the claim was false, misleading, overstated, or unsupported. Product shortcomings, poor investment returns, layoffs, an AI-themed name, or bankruptcy alone are insufficient.

The broad definition includes unsupported earnings promises associated with purported AI-powered services, misleading AI provenance or affiliation, disputed safety assurances, and corrected performance claims. Intentional deception is not inferred from a correction alone. Those cases need not establish that AI technology was absent. The `limitations` field preserves that distinction.

## Evidence and uncertainty

- Regulatory findings / settlement: an agency order records findings; parties may settle without admitting or denying them.
- Criminal guilty plea / sentencing: an individual pleaded guilty and was sentenced. This does not establish liability of every employee or affiliate.
- Regulatory settlement: an agreement addresses agency allegations; settlement is not a trial verdict.
- Proposed regulatory settlement: the cited source describes proposed terms, not proof of subsequent court entry.
- Regulatory or criminal allegations: a complaint or indictment provides specific allegations that remain allegations in this dataset.
- Court default judgment: a court entered findings against a defendant who defaulted; this is not a contested trial verdict.
- Advertising self-regulation: an industry body evaluated advertising. This is not a government enforcement ruling. Apple's entry concerns historical availability claims, not a conclusion that its AI does not exist.
- Reported / disputed: journalism supports a plausible pattern, with management's response included. Builder.ai and ScaleFactor are included on this basis.

- Regulatory findings / administrative order: a regulator issued an administrative order; it is not a criminal conviction.
- Regulatory allegations / emergency order: emergency administrative action records allegations and risk concerns; no final criminal finding is implied.
- Criminal guilty plea: the identified individual's admissions; other defendants can have different statuses.
- Regulatory findings / corrective action: includes the Tesla DMV marketing finding and the February 2026 announcement that corrective action avoided suspension.
- Company clarification: a company corrected or explained its own marketing language, as in Lemonade.
- Independent research / contested interpretation: a defined product evaluation, not a legal fraud determination. LexisNexis's citation-existence claim is narrower than the study's answer-correctness measure.
- Advocacy complaint / disputed: a complainant's allegations, such as EPIC's HireVue complaint, not an agency finding.
- Independent investigation / disputed and Reported / disputed demonstration: external scrutiny of a historical product or demonstration; limitations and company responses remain material.
- Mixed: guilty plea / allegations: an operation has different procedural statuses for different participants.
- Regulatory commitments / no infringement finding: AGCM accepted commitments without determining an infringement. DeepSeek, Mistral and NOVA are conditional disclosure cases, not established frauds.

Assessment labels describe the basis for inclusion, not numerical probabilities. All “why AI washing” explanations are editorial synthesis of the linked sources. Sources include SEC, FTC, DOJ, CFTC, Montana securities-regulator documents, and a BBB National Programs advertising decision. Builder.ai uses Rest of World reporting and ScaleFactor uses Forbes reporting, with management's responses retained.

Dates describe the cited event or publication. They do not necessarily describe when the conduct occurred. `reviewed_on` records when sources were examined, not certification that every possible subsequent court filing was searched. Click Profit (`2025-08`), Lemonade (`2021-05`) and the Devin demonstration review (`2024-04`) use month precision; other records use day precision. The CSV preserves dates as text.

## Unit of analysis and deduplication

Each record ordinarily represents a company/operation, rather than a lawsuit, individual defendant, or news story. Two disclosed exceptions are the Beijing regulator's anonymized company proceeding and CAC's grouped stock-promotion account example. The latter does not assert common ownership; both are specific published records, not anonymous composite patterns. Delphia and Global Predictions have separate records because they are separate firms with separate orders. Rimar's related entities are grouped. FBA Machine and Passive Scaling are one operation. Builder.ai and Engineer.ai are one operation. Automators, its former Empire Ecommerce name, and Onyx Distribution are grouped; Ecommerce Empire Builders is a different operation.

Cryptoaiml and TSAI Pro are separate operations charged in separate complaints in one September 2026 announcement. Each operation's related entities remain grouped. Destiny Robotics' company and CEO, and Mirror Trading International and its CEO, each form one record.

The five April 2023 DFPI operations are separate businesses despite a shared announcement. Related brands and defendants in the Circle Society/Saffron scheme remain one record; Kagel is not counted separately. Morocoin, Berge, Cirkor and their associated investment clubs are one coordinated scheme, not seven cases. Thomson Reuters' two evaluated tools are one company record. DeepSeek, Mistral and Scaleup/NOVA have separate AGCM proceedings and are separate companies.

## Fields

| Field | Meaning |
| --- | --- |
| id | Stable identifier AW001–AW100 |
| reviewed_on | Research review date |
| company | Entity, grouped operation, or trading name |
| industry | Relevant business sector |
| country | Country / market context for AW061–AW100; may describe operations, advertising jurisdiction or investor exposure rather than headquarters. Unassessed for the original 60. |
| date_basis | Explains what the new record's source date represents, including later developments about historical conduct. Unassessed for the original 60. |
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
| chart | Claim-versus-outcome panel: comparison_type, claimed_benefit, documented_outcome, claimed_value, outcome_value, unit, numeric_availability, gap, gap_unit, caveat, evidence_status, source_date, sources |
| context_data | Previous sourced numerical panel, or null for new records; retained for research context; not displayed as a benefit-versus-output comparison |

Market categories are analytical groupings for this dataset, not current exchange-listing certifications. “Public issuer” refers to the relevant historical context. “Investment” identifies advisory/trading services, not necessarily exchange-listed firms. “Private fundraising” covers the fundraising context of the identified case. “Other” does not assert that a company has never raised capital.

JSON stores sources as objects. CSV flattens them into a single field separated by ` | `. Both files contain the same 100 records and fields. The Cases page displays these records without requiring a server; JavaScript only adds filtering and expansion controls. Downloads always contain the full dataset.

## Claim-versus-outcome panels and exports

Every one of the 100 cases has two labeled evidence blocks: **Claimed benefit** and **Documented outcome**. Outcome statements preserve whether they are findings, allegations, or reporting. A documented outcome can be a failure of substantiation; it does not always mean a measured product failure.

- Workado has the one numerical claim-versus-test comparison in this version: 98% advertised accuracy versus approximately 53% on general-purpose content, an approximate 45-percentage-point difference. The general-purpose test is not a universal product benchmark.
- The other 99 cases show qualitative comparisons with an explicit numerical-data-unavailable notice. Quantitative observations may appear in the text, but they cannot be forced into a matched comparison.
- A numerical gap is calculated only when both sides use a comparable measure. Human-intervention rates, false alarms, store restrictions, and training-data counts are not interchangeable with automation claims, weapons-detection accuracy, profit, or fairness.
- Missing numerical values are JSON `null` and blank CSV cells, never zero. Some claims have a number but lack a measured outcome: Ecommerce Empire Builders' $10,000 per month, Builder.ai's at-least-80% automation claim, and YieldTrust's up-to-2.2% daily return. Their qualifiers remain in the claim text. None is a verified result.
- Nate's alleged effectively-zero automation remains qualitative; it is not encoded as an exact zero.
- JSON stores the active panel in `chart`. The main case CSV serializes `chart` and `context_data` as quoted JSON. Sources are flattened with ` | `.
- `aiwashing-case-metrics.csv` now contains **100 comparison rows**, one per case. Fields include both evidence statements, values where supplied, unit, gap, missing-data explanation, procedural status, source date, caveat, and URLs.
- The previous numerical panels remain under `context_data` in the full JSON and case CSV for traceability. They are not rendered as the active comparisons. Funding, losses, penalties, restitution, and judgments measure context rather than AI output.
- Dates identify the cited records, not a certification of current product performance or every later docket development. Apple's panel concerns the historical availability messaging reviewed in April 2025.
- Blue identifies claims and green identifies documented outcomes. Green does not imply a successful outcome. Workado's bars share a linear 0–100% scale; qualitative cards do not use invented bar lengths or scores.

New claims with ranges or qualifiers remain in the text; they are not encoded as unqualified point estimates. The legal-research studies provide observed error rates but no equivalent promised rate under the same definition. Consequently, they remain qualitative panels. None of the 40 latest additions supplies a defensible matched numerical comparison in the sources used.

The selected cases are not statistically representative, and the panels do not establish industry prevalence or a ranking of harm.

## Exclusions and limits

Innodata is discussed as an exclusion in the page. The April 27, 2026 court opinion dismissed the operative complaint and noted closure of SEC and DOJ investigations without enforcement action. The allegation alone is not an adequate basis to list it as likely misconduct. Source: https://law.justia.com/cases/federal/district-courts/new-jersey/njdce/2:2024cv00971/540684/58/

Amazon Just Walk Out is not included: acknowledged human review does not itself substantiate the viral claim that the technology was fake. General AI harms and misconduct not involving a misleading AI claim are also outside this selection.

The sample overrepresents U.S. enforcement and e-commerce business opportunities because those have accessible primary records. It cannot establish which industries have the most AI washing. It contains historical records plus 2026 developments; it is not a 2026-only dataset.

## Navigation and research scope

Use the Overview and Cases (100) navigation links to switch pages. All case records live in `aiwashingcases.html`; searches and filters operate on all 100 entries. Existing case identifiers AW001–AW060 are preserved. Overview links point to the new page, and old direct case hashes redirect there when JavaScript is enabled.

The additions include U.S. and Italian regulatory documents, DOJ and CFTC records, first-party clarifications, academic evaluation and reporting. Disclosure disputes, advocacy complaints and demonstration controversies are deliberately labeled conditional. Inclusion does not classify every organization as a proven fraud. Historical examples describe the versions and claims cited, not current product performance.

## Updating

For consumer-service claims, review the FTC Legal Library and news feeds. For public-company claims, compare EDGAR filings with SEC enforcement records. Preserve the exact claim and source date, check for later orders or corrections, retain counterevidence, and update an existing record instead of counting a settlement as a new case. Keep the JSON, case CSV, metric CSV, and HTML records synchronized.

## October 24 expansion: 40 records

AW061–AW100 add 40 cases, ordered by descending source-event date. **24 additions have a 2026 source event**; this does not mean all 24 began in 2026. For example, Zillow is a procedural update to older litigation, MTFE is an investigation/recovery update, and the three SAMR affiliation cases use their 2026 publication date because individual penalty dates were not stated. The original 60 were preserved rather than comprehensively re-reviewed.

Country context is supplied for the new 40 only. Search can find these countries, but no country prevalence comparison is justified. The 2026 filter uses source-event year for all records; the additions filter selects AW061–AW100. Downloads always contain all 100 cases.

New statuses include advertising rulings, regulatory warnings, mediated complaints, civil settlements, benchmark-organizer findings, research corrections and program-eligibility decisions. Naver's eligibility decision concerns a specific sovereignty criterion. The three SAMR cases concern service identity or affiliation, including services with genuine AI. Sakana acknowledged a research error. Klarna's disclosure review did not establish fabricated metrics. Samsung's voluntary AI wording changes were not adjudicated. AI Quest's order principally concerns securities registration. Their inclusion is conditional and narrower than a fraud finding.

Cox Media Group, MindSift and 1010 Digital Works are one service record. Privvy and Gateway are one operation. Gold Fun and Angel Guardian are one arrangement. BG Wealth Sharing, DSJ and HQIEX are grouped; unrelated similarly named firms are excluded. The three SAMR firms have distinct proceedings and receive separate records. Unitree is the real manufacturer in the Galgotias provenance controversy, not an accused party.

The new sources include Chinese market and internet regulators, Hong Kong SFC, Philippine SEC, New Zealand FMA, Korea MSIT, UK ASA, US regulators and courts, company statements and original reporting. This improves geographic breadth but does not make the sample representative. Numerical claims without matched measured outcomes stay in text; chart numeric fields remain null.
