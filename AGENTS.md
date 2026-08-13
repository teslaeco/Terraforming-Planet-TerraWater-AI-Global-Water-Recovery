# AGENTS.md

## Mission
Build TerraWater AI as an evidence-first open-source water monitoring and recovery decision-support application.

## Non-negotiable rules
- Use only legal official and/or openly licensed public data.
- Never present synthetic imagery, interpolation, reconstruction, AI-generated imagery, or a basemap as a real satellite observation.
- Preserve provenance for every observation: source, product ID when available, acquisition time, retrieval time, resolution and license/access note.
- Separate `OBSERVED`, `DERIVED`, `CANDIDATE_CAUSE`, `VERIFICATION_REQUIRED`, and `CONFIRMED` states in code and UI.
- Do not call a blocked inflow/outflow, damaged culvert, diversion, drought cause, contamination source or other cause "confirmed" without authoritative evidence.
- Physical interventions in rivers, lakes, wetlands, drainage, dams or channels must always be framed as requiring local hydrological, ecological, legal and safety review.
- Never commit API keys, tokens, `.env` files or credentials.

## Engineering expectations
- TypeScript strict mode.
- Small modules with tests.
- Run typecheck, tests and build before proposing merge.
- CI must be green before merge.
- Prefer deterministic geospatial calculations outside the language model.
- OpenAI is used for evidence synthesis, alternatives, uncertainty and next-step planning; it must not invent measurements.
- Keep OpenAI calls server-side.
- Make the static UI degrade gracefully when the AI backend is unavailable.

## Initial case
Olszówka / Gardeja, Poland is Case Study 001. Treat local observations as investigation leads. Verify coordinates, waterbody geometry and hydrological connectivity with authoritative/public geodata before scientific conclusions.

## Challenge traceability
When Codex makes a meaningful change, describe the task and tests in the pull request conversation so the development history is auditable for the Build for Good challenge.
