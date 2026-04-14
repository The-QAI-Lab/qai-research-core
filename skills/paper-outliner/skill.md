# Paper Outliner Skill

## Purpose
Produce high-rigor, structured outlines for research papers and manuscripts that explicitly align claims to evidence, surface missing evidence, suggest figure/table strategies, flag weak sections, and provide a publication readiness checkpoint. Outputs are designed for direct use by Reviewer Mode and for seamless handoff from Statistical Analysis.

## Scope
- Academic papers, reviews, and reports
- Outputs: section breakdowns, outline templates, section notes, Reviewer Exposure Block
- Upstream: Statistical Analysis (Paper Claims Block)
- Downstream: Reviewer Mode

## When to Use
- After statistical analysis, during manuscript preparation or collaborative writing

## When Not to Use
- If study results or research topic are missing, ambiguous, or unreviewed

## Required Inputs
- Study results or structured research topic (see `skills/statistical-analysis/skill.md`)
- Target journal or format
- Paper Claims Block from Statistical Analysis

## Optional Inputs
- Section emphasis, custom structure, or reporting standards (e.g., IMRAD, PRISMA)
- Output format preference (Markdown, table)

## Workflow
1. Parse study results, Paper Claims Block, and target format
2. Propose outline structure and section breakdowns, aligning claims to evidence and surfacing missing evidence
3. Suggest figure/table strategy and flag weak sections before drafting
4. Output structured outline with section notes, Reviewer Exposure Block, and publication readiness checkpoint

## Output Contract
- Outline (Markdown list or table, with explicit section headers)
- Section Notes (purpose, content, rationale, evidence linkage)
- Figure/Table Strategy
- Reviewer Exposure Block (machine-readable: weak sections, missing evidence, likely reviewer concerns)
- Publication Readiness Checkpoint
- References Section (placeholder or populated)
- Errors (if any)

## Quality Checks
- Outline is complete, logically structured, and standards-compliant
- Claims are explicitly linked to evidence
- Missing evidence and weak sections are surfaced
- Figure/table strategy is present
- Reviewer Exposure Block is present and machine-readable
- Output is suitable for direct use by Reviewer Mode skill

## Failure Modes
- Missing, irrelevant, or unjustified sections
- Overly generic, incomplete, or non-actionable outlines
- Failure to address journal or reporting standards
- Missing Reviewer Exposure Block or evidence linkage

## Domain Adaptation Notes
- For biomechanics: include methods, sensor details, population notes, and harmonization challenges
- For neuroperformance: include cognitive domain sections, task descriptions, and domain-specific reporting needs

## Example Invocation Patterns
- "Outline a paper on wearable sensor validation in sports (target: IEEE TBME, 2024, Paper Claims Block attached), including Reviewer Exposure Block and figure/table strategy."
- "Generate a manuscript outline for cognitive task performance analysis, with explicit claims-to-evidence linkage, section notes, and publication readiness checkpoint."
