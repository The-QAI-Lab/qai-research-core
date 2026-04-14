# Dataset QA Skill

## Purpose
Assess dataset quality, completeness, and integrity for research, ensuring datasets are ready for analysis, publication, and downstream use. Classify issues by severity and impact, separate blocking from non-blocking issues, identify likely root causes, and produce a machine-readable Feature Risk Block for downstream skills.

## Scope
- Human, animal, or simulation datasets
- Outputs QA reports, issue lists, actionable recommendations, and Feature Risk Block
- Upstream: Dataset Schema Designer (QA Validation Block)
- Downstream: Feature Engineering, Statistical Analysis

## When to Use
- After data collection, before analysis, or during data harmonization, with QA Validation Block available

## When Not to Use
- If dataset schema is missing or ambiguous

## Required Inputs
- Dataset sample or summary
- QA Validation Block from Dataset Schema Designer

## Optional Inputs
- Domain-specific QA criteria (e.g., biomechanics, neuroperformance)
- Output format preference (Markdown, table)

## Workflow
1. Parse dataset, schema, and QA Validation Block
2. Check for completeness, consistency, errors, standards compliance, and downstream risk
3. Classify issues by severity and impact (blocking/non-blocking)
4. Identify likely root causes and remediation priority
5. Surface downstream risk to Feature Engineering and Statistical Analysis
6. Output structured QA report with explicit rationale for findings
7. Generate Feature Risk Block for downstream skills (machine-readable)

## Output Contract
- QA Report (Markdown, with explicit section headers)
- Issue List (table: issue, location, severity, impact, recommendation)
- Recommendations (actionable, prioritized)
- Feature Risk Block (machine-readable)
- Errors (if any)

## Quality Checks
- All issues are clearly identified, described, and actionable
- Severity and impact are classified (blocking/non-blocking)
- Recommendations are specific, feasible, and standards-compliant
- Root causes and remediation priorities are surfaced
- Downstream risk is explicit
- Output is suitable for direct use by Feature Engineering and Statistical Analysis skills

## Failure Modes
- Missed errors, incomplete checks, or vague recommendations
- Failure to address standards compliance, harmonization, or downstream risk
- Lack of issue severity/impact classification

## Domain Adaptation Notes
- For biomechanics: check sensor calibration, sampling rates, and missing data
- For neuroperformance: check cognitive domain coverage, timing accuracy

## Example Invocation Patterns
- "Assess the quality of this motion capture dataset for gait analysis (schema and QA Validation Block attached). Include Feature Risk Block."
- "QA report for multi-sensor wearable data in soccer, with actionable recommendations and downstream risk surfacing."
