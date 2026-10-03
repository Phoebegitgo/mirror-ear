# Mirror Ear

Mirror Ear is a longitudinal digital twin platform for microtia and atresia care. It integrates patient journeys, hearing rehabilitation, anatomy, intervention history, and quality-of-life data into a patient-held and multicentre clinical view.

## Vision

Our long-term vision is a longitudinal digital twin of the patient’s ear and hearing journey: a family-first, clinician-supported, research-ready platform spanning the full care pathway across childhood and adolescence.

## Phase roadmap

- Phase 0: hackathon prototype and education-only content
- Phase 1: family app with patient-held record and information tools
- Phase 2: clinician + registry support with multicentre, consented data
- Phase 3: clinical modules and regulated measurement tools

## Repository structure

- `apps/web-family`: family app and patient experience
- `apps/web-clinician`: clinical team interface
- `apps/research-portal`: research cohort and registry tools
- `services/api-gateway`: shared auth, routing, and audit
- `services/patient-record`: FHIR-backed patient records
- `services/pathway-engine`: versioned treatment logic
- `services/journey-proms`: timelines, hearing logs, PROMs
- `services/media-service`: photos and scan management
- `services/measurement-service`: landmarking and symmetry metrics
- `services/3d-pipeline`: mesh and mirror processing for 3D anatomy
- `packages/shared-core`: shared models and utilities
- `docs`: architecture, development, compliance, and design docs

## Stack

- Frontend: TypeScript + React/Svelte + three.js
- API: Node.js / TypeScript
- Imaging & analytics: Python / FastAPI / OpenCV / Open3D
- Data: PostgreSQL + FHIR-compatible data model
- Identity: OIDC / Keycloak
- Storage: encrypted object storage in EU region

## Getting started

```bash
git clone https://github.com/Phoebegitgo/mirror-ear.git
cd mirror-ear
pnpm install
pnpm run dev
```

## Notes

This project intentionally separates non-regulated information services from future device/software modules so the regulated boundary remains narrow and auditable.
