# Feature Engineering Skill — Examples

## Example 1: Generic Academic
**Input:** Suggest features for image classification dataset (2024, schema attached, goal: disease detection). Include feature family separation, leakage risk analysis, and Feature Handoff Block.
**Output:**
- Feature table (name, type, family, calculation, rationale, value range, hypothesis linkage, leakage risk)
- Explicit calculations (e.g., "Mean pixel intensity" [raw], "Texture entropy" [derived])
- Rationale for each feature
- Leakage risk analysis (e.g., label leakage)
- Validation and ablation suggestions
- Feature Handoff Block (machine-readable)

## Example 2: Biomechanics
**Input:** Features for analyzing knee joint loading in running studies (adult athletes, 2023–2024, schema and Feature Risk Block attached). Include domain-informed and exploratory features, leakage risk, and validation suggestions.
**Output:**
- Feature table (e.g., "Peak knee flexion angle" [domain-informed], "Ground reaction force" [raw], "Stride variability" [exploratory])
- Calculation methods, value ranges, rationale, and hypothesis linkage
- Leakage risk identification (e.g., sensor drift)
- Validation and ablation suggestions
- Feature Handoff Block

## Example 3: QAI-Style Applied
**Input:** Features for wearable sensor data in soccer (10 sensors, 2024, harmonization with lab data required, schema and Feature Risk Block attached). Include feature family separation, leakage risk, and handoff block.
**Output:**
- Structured feature list (e.g., "Acceleration variance" [derived], "Step frequency" [raw], "Player load" [domain-informed])
- Calculation methods, rationale, value ranges, and hypothesis linkage
- Leakage risk analysis (e.g., time sync errors)
- Validation and ablation suggestions
- Feature Handoff Block
