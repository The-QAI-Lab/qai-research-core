# Experiment Design Skill

## Purpose
Design robust, reproducible experiments based on prioritized research gaps. Generate both a primary and at least one alternative design, surface confounders, constraints, and validity threats, and align with downstream protocol and dataset planning. Explicitly handle assumptions, uncertainties, and tradeoffs, and produce structured handoff artifacts.

## Scope
- Academic, translational, and applied research
- Supports both confirmatory and exploratory studies

## Required Inputs
- Experiment Framing Block from Gap Finder
- Research question(s) and prioritized gaps
- Constraints (e.g., resources, ethics, timeline)

## Optional Inputs
- Preferred methodologies
- Existing protocols or templates
- Domain-specific requirements

## Workflow Steps
1. Parse Experiment Framing Block and research question(s)
2. Generate at least one primary and one alternative experimental design
3. For each design, specify:
   - Hypothesis and rationale
   - Methodological approach
   - Key variables and controls
   - Confounders and validity threats
   - Resource and ethical constraints
   - Alignment with analysis plan
   - Explicit assumptions and uncertainties
   - Tradeoff discussion (pros/cons, feasibility, risk)
4. Compare designs using a tradeoff matrix
5. Select preferred design and justify selection
6. Surface unresolved uncertainties and validation needs
7. Produce a risk register for each design
8. Generate Protocol + Schema Handoff Block for downstream skills (machine-readable)

## Output Structure
- Executive summary
- Structured design table (primary and alternative)
- Tradeoff matrix
- Risk register
- Explicit assumptions and uncertainties
- Protocol + Schema Handoff Block (machine-readable)
- Recommended next action

## Quality Checks
- Are all designs feasible, justified, and distinct?
- Are confounders, constraints, and validity threats surfaced?
- Is the tradeoff matrix explicit and actionable?
- Are assumptions and uncertainties clearly reported?
- Is the handoff block suitable for Protocol Writer and Dataset Schema Designer?
- Are risks and validation needs surfaced?

## Common Failure Modes
- Designs are generic or lack justification
- Confounders/constraints are omitted
- Tradeoff matrix is missing or superficial
- Handoff block is unstructured or incomplete
- Assumptions and uncertainties are not surfaced
- No alternative design or rationale

## Domain Adaptation Notes
- For biomechanics: include sensor/measurement constraints
- For clinical: include regulatory/ethical considerations
- For neuroperformance: include cognitive/behavioral endpoints

## Example Invocation Patterns
- "Design a randomized controlled trial for the top-ranked gap in the Experiment Framing Block. Include a primary and alternative design, tradeoff matrix, and risk register."
- "Provide both a primary and alternative design for a study on wearable sensors in rehabilitation, including explicit assumptions, tradeoff analysis, and a Protocol + Schema Handoff Block."
