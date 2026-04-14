# Reviewer Mode Skill

## Purpose
Emulate rigorous, standards-driven peer review for manuscripts, protocols, or research outputs, surfacing fatal flaws, fixable weaknesses, and providing prioritized, actionable revision guidance. Outputs are designed for internal QA and pre-submission review, with explicit Reviewer Exposure Block integration.

## Scope
- Academic papers, protocols, and reports
- Outputs: review reports, actionable feedback, rubric scores, Reviewer Exposure Block
- Upstream: Paper Outliner (Reviewer Exposure Block)
- Downstream: (End of pipeline)

## When to Use
- After manuscript or protocol drafting, before submission or publication, or for internal QA

## When Not to Use
- If input document or review rubric is missing, ambiguous, or unreviewed

## Required Inputs
- Manuscript, protocol, or research output (see `skills/paper-outliner/skill.md`)
- Review rubric or checklist (see `shared/review-rubric.md`, `standards/evaluation-checklist.md`)
- Reviewer Exposure Block from Paper Outliner

## Optional Inputs
- Specific review focus (e.g., methods, clarity, reproducibility)
- Output format preference (Markdown, table)

## Workflow
1. Parse input document, rubric/checklist, and Reviewer Exposure Block
2. Evaluate against rubric criteria, explicitly referencing each criterion and surfacing fatal flaws vs. fixable weaknesses
3. Generate structured review report with actionable feedback, rubric scores, and revision priority ranking
4. Output structured review report with explicit rationale, fatal flaw/weakness distinction, and Reviewer Exposure Block integration

## Output Contract
- Review Report (Markdown, with explicit section headers)
- Actionable Feedback List (prioritized, specific, fatal flaw/weakness distinction)
- Rubric Scores (table: criterion, score, rationale)
- Revision Priority Ranking
- Reviewer Exposure Block (machine-readable: weak sections, missing evidence, likely reviewer concerns)
- Errors (if any)

## Quality Checks
- Feedback is specific, actionable, and standards-compliant
- All rubric criteria are addressed, justified, and referenced
- Fatal flaws and fixable weaknesses are distinguished and prioritized
- Reviewer Exposure Block is integrated and machine-readable
- Output is suitable for direct use by authors and internal QA

## Failure Modes
- Vague, generic, or non-actionable feedback
- Missed critical issues or rubric criteria
- Failure to address standards, reproducibility, or Reviewer Exposure Block
- Lack of fatal flaw/weakness distinction

## Domain Adaptation Notes
- For biomechanics: emphasize methods, measurement, population criteria, and sensor calibration
- For neuroperformance: emphasize cognitive domain coverage, task clarity, and domain-specific reporting

## Example Invocation Patterns
- "Review this protocol for a motion capture study using the provided rubric and Reviewer Exposure Block (2024)."
- "Peer review for a manuscript on wearable sensor data analysis, with explicit rubric scores, fatal flaw/weakness distinction, and prioritized revision guidance."
