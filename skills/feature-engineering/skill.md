# Feature Engineering Skill

## Purpose
Propose, define, and justify explicit, standards-driven features for research data analysis and modeling. Separate raw, derived, domain-informed, and exploratory features; justify feature families; identify leakage risks; connect feature choices to hypotheses and analysis plans; and produce a machine-readable Feature Handoff Block for downstream analysis.

## Scope
- Human, animal, or simulation datasets
- Outputs feature lists, calculations, rationales, leakage risk analysis, and Feature Handoff Block
- Upstream: Dataset QA (Feature Risk Block)
- Downstream: Statistical Analysis, Paper Outliner

## When to Use
- After dataset QA and Feature Risk Block are available, before statistical analysis or model building

## When Not to Use
- If dataset or schema is missing, ambiguous, or unreviewed

## Required Inputs
- Dataset or structured schema (see `skills/dataset-qa/skill.md`)
- Feature Risk Block from Dataset QA
- Research question or analysis goal

## Optional Inputs
- Domain-specific feature requirements (e.g., biomechanics, neuroperformance)
- Output format preference (Markdown, table)

## Workflow
1. Parse dataset/schema, Feature Risk Block, and research goal
2. Propose candidate features, separated by family (raw, derived, domain-informed, exploratory)
3. For each feature, define calculation, value range, rationale, and linkage to hypothesis/analysis
4. Identify leakage risks and mitigation strategies
5. Suggest validation and ablation strategies
6. Output structured feature list with rationale for each feature
7. Generate Feature Handoff Block for downstream skills (machine-readable)

## Output Contract
- Feature List (table: name, type, family, calculation, rationale, value range, hypothesis/analysis linkage, leakage risk)
- Domain Notes (adaptation, interpretability)
- Validation and ablation suggestions
- Feature Handoff Block (machine-readable)
- Errors (if any)

## Quality Checks
- Features are relevant, justified, and standards-compliant
- Feature families are explicit and separated
- Calculations are explicit and reproducible
- Leakage risks and mitigation are surfaced
- Output is suitable for direct use by Statistical Analysis and Paper Outliner skills

## Failure Modes
- Vague, generic, or unjustified features
- Missing rationale, calculation, or family assignment
- Failure to address interpretability, leakage, or domain adaptation
- Lack of validation/ablation suggestions

## Domain Adaptation Notes
- For biomechanics: specify sensor-derived features, normalization methods, and leakage risks
- For neuroperformance: specify cognitive domain features, scoring methods, and validation strategies

## Example Invocation Patterns
- "Propose features for classifying running gait from wearable sensor data (schema and Feature Risk Block attached, 2024), including leakage risk analysis and validation suggestions."
- "Define features for cognitive task performance analysis, with explicit calculations, rationale, and Feature Handoff Block."
