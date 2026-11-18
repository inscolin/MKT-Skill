---
name: australia-ebike-research
description: Research the Australian electric bicycle market and benchmark E-bike products. Use to discover Australian brands and models, extract and normalize product specifications, compare competitors, assess price positioning and Australian regulatory fit, and produce evidence-traceable Excel/CSV and HTML reports.
---

# Australia E-bike Research

## Purpose

Create a repeatable, evidence-led research workflow for the Australian E-bike market. The primary deliverable is a structured product benchmark database that can be updated as brands, models, prices, and regulations change.

This is an independent module in MKT-Skill. It can be used alone or alongside the broader `market-analysis-insights` skill. Use this skill for product-level research; use the broader skill when the task expands into customer research, market sizing, channel strategy, or commercial recommendations.

## Core workflow

**Scope → Market/brand discovery → Model selection → Source collection → Specification extraction → Normalization → Validation → Feature matrix → Competitive insights → Deliverables**

### Step 1 — Define the research scope

Capture:
- Geography: Australia nationally, or named state/territory.
- Product scope: all E-bikes or selected types (urban/commuter, trekking, MTB, folding, cargo/utility, fat tyre, family).
- Benchmark subject(s), such as Segway Myon and MUXI.
- Model count and selection logic.
- Price currency and tax basis (normally AUD and GST-inclusive retail price where stated).
- Research date and intended decision.
- Required output: CSV/XLSX database, HTML report, or both.

If one essential scope detail is missing, ask one concise question. Otherwise state assumptions and proceed.

Before collecting specifications, write a short scope note that locks:
1. Included segments and target number of models per segment.
2. Direct competitors versus functional or aspirational benchmarks.
3. Australian-market inclusion rule.
4. Model-year/version rule.
5. Price observation date and GST basis.
6. Research cut-off date.

Do not silently change the cohort during research. If a model must be replaced, record the original model, reason for replacement, replacement model, and date in the research log.

### Step 2 — Discover Australian brands and models

Build a candidate longlist from:
1. Australian brand/manufacturer websites.
2. Official Australian distributors and authorized retailers, where the relationship is verifiable.
3. Specialist E-bike retailers with detailed product listings.
4. Relevant industry sources and reputable reviews for discovery only.

Classify each candidate by:
- Brand owner / manufacturer / importer / distributor / retailer (do not conflate them).
- Product type and use case.
- Australian availability evidence: official local store, authorized retailer, retailer listing, pre-order, discontinued, or unverified.
- Direct, functional, premium, price-led, or adjacent benchmark relative to the subject product.

A product appearing on a retailer site does not by itself prove exclusivity, official distribution, sales volume, or market leadership.

Use directories and aggregators to discover candidate models, not as the sole evidence for final specifications. A directory listing does not establish current stock, authorized distribution, exact Australian configuration, or market share.

For every shortlisted model, assign one availability status:
- **Confirmed — official Australia:** current Australian brand/manufacturer page or official Australian catalogue.
- **Confirmed — authorized channel:** current Australian distributor or retailer listing with verifiable authorization.
- **Listed — retailer evidence:** current Australian retailer listing, authorization not established.
- **Historical/discontinued:** credible evidence the model was previously sold in Australia but is no longer currently listed.
- **International benchmark only:** no adequate evidence of Australian sale; retain only if useful and label clearly.
- **Unverified:** Australian availability has not been established.

### Step 3 — Select comparable models

Select models based on use case and architecture, not just broad E-bike category:
- Urban/commuter: riding posture, frame access, comfort, battery, motor, daily utility.
- Utility/fat tyre: payload, rack rating, passenger options, tyres, frame and braking.
- Cargo/family: gross system weight, rated payload, rack capacity, child/passenger compatibility and accessories.
- MTB/trekking: drive system, torque, suspension, drivetrain, brakes and intended terrain.

Separate direct competitors from functional and aspirational benchmarks. Explain why each model is included. Do not force unlike products into a single ranking.

