# Gap Finder Skill

## Purpose
Identify, rank, and structure actionable, high-impact research gaps from structured literature review outputs, enabling targeted experiment and protocol design.

## Scope
- Academic research domains (biomechanics, neuro, vision, rehabilitation, etc.)
- Consumes structured, standards-compliant literature summaries with Gap Handoff Blocks
- Outputs gap prioritization matrices, candidate research questions, and experiment framing blocks
- Upstream: Literature Review
- Downstream: Experiment Design, Protocol Writer

## When to Use
- After a literature review with explicit limitations, uncertainties, and Gap Handoff Block
- When planning new studies or grant proposals

## When Not to Use
- If literature review is missing, unstructured, or lacks explicit limitations/gaps

## Required Inputs
- Structured literature review output (see `skills/literature-review/skill.md`)

## Optional Inputs
- Domain focus (e.g., biomechanics, neuro)
- Exclusion criteria (e.g., populations, methods)

## Workflow
1. Parse literature summary, limitations, uncertainties, and Gap Handoff Block
2. Extract explicit and implicit research gaps
3. Rank gaps by novelty, feasibility, impact, and data accessibility
4. Distinguish true research gaps from implementation gaps
5. Generate candidate research questions and paper directions
6. Output a structured, traceable gap list with rationale, prioritization matrix, and supporting citations
7. Produce an Experiment Framing Block for downstream skills

## Output Contract
- Gap List (each with rationale, supporting citations, and traceability to literature review)
- Gap Prioritization Matrix (criteria: novelty, feasibility, impact, data accessibility)
- Candidate Research Questions
- Experiment Framing Block (structured for Experiment Design and Paper Outliner)
- Errors (if any)

## Assumption Handling
- List assumptions about gap novelty, feasibility, and data accessibility
- Surface weak or unvalidated assumptions

## Uncertainty Handling
- Report unresolved or ambiguous gaps
- Highlight areas where evidence is insufficient

## Tradeoff Analysis
- Discuss tradeoffs in pursuing different gaps (e.g., feasibility vs. impact)
- Present decision logic for prioritization

## Alternative Generation
- Present at least one alternative gap prioritization or research direction

## Failure Awareness
- Warn if gaps are trivial, unsupported, or not actionable
- Report ambiguous or missing data explicitly

## Handoff Artifacts
- Experiment Framing Block: machine-readable summary of prioritized gaps and candidate research questions for downstream skills

## Evidence Discipline
- Distinguish evidence-backed gaps from speculative or inferred gaps
- All claims must be cited

## Quality Checks
- Gaps are actionable, specific, and non-generic
- Each gap is traceable to literature review content
- Prioritization logic is explicit and justified
- Output is suitable for direct use by Experiment Design and Paper Outliner

## Failure Modes
- Vague, generic, or unsupported gaps
- Gaps not traceable to literature
- Failure to prioritize or explain rationale
- Failure to produce a usable Experiment Framing Block

## Domain Adaptation Notes
- For biomechanics: focus on populations, measurement gaps, intervention gaps
- For neuroperformance: focus on cognitive domains, measurement modalities

## Example Invocation Patterns
- "Identify and rank research gaps from the attached literature review on ACL injury prevention. Include a prioritization matrix and Experiment Framing Block."
- "Extract and prioritize gaps from a review of wearable sensor accuracy in sports performance, and generate candidate research questions."
