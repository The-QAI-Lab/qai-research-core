# Dataset QA Skill — Examples

## Example 1: Generic Academic
**Input:** QA for clinical trial dataset (2024, schema and QA Validation Block attached, required: demographics, outcomes, adverse events). Include issue severity/impact, root cause analysis, and Feature Risk Block.
**Output:**
- QA report (sections: completeness, consistency, errors, downstream risk)
- Issue list (table: issue, location, severity, impact, recommendation)
- Root cause analysis and remediation priority
- Feature Risk Block (machine-readable)

## Example 2: Biomechanics
**Input:** QA for wearable sensor data in running studies (adult athletes, 2023–2024, schema and QA Validation Block attached). Include blocking/non-blocking classification and downstream risk.
**Output:**
- Completeness check (missing data, sensor calibration)
- Error list (table: error, location, severity, impact, recommendation)
- Blocking/non-blocking classification
- Downstream risk to feature engineering
- Feature Risk Block

## Example 3: QAI-Style Applied
**Input:** QA for multi-sensor soccer dataset (10 sensors, 2024, harmonization with lab data required, schema and QA Validation Block attached). Include root cause analysis, remediation priority, and Feature Risk Block.
**Output:**
- Structured QA report (sections: harmonization, missing data, sensor errors, downstream risk)
- Issue list (table: issue, location, severity, impact, recommendation)
- Root cause analysis and remediation priority
- Feature Risk Block