For a multi-segment benchmark, maintain the agreed segment quota and identify the comparison group for each model. Do not compare cargo-bike gross system weight with commuter-bike rider payload as if they were identical.

### Step 4 — Collect sources

Prioritize:
1. Official Australian brand/model product page and downloadable specification sheet.
2. Official Australian distributor or authorized retailer listing.
3. Manufacturer's global product page, clearly flagging market/version differences.
4. Reputable specialist retailer or technical review.
5. General retailer listings, forums and user reports as secondary evidence.

For every model, record:
- Exact source title and direct URL.
- Source type and publisher.
- Date accessed and visible publication/update date, if available.
- Market/version represented (Australia, global, US, EU, etc.).
- Model year or generation, where available.
- Which fields the source supports.
- Whether the source is current, archived, or a cached/search-result-only reference.

Use model-specific product pages rather than homepages. Keep source links next to the facts they support. Never invent URLs or citations.

Maintain a source register with one row per source, not merely one URL per model. A single model may require separate sources for price, battery, motor, payload, warranty, and compliance. Record the field(s) supported by each source.

Do not treat a search-result snippet as equivalent to opening and checking the underlying page. If a page is inaccessible, record that limitation and do not imply that its full contents were verified.

### Step 5 — Extract and normalize specifications

Use the schema in `references/specification-schema.md`. Preserve the source's original wording and value in addition to normalized values when ambiguity is possible.

Normalization rules:
- Battery energy: Wh. If only voltage and amp-hours are given, calculate Wh = V × Ah and mark as calculated.
- Battery capacity: Ah; retain voltage separately.
- Motor power: distinguish continuous/rated power from peak/maximum power.
- Torque: Nm; do not infer torque from motor wattage.
- Range: km; preserve the manufacturer's test conditions and mode if stated.
- Weight: kg; distinguish bike weight, battery-included weight, and accessories.
- Payload: distinguish rider limit, rack limit, gross vehicle/system weight, and total payload.
- Speed: km/h; distinguish assisted cut-off from throttle-only speed and maximum mechanical speed.
- Price: AUD; record list price, current promotional price, date, GST status if known, and whether accessories/delivery are included.
- Wheel/tyre size: preserve inch and metric notation where useful.
- Components: record exact brand/model only when explicitly supported.

Do not convert an unknown field into an estimate. Use `Not disclosed`, `Not found`, `Not applicable`, or `Conflicting sources` as appropriate.

For each extracted field, retain these separate attributes:
- **Raw value:** exactly as stated in the source.
- **Normalized value:** converted to the agreed unit, if conversion is valid.
- **Value type:** manufacturer claim, independently tested, calculated, observed retail price, or other clearly defined type.
- **Source reference:** source-register ID or direct URL.
- **Market/version:** the market and model variant the evidence refers to.
- **Confidence grade:** A/B/C/D, as defined in Step 6.
- **Notes:** test conditions, definition, caveat, or unresolved ambiguity.

Never fill a missing Australian specification using a different regional model without an explicit cross-market equivalence statement. If a US/EU manual is used as a reference, label the value as that market's specification and do not present it as an Australian specification.

### Step 6 — Validate and resolve conflicts

For every important field:
- Check that the source refers to the same model year and market version.
- Check units and whether the figure is rated, peak, nominal, maximum, or estimated.
- Compare official and retailer values.
- Record conflicts instead of silently selecting one.
- Give each field a confidence grade:
  - **A:** current official Australian product/specification source.
  - **B:** official global source or verified Australian distributor/retailer.
  - **C:** reputable independent source or retailer with incomplete provenance.
  - **D:** unverified secondary claim; do not use as a firm comparison fact.

Keep source confidence separate from value type (manufacturer claim, independently tested, calculated, observed retail price, estimate, hypothesis).

