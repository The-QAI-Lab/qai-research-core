# Protocol Writer Skill

## Purpose
Generate detailed, reproducible, and standards-compliant protocols for experiments or studies, tying each operational step to experimental design rationale. Surface operational failure points, include checkpoints and deviations tracking, and produce structured handoff artifacts for dataset planning and QA.

## Scope
- Human, animal, or simulation protocols
- Outputs step-by-step procedures, materials lists, compliance checklists, and documentation requirements
- Upstream: Experiment Design (Protocol + Schema Handoff Block)
- Downstream: Dataset Schema Designer, Dataset QA

## When to Use
- After experiment design is finalized and Protocol + Schema Handoff Block is available
- For IRB submission, preregistration, or operational documentation

## When Not to Use
- If experiment plan is missing, ambiguous, or lacks variable/control definitions

## Required Inputs
- Protocol + Schema Handoff Block from Experiment Design
- Methods and materials

## Optional Inputs
- Specific reporting standards (e.g., CONSORT, SPIRIT)
- Output format preference (Markdown, table)

## Workflow
1. Parse Protocol + Schema Handoff Block, methods, and materials
2. Generate explicit protocol steps, each linked to design rationale
3. Identify operational failure points and checkpoints
4. Specify required documentation during execution
5. Generate materials list and compliance checklist
6. Output structured protocol document with explicit rationale, checkpoints, and deviations tracking

## Output Contract
- Protocol Steps (Markdown, with explicit section headers)
- Step-to-design rationale mapping
- Materials Table (with quantities and specifications)
- Compliance Checklist (regulatory, ethical, operational)
- Checkpoints and deviations tracking
- Documentation requirements
- Protocol Handoff Block (machine-readable)
- Errors (if any)

## Quality Checks
- Steps are explicit, reproducible, and standards-compliant
- Each step is traceable to design rationale
- Materials and compliance requirements are addressed and justified
- Operational failure points and checkpoints are surfaced
- Output is suitable for direct use by Dataset Schema Designer and Dataset QA skills

## Failure Modes
- Missing steps, unclear instructions, or unjustified materials
- Non-compliance with reporting standards
- Failure to address regulatory or ethical requirements
- Lack of traceability between steps and design rationale
- Missing checkpoints or deviations tracking

## Domain Adaptation Notes
- For clinical: include patient safety and consent procedures
- For biomechanics: specify measurement tools and calibration steps
- For engineering: include device specifications and validation steps

## Example Invocation Patterns
- "Write a protocol for a randomized controlled trial of a new knee brace (adult athletes, 2024), including checkpoints and deviations tracking."
- "Generate a protocol for field-based wearable sensor validation, with step-to-design rationale mapping and compliance checklist."
