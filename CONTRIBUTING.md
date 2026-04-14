# Contributing to QAI Lab Research Core

This repository is a critical part of QAI Lab’s research infrastructure. All contributions must meet the highest standards of scientific rigor, reproducibility, and operational clarity.

## Proposing a New Skill
- Review `standards/skill-spec-template.md` and `standards/naming-conventions.md` before starting.
- Submit a draft `skill.md`, `README.md`, `examples.md`, and `tests.md` in a new folder under `skills/`.
- Reference shared standards and templates in all documentation and logic.
- Clearly define required/optional inputs, output contracts, and quality checks.

## Updating an Existing Skill
- Document all changes in `CHANGELOG.md` with clear rationale.
- Update all affected documentation, examples, and tests.
- Ensure backward compatibility unless a breaking change is justified and reviewed.

## Documentation Standards
- Every skill must have:
  - A detailed, standards-compliant `skill.md`
  - A concise, operational `README.md`
  - Three realistic, research-driven examples in `examples.md`
  - Behavioral validation criteria in `tests.md`
- All documentation must reference relevant standards and shared assets.

## Naming and Structure
- Use lowercase, hyphen-separated folder and file names (see `standards/naming-conventions.md`).
- Skill names must be descriptive, unambiguous, and consistent with the skill pipeline.

## Testing and Validation
- Each skill must include behavioral tests in `tests.md` that:
  - Validate output structure and rigor
  - Check for unsupported claims and limitations
  - Ensure domain relevance and reproducibility
- Tests must be operational, not theoretical.

## Review and Acceptance
- All contributions are peer-reviewed for:
  - Scientific rigor
  - Reproducibility
  - Standards compliance
  - Operational clarity
- Use `shared/review-rubric.md` and `standards/evaluation-checklist.md` during review.

## Versioning and Changelog
- Use semantic versioning for all major changes.
- Every change must be logged in `CHANGELOG.md` with a summary and rationale.
- Prioritize stability, reproducibility, and cross-skill alignment.

---

For questions, contact the QAI Lab core team. All contributions are subject to internal review and may be rejected if they do not meet operational standards.