# Dataset Schema Templates

## Minimal Schema
- Dataset Name
- Description
- Fields (name, type, description, units, value range, required/optional)
- Metadata (creator, version, date, license)
- Units
- Value Ranges
- Missing Data Policy (explicit handling)
- Provenance/Lineage (if applicable)

## Domain Adaptation
- **Biomechanics:** Include sensor type, anatomical reference, sampling rate
- **Computer Vision:** Include image resolution, annotation schema, file format
- **Rehabilitation:** Include patient ID anonymization, assessment scales
- **Neuroperformance:** Include modality (EEG/fMRI), channel layout, event markers

## Example
| Field Name | Type   | Description         | Units | Range   | Required |
|-----------|--------|---------------------|-------|---------|----------|
| age       | int    | Participant age     | years | 18-99   | Yes      |
| score     | float  | Test score          | N/A   | 0-100   | Yes      |
