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
- Benchmark subject(s): supplied brand/model(s), such as Segway Myon and MUXI.
- Model count and selection logic.
- Price currency and tax basis (normally AUD and GST-inclusive retail price where stated).
- Research date and intended decision.
- Required output: CSV/XLSX database, HTML report, or both.

If one essential scope detail is missing, ask one concise question. Otherwise state assumptions and proceed.

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

### Step 3 — Select comparable models

Select models based on use case and architecture, not just broad E-bike category:
- Urban/commuter: riding posture, frame access, comfort, battery, motor, daily utility.
- Utility/fat tyre: payload, rack rating, passenger options, tyres, frame and braking.
- Cargo/family: gross system weight, rated payload, rack capacity, child/passenger compatibility and accessories.
- MTB/trekking: drive system, torque, suspension, drivetrain, brakes and intended terrain.

Separate direct competitors from functional and aspirational benchmarks. Explain why each model is included. Do not force unlike products into a single ranking.

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
- Which fields the source supports.

Use model-specific product pages rather than homepages. Keep source links next to the facts they support. Never invent URLs or citations.

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

### Step 6 — Validate and resolve conflicts

For every important field:
- Check that the source refers to the same model year and market version.
- Check units and whether the figure is rated, peak, nominal, maximum, or estimated.
- Compare official and retailer values.
- Record conflicts instead of silently selecting one.
- Give each field a confidence grade:
  - A: current official Australian product/specification source.
  - B: official global source or verified Australian distributor/retailer.
  - C: reputable independent source or retailer with incomplete provenance.
  - D: unverified secondary claim; do not use as a firm comparison fact.

Keep source confidence separate from value type (manufacturer claim, independently tested, calculated, observed retail price, estimate, hypothesis).

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

### Step 9 — Generate insights

For each insight use:
- Evidence: observed, sourced fact.
- Interpretation: what the comparison indicates.
- Implication for the subject product.
- Recommended action or further validation.
- Confidence: High / Medium / Low.

Analyze:
- Specification advantages and disadvantages.
- Price-to-specification positioning, with caveats.
- Segment fit and product architecture.
- Feature gaps and differentiation.
- Australian compliance and service risks.
- Data gaps that could change the conclusion.

Do not infer market share, sales, popularity, or sell-through from the number of models or retailer listings.

## Standard deliverables

### A. Brand & Model Database
One row per model. Include identity, product segment, Australian availability, price, key specs, source URLs, access date and confidence.

### B. Technical Specification Comparison
Models as columns or rows, depending on readability. Include units in field names and retain missing-value labels. Split by segment where necessary.

### C. Competitive Analysis HTML
A single self-contained HTML file with:
- Executive summary.
- Subject product profiles.
- Competitor profiles and comparison tables.
- Filter/search controls where useful.
- Price and specification charts only when data is comparable.
- Australian regulatory considerations.
- Product positioning and opportunities.
- Source register, access dates, limitations and assumptions.

Embed CSS and JavaScript. Avoid external dependencies. Make it responsive and printable.

### D. Research log
Record search date, queries, source URLs, models included/excluded, unresolved conflicts and next validation tasks.

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

## Example use

"Compare Segway Myon and MUXI with 30 relevant E-bikes sold in Australia. Cover commuter, utility/fat-tyre and cargo segments. Extract official specifications, normalize units, show price and Australian availability, assess state-specific compliance, and deliver a source-linked database plus a self-contained HTML report."

## Relationship to other MKT-Skill modules

- Use `market-analysis-insights` for broader market/customer/channel strategy and management recommendations.
- Use this module for product discovery, technical specification research, model-level benchmarking and product comparison.