Apply the following validation checks:
1. **Identity check:** exact model name, generation, model year, and SKU/variant where available.
2. **Market check:** Australian versus US/EU/global configuration is explicit.
3. **Unit check:** units and conversions are correct; calculated values are labelled.
4. **Definition check:** rated versus peak power, claimed versus tested range, bike weight versus packaged weight, rider limit versus total payload, and rack limit versus total payload are not conflated.
5. **Freshness check:** price and availability are current as of the recorded access date.
6. **Conflict check:** conflicting sources remain visible in a conflict log with the selected treatment and reason.
7. **Traceability check:** every material numeric comparison has a source reference or is explicitly marked calculated.

Do not award grade A merely because a source uses an official-looking logo. Confirm that it is the official Australian page or document and that it refers to the relevant variant. A global manufacturer page is normally grade B for an Australian-market claim unless it explicitly establishes Australian configuration.

When sources disagree, do not average the values. Prefer the source that best matches the exact market, variant, and model year; retain the alternative value and explain the decision. If the discrepancy cannot be resolved, use `Conflicting sources`.

### Step 7 — Build the feature matrix

Create two views:
1. **Full specification matrix:** all models, all relevant fields, source traceability.
2. **Decision matrix:** a smaller set of comparable decision criteria by segment.

Use separate comparison groups when product types differ. Do not compare cargo-bike gross system weight with commuter-bike rider payload as if they were identical.

Recommended fields:
- Brand, model, model year, product type, use case, Australian availability.
- Current/list/promotional price (AUD).
- Motor type, brand, continuous rated power, peak power, torque, drive position.
- Battery voltage, Ah, Wh, chemistry if disclosed, removable/integrated.
- Claimed range, test conditions, assist cut-off speed.
- Weight, rider limit, total payload, rear/front rack rating.
- Frame material, frame style, wheel/tyre size.
- Fork/rear suspension, drivetrain/gears, brakes, display, lights.
- Warranty, service footprint, safety/certification claims.
- Source URLs, access date, confidence, caveats.

Every comparison table must display units in the field label or column heading. Mark unavailable data with the standard missing-value labels; do not leave ambiguous blank cells. Include a legend explaining all missing-value labels and confidence grades.

Only calculate ratios or rankings from comparable fields with consistent definitions. If comparability is partial, disclose the limitation and avoid presenting a precise rank as definitive.

### Step 8 — Assess Australian regulatory fit

Do not assume US Class 1/2/3 or EU EPAC labels automatically establish Australian road legality.

Research current requirements for the target state/territory and distinguish:
- Motor continuous rated power versus peak power.
- Pedal-assist versus throttle operation.
- Assistance cut-off speed.
- Applicable product standards and conformity evidence.
- Import/product safety obligations versus public-road use rules.
- State/territory road-use rules, age rules, helmet rules and local restrictions.

Use current official Australian Government, state/territory government, regulator, and standards-body sources. Record source date and effective date. If requirements vary or transition periods apply, explain the scope and dates. Do not provide legal advice; flag unresolved compliance questions for confirmation by the importer or regulator.

Regulatory conclusions must be jurisdiction- and date-specific. Do not generalize one state's rules to all of Australia. Distinguish a product safety standard, a market/import requirement, and a road-use rule; they are not interchangeable.

A manufacturer's claim such as `250 W`, `EN 15194`, or `EPAC` is not by itself proof of compliance. Seek the relevant test report, declaration, conformity documentation, permanent label, or regulator guidance where applicable. If documentary evidence is absent, state `Compliance evidence not verified` rather than declaring the product compliant or non-compliant.

### Step 9 — Generate insights

For each insight use:
- **Evidence:** observed, sourced fact.
- **Interpretation:** what the comparison indicates.
- **Implication for the subject product.**
- **Recommended action or further validation.**
- **Confidence:** High / Medium / Low.

Analyze:
- Specification advantages and disadvantages.
- Price-to-specification positioning, with caveats.
- Segment fit and product architecture.
- Feature gaps and differentiation.
- Australian compliance and service risks.
- Data gaps that could change the conclusion.

Do not infer market share, sales, popularity, or sell-through from the number of models or retailer listings.

