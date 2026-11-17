# E-bike Specification Schema

Use this schema as the canonical field dictionary for Australian E-bike research. Keep source-original values alongside normalized values wherever possible.

## 1. Product identity

| Field | Definition / rule |
|---|---|
| brand | Consumer-facing brand name |
| model | Exact model name and trim |
| model_year | Model year only when stated |
| sku_or_variant | Exact SKU, size, battery or regional variant |
| product_type | Urban, commuter, trekking, MTB, folding, cargo, utility, fat tyre, etc. |
| use_case | Intended riding scenario |
| market_version | Australia, EU, US, global, etc. |
| australian_availability | Official AU store / authorized retailer / retailer listing / preorder / discontinued / unverified |
| manufacturer | Actual manufacturer if verifiable |
| importer_distributor | Australian importer/distributor if verifiable |
| retailer | Seller, not automatically the brand distributor |

## 2. Price and commercial fields

| Field | Unit / rule |
|---|---|
| list_price_aud | AUD; record GST basis if known |
| current_price_aud | Observed price at access date |
| promotional_price_aud | Promotional price, with campaign/date |
| price_accessory_included | Yes / No / unclear |
| delivery_included | Yes / No / unclear |
| price_source_url | Direct product/retailer URL |
| price_access_date | YYYY-MM-DD |

## 3. Motor and drive system

| Field | Unit / rule |
|---|---|
| motor_brand_model | Exact motor brand/model if disclosed |
| motor_position | Front hub / rear hub / mid-drive / other |
| motor_type | Hub / direct-drive hub / geared hub / mid-drive / other |
| rated_continuous_power_w | Continuous/rated output; never substitute peak |
| peak_power_w | Peak/maximum power, if disclosed |
| torque_nm | Nm; no inference from watts |
| assist_cutoff_kmh | Pedal-assist cut-off speed |
| throttle_type | None / thumb / twist / other / unclear |
| sensor_type | Cadence / torque / speed / combined / not disclosed |

## 4. Battery and charging

| Field | Unit / rule |
|---|---|
| battery_voltage_v | V |
| battery_capacity_ah | Ah |
| battery_energy_wh | Wh; calculated V × Ah only if both inputs are known |
| battery_energy_method | Manufacturer stated / calculated |
| battery_chemistry | Only if disclosed |
| battery_location | Downtube / integrated / rear rack / other |
| battery_removable | Yes / No / unclear |
| charger_output | V and A if disclosed |
| charging_time_h | Hours; note conditions |
| battery_safety_certification | Exact certification and scope, if evidenced |

## 5. Performance

| Field | Unit / rule |
|---|---|
| claimed_range_km | Manufacturer-claimed range |
| range_test_conditions | Mode, rider weight, terrain, temperature, etc. |
| independently_tested_range_km | Only for a cited independent test |
| max_assisted_speed_kmh | Assist limit, not generic maximum speed |
| climbing_claim | Preserve original claim; normalize only with clear method |
| ip_rating | Exact IP rating |

## 6. Frame, wheels and components

| Field | Unit / rule |
|---|---|
| frame_material | Aluminium, steel, carbon, etc. |
| frame_style | Step-through, step-over, compact, cargo, etc. |
| frame_sizes | Exact sizes |
| bike_weight_kg | Clarify battery/accessory inclusion |
| wheel_size_in | Inches |
| tyre_size | Preserve exact notation, e.g. 20 × 4.0 |
| front_suspension | Fork brand/model/travel if stated |
| rear_suspension | Yes/no and exact details |
| drivetrain | Brand/model |
| gear_count | Number of speeds |
| brake_type | Hydraulic/mechanical; disc/rim |
| brake_model | Exact model if disclosed |
| display | Brand/model/type |
| lighting | Front/rear and integration |
| accessories | Rack, mudguards, kickstand, child seat compatibility, etc. |

## 7. Load, dimensions and utility

| Field | Unit / rule |
|---|---|
| rider_weight_limit_kg | Rider-only limit |
| total_payload_kg | Define whether rider + luggage or other |
| gross_system_weight_kg | Bike + rider + cargo, only when defined |
| rear_rack_limit_kg | Rear rack rating |
| front_rack_limit_kg | Front rack rating |
| passenger_capacity | Only when manufacturer explicitly permits |
| dimensions_mm | Length × width × height, with order stated |
| trailer_compatibility | Only when explicitly supported |

Never treat rider limit, total payload, gross system weight and rack limit as interchangeable.

## 8. Warranty, service and compliance

| Field | Definition |
|---|---|
| frame_warranty | Duration and conditions |
| motor_warranty | Duration and conditions |
| battery_warranty | Duration and conditions |
| australian_service_network | Evidence-based service locations/coverage |
| certification_claim | Exact standard/certificate claim |
| en15194_status | Certified / claimed / not disclosed / not applicable / unverified |
| australian_road_use_status | Confirmed / conditional / unclear / not assessed |
| compliance_jurisdiction | State/territory or national scope |
| compliance_source_url | Official source |
| compliance_checked_date | YYYY-MM-DD |

## 9. Evidence and data governance

For each field, capture:
- source_value
- normalized_value
- unit
- source_url
- source_publisher
- source_type
- access_date
- source_market_version
- confidence_grade (A/B/C/D)
- value_type (manufacturer claim / independently tested / calculated / observed price / estimate / hypothesis)
- notes_or_conflict

### Confidence grades

- A — current official Australian model/specification source.
- B — official global source or verifiable Australian distributor/retailer.
- C — reputable independent source or retailer with incomplete provenance.
- D — unverified secondary source. Do not use as a firm comparison fact.

### Missing values

Use one of:
- Not disclosed
- Not found
- Not applicable
- Conflicting sources
- Pending verification

Never leave a blank if the blank could be mistaken for zero or overlooked data.
