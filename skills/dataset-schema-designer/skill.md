# Dataset Schema Designer Skill

## Purpose
Define structured, FAIR-compliant, and standards-driven dataset schemas for research projects. Explicitly surface required/optional fields, metadata, provenance, versioning, schema risks, harmonization considerations, downstream analysis implications, and validation rules. Produce machine-readable QA Validation Block for downstream skills.

## Scope
- Human, animal, or simulation datasets
- Outputs field definitions, types, metadata, provenance, versioning, and validation rules
- Upstream: Protocol Writer (Protocol Handoff Block)
- Downstream: Dataset QA, Feature Engineering

## When to Use
- Before data collection, during protocol development, or for schema review/harmonization, with Protocol Handoff Block available

## When Not to Use
- If research goals or data collection plan are missing or ambiguous

## Required Inputs
- Protocol Handoff Block from Protocol Writer
- Data types and sources

## Optional Inputs
- Domain-specific metadata requirements (e.g., MIAME, BIDS)
- Output format preference (Markdown, table)

## Workflow
1. Parse Protocol Handoff Block, data collection plan, and data types
2. Propose dataset fields, types, value ranges, and validation rules
3. Define metadata (units, standards, provenance, versioning) and missing data policy
4. Identify schema risks and harmonization considerations
5. Surface downstream analysis implications
6. Output structured schema with explicit rationale for field choices
7. Generate QA Validation Block for downstream skills (machine-readable)

## Output Contract
- Field Table (name, type, description, units, range, required/optional, validation rules)
- Metadata Section (standards, provenance, harmonization notes, versioning)
- Missing Data Policy (handling, imputation, reporting)
- Schema Risks and Harmonization Considerations
- Downstream Analysis Implications
- QA Validation Block (machine-readable)
- Errors (if any)

## Quality Checks
- All fields are defined, described, and justified
- Metadata, provenance, and versioning are explicit
- Schema risks and harmonization are surfaced
- Validation rules are present and actionable
- Output is suitable for direct use by Dataset QA and Feature Engineering skills

## Failure Modes
- Missing, ambiguous, or unjustified field definitions
- Non-compliance with standards or FAIR principles
- Failure to address missing data, harmonization, or validation
- Lack of downstream analysis implications

## Domain Adaptation Notes
- For biomechanics: specify sensor types, sampling rates, and units
- For neuroperformance: specify cognitive domains, measurement modalities

## Example Invocation Patterns
- "Define a dataset schema for wearable sensor data in running studies (2024, field/lab, 100Hz sampling), including validation rules and harmonization notes."
- "Propose a schema for cognitive task performance data, including metadata, versioning, and QA Validation Block."
