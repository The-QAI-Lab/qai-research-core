# Statistical Analysis Skill

## Purpose
Deliver high-rigor, auditable statistical analysis plans that explicitly connect hypotheses to tests, surface assumptions and uncertainties, analyze tradeoffs, and produce structured, machine-readable outputs for downstream research skills.

## Scope
- Human, animal, or simulation datasets
- Outputs: analysis plans, statistical test tables, reporting structures, Paper Claims Block
- Upstream: Feature Engineering (Feature Handoff Block)
- Downstream: Paper Outliner, Reviewer Mode

## When to Use
- After feature engineering and Feature Handoff Block are available, before or during data analysis

## When Not to Use
- If dataset or feature list is missing, ambiguous, or unreviewed

## Required Inputs
- Feature Handoff Block from Feature Engineering
- Hypotheses or research questions

## Optional Inputs
- Preferred statistical methods or reporting standards (e.g., CONSORT, STROBE)
- Output format preference (Markdown, table)

## Workflow
1. Parse Feature Handoff Block and hypotheses
2. Propose analysis plan with explicit rationale, surfacing all assumptions and uncertainties
3. For each hypothesis, link to specific test(s), check and document assumptions, and report unresolved ambiguities
4. Offer primary and fallback analysis paths, with tradeoff analysis and justification
5. Identify power/sample size concerns, interpretation cautions, and risk factors
6. Distinguish exploratory vs. confirmatory analysis, and surface any limitations
7. Define reporting structure (tables, figures, summary statistics)
8. Output structured analysis plan with explicit section headers, rationale, and machine-readable blocks
9. Generate Paper Claims Block for downstream skills (machine-readable, with claims, evidence, limitations, and open questions)

## Output Contract
- Executive Summary
- Analysis Plan (Markdown, explicit section headers)
- Statistical Test Table (test, variables, assumptions, rationale, hypothesis linkage, tradeoff notes)
- Primary and fallback analysis paths
- Power/sample size notes
- Interpretation cautions
- Exploratory vs. confirmatory distinction
- Paper Claims Block (machine-readable: claims, evidence, limitations, open questions)
- Errors and unresolved ambiguities (if any)

## Quality Checks
- All analysis steps are explicit, justified, and standards-compliant
- Hypothesis-to-test linkage is explicit and auditable
- Assumptions and uncertainties are surfaced and documented
- Tradeoff logic is present for method selection
- Primary and fallback analysis paths are present
- Power/sample size and interpretation cautions are surfaced
- Output is suitable for direct use by Paper Outliner and Reviewer Mode skills
- Machine-readable Paper Claims Block is present

## Failure Modes
- Inappropriate, unjustified, or non-reproducible tests
- Vague, incomplete, or generic analysis plans
- Failure to address assumptions, power/sample size, or reporting standards
- Lack of exploratory/confirmatory distinction
- Missing or malformed Paper Claims Block

## Domain Adaptation Notes
- For biomechanics: specify repeated measures, mixed models, sensor-derived variables, harmonization issues
- For neuroperformance: specify cognitive domain analyses, correction for multiple comparisons, domain-specific confounders

## Example Invocation Patterns
- "Plan statistical analysis for a study on running gait variability (feature list and Feature Handoff Block attached, 2024), including primary/fallback analysis, tradeoff logic, and Paper Claims Block."
- "Outline analysis plan for cognitive task performance data, with explicit hypothesis-to-test linkage, assumption checks, tradeoff analysis, and reporting structure."