Separate factual findings from interpretation and hypotheses. Do not turn a missing competitor specification into a product advantage. If a conclusion depends on incomplete or non-comparable data, state that dependency next to the conclusion.

## Standard deliverables

### A. Brand & Model Database

One row per model. Include identity, product segment, Australian availability, price, key specs, source URLs, access date and confidence.

### B. Technical Specification Comparison

Models as columns or rows, depending on readability. Include units in field names and retain missing-value labels. Split by segment where necessary.

### C. Competitive Analysis HTML

A single self-contained HTML file with:
- Executive summary.
- Research scope, cut-off date, and cohort selection logic.
- Subject product profiles.
- Competitor profiles and comparison tables.
- Filter/search controls where useful.
- Price and specification charts only when data is comparable.
- Australian regulatory considerations.
- Product positioning and opportunities.
- Source register, access dates, limitations and assumptions.
- Clear distinction between verified facts, manufacturer claims, calculated values, and hypotheses.

Embed CSS and JavaScript. Avoid external dependencies. Make it responsive and printable.

### D. Research log

Record search date, queries, source URLs, models included/excluded, unresolved conflicts and next validation tasks.

### E. Validation and issue log

Record:
- Models with no adequate Australian availability evidence.
- Fields supported only by global or non-Australian sources.
- Conflicting values and their resolution status.
- Missing primary sources.
- Regulatory evidence gaps.
- Failed or inaccessible URLs.
- Follow-up actions, owner if known, and status.

## Research status and draft-delivery rules

Use an explicit status for the overall research and for each model:
- **Not started**
- **Discovery complete**
- **Sources collected**
- **Extraction complete**
- **Validation complete**
- **Ready for comparison**
- **Final checked**

Do not mark the whole research as complete merely because the target number of candidate models has been found or a preliminary table has been assembled.

A **Research Draft** may be delivered before all validation is complete, but it must:
1. Be labelled `DRAFT` prominently in the file name and report header.
2. State the research cut-off date and the actual completion status.
3. Separate verified data from preliminary, unverified, and missing data.
4. Include a list of models and fields still requiring validation.
5. Avoid definitive market, compliance, or product-positioning conclusions that are not supported by the evidence.
6. Never imply that a planned deliverable has been generated when it has not.

A **V1.0 Final** may be declared only after the quality gates below are met, the agreed model cohort has been checked, and both requested output files have been opened and checked for completeness and usability. If a requirement cannot be met, report the limitation and retain Draft status.

When reporting progress, give counts where possible: number of models selected, number with Australian availability confirmed, number with primary sources, number with validation complete, and number still pending. Do not describe an approximate or discovery-only cohort as a fully validated competitor set.

## Quality gates before delivery

- Every benchmark model has evidence of Australian availability or is explicitly labelled as an international/aspirational benchmark.
- Every displayed numeric specification has a source or is explicitly labelled calculated.
- Rated and peak motor power are not conflated.
- Range claims are labelled manufacturer-claimed unless independently tested.
- Weight and payload definitions are explicit.
- Price has a date and source.
- Regulatory statements link to current official sources and specify jurisdiction.
- Missing values are not guessed.
- Conflicting values are visible.
- Conclusions distinguish facts, interpretation and hypotheses.
- Deliverables include a limitations section.
- Every model has an explicit research status and source trail.
- The model cohort matches the agreed scope, or all deviations are logged.
- Draft versus final status is stated accurately.
- XLSX/CSV and HTML files requested by the user have actually been generated and checked before being described as delivered.

## Example use

"Compare Segway Myon and MUXI with 30 relevant E-bikes sold in Australia. Cover commuter, utility/fat-tyre and cargo segments. Extract official specifications, normalize units, show price and Australian availability, assess state-specific compliance, and deliver a source-linked database plus a self-contained HTML report."

## Relationship to other MKT-Skill modules

- Use `market-analysis-insights` for broader market/customer/channel strategy and management recommendations.
- Use this module for product discovery, technical specification research, model-level benchmarking and product comparison.
