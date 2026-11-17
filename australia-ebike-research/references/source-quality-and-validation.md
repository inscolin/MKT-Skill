# Source Quality, Validation and Research Log

## Source hierarchy

1. Australian Government, state/territory regulators, official legislation and standards bodies.
2. Official brand/manufacturer Australian product pages and specification sheets.
3. Official Australian importer/distributor pages where the relationship is verified.
4. Authorized or specialist Australian retailers with model-specific technical detail.
5. Reputable independent tests and established trade publications.
6. General marketplaces, forums, social media and user-generated content.

The hierarchy is a default, not a substitute for judging whether the source directly supports the field.

## Required source record

For each source:
- source_id
- brand/model
- page or document title
- publisher
- exact URL
- source category
- market/version
- published or updated date (if visible)
- access date
- fields supported
- limitations

## Source matching

Before extracting data, confirm:
- Exact model and variant.
- Model year where available.
- Battery option and frame size if relevant.
- Market version (Australian, US, EU, global).
- Whether the page describes a current or discontinued product.

Do not merge specifications from different variants into a synthetic model.

## Conflict handling

When values differ:
1. Preserve each source's original value.
2. Check variant, market, model year and unit.
3. Prefer the source most specific to the Australian product being benchmarked.
4. Keep unresolved differences visible.
5. Set the field status to Conflicting sources.
6. Explain whether the conflict materially affects the comparison.

Never silently average conflicting values.

## Calculations

Permitted calculations must be reproducible and labelled:
- Wh = V × Ah, when both are explicitly stated for the same battery.
- Unit conversions such as lb to kg, miles to km, inches to mm.
- Derived price-per-Wh or similar metrics only when the inputs are comparable and the formula is shown.

Do not derive motor torque from wattage, real-world range from battery size, or legal status from a product class label.

## Retail price capture

Record:
- AUD price as displayed.
- Whether it is list, sale, clearance or bundle price.
- Date accessed.
- GST inclusion if stated.
- Delivery and accessories inclusion if material.
- Retailer name and product URL.

A price snapshot is not a permanent MSRP. Do not describe a retailer price as the manufacturer's RRP unless explicitly supported.

## Availability and channel claims

Use precise labels:
- Brand direct Australia store.
- Official Australian distributor (relationship verified).
- Authorized retailer (authorization evidenced).
- Australian retailer listing (authorization unknown).
- Marketplace listing.
- International benchmark (not confirmed for Australia).

A listing alone does not establish sales, market share, exclusivity or official authorization.

## Research log template

| Date | Query / task | Source URL | Models affected | Fields collected | Open issue |
|---|---|---|---|---|---|
| YYYY-MM-DD | Example: Myon battery specification | https://... | Myon | Battery Wh, V, Ah | Confirm AU variant |

## Final validation checklist

- [ ] Every model has exact identity and market/version.
- [ ] Australian availability is evidenced or clearly labelled unverified.
- [ ] Every numeric comparison value has a direct source or calculation note.
- [ ] Rated continuous and peak power are separate.
- [ ] Claimed and independently tested range are separate.
- [ ] Rider limit, payload, gross system weight and rack rating are separate.
- [ ] Price includes source and access date.
- [ ] Conflicting specifications are shown.
- [ ] No unknown value has been guessed.
- [ ] Compliance claims are linked to current official sources.
- [ ] Findings distinguish fact, interpretation and hypothesis.
