# Skill Specification Template

This template is mandatory for every new skill in the QAI Lab Research Core. All sections are required unless explicitly marked optional. Use precise, operational language. Skills must be reasoning modules, not just formatters.

## Skill Name
- Descriptive, hyphen-separated (see naming conventions)

## Purpose
- What research reasoning function does this skill operationalize?
- What problem does it solve?

## Scope
- Boundaries of the skill (what is in/out)
- Upstream and downstream dependencies

## When to Use
- Scenarios where this skill is essential

## When Not to Use
- Scenarios where this skill is not appropriate

## Required Inputs
- List and describe all required inputs (types, formats, constraints)

## Optional Inputs
- List and describe all optional inputs (types, formats, constraints)

## Workflow
1. Step-by-step operational logic (no vague steps)
2. Explicit decision logic, tradeoff analysis, and alternative path generation where appropriate
3. Assumption surfacing and uncertainty reporting at each step

## Output Contract
- Explicit structure (sections, tables, fields, handoff blocks)
- Minimum rigor requirements (citations, limitations, error handling, tradeoff matrices, risk registers as needed)
- Machine-readable handoff artifacts for downstream skills
- Reference to shared standards

## Assumption Handling
- What assumptions are made (explicitly list)
- Which assumptions are weak or require validation
- How assumptions are surfaced in outputs

## Uncertainty Handling
- What is known, inferred, or unresolved
- How uncertainty is reported in outputs

## Tradeoff Analysis
- Where competing options exist, what are the tradeoffs
- What is gained/lost by each option
- Decision tables or matrices if appropriate

## Alternative Generation
- At least one main path and one alternative path (when appropriate)
- Rationale for preference

## Failure Awareness
- What could cause low-quality output
- Warning signs and error reporting

## Handoff Artifacts
- Define structured outputs intended for downstream skills (not just prose)
- Include reusable handoff blocks

## Evidence Discipline
- Distinguish evidence-backed claims, domain assumptions, and recommendations
- Explicit citation and reference structure

## Quality Checks
- Criteria for high-quality, reproducible, and reasoning-rich outputs
- How to validate outputs against standards

## Failure Modes
- Common errors, edge cases, and how to handle them
- How uncertainty and missing data are reported

## Examples
- At least one academic, one domain, and one QAI-style invocation
- At least one example demonstrating tradeoff or ambiguity handling

## Domain Adaptation Notes
- How to adapt this skill for biomechanics, computer vision, rehabilitation, neuroperformance, etc.
