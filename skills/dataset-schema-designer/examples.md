# Dataset Schema Designer Skill — Examples

## Example 1: Generic Academic
**Input:** Schema for clinical trial patient data (2024, multi-site, required: demographics, outcomes, adverse events). Include validation rules, schema risks, harmonization notes, and QA Validation Block.
**Output:**
- Field table (name, type, description, units, required/optional, validation rules)
- Metadata section (site, protocol version, provenance, versioning)
- Missing data policy (reporting, imputation)
- Schema risks (e.g., inconsistent site reporting)
- Harmonization considerations (multi-site alignment)
- QA Validation Block (machine-readable)

## Example 2: Biomechanics
**Input:** Schema for motion capture data in gait analysis (adult athletes, 2023–2024, 100Hz sampling, field/lab). Include downstream analysis implications and validation rules.
**Output:**
- Structured fields (e.g., "Joint Angle", "Force Plate Reading"), units, value ranges, validation rules
- Metadata (sensor type, calibration date, provenance)
- Missing data policy (acceptable gaps, handling)
- Downstream analysis implications (e.g., feature extraction constraints)
- QA Validation Block

## Example 3: QAI-Style Applied
**Input:** Schema for multi-sensor wearable data in soccer (10 sensors, 2024, outdoor, harmonization with lab data required). Include schema risks, harmonization, and QA Validation Block.
**Output:**
- Field definitions (sensor type, timestamp, measurement, units, validation rules)
- Metadata (harmonization notes, provenance, versioning)
- FAIR compliance notes and missing data policy
- Schema risks (sensor drift, time sync)
- Harmonization considerations (lab/field alignment)
- QA Validation Block
