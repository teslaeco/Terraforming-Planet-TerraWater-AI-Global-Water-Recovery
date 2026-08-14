# TerraWater AI — Global Water Recovery Observatory

> Open-source evidence platform for detecting water loss, comparing change through time, and helping people investigate how water moves through a watershed before proposing restoration.

TerraWater AI is being built for the **Build for Good** developer challenge. The project combines public satellite and hydrology data, reproducible geospatial analysis, a 3D/map interface, and the OpenAI API to help people understand shrinking lakes, degraded wetlands, disrupted inflows/outflows, drought exposure, and flood-risk trade-offs.

## New research direction — Arctic 90°N reference station

As an extension of the same evidence-first monitoring idea, TerraWater AI is also documenting a concept for a **permanently fixed scientific reference station at the geographic North Pole (90°N)**.

The purpose would be to combine continuous in-situ measurements of snow, sea ice, melt ponds, ocean conditions and atmosphere with selected official satellite products. AI could synchronize satellite overpasses with direct measurements, detect disagreements, classify ice/water states, estimate uncertainty and flag sensor or retrieval anomalies.

**Critical measurement distinction:** ESA documents that CryoSat reaches about **88°N/S** on each orbit. That is a property of CryoSat's orbit, not a universal rule for all satellites. Existing drifting camps and ice-tethered instruments provide real, scientifically valuable calibrated data, but they are not equivalent to a permanent multi-year geodetic benchmark fixed exactly at 90°N. TerraWater therefore treats a fixed 90°N reference as a research proposal for reducing one class of satellite/ground comparison uncertainty — not as proof that existing Arctic measurements are invalid.

The concept now also includes a **seabed-supported artificial research island / tapered megastructure** as one architecture to test numerically. The initial simulation envelope uses a nominal **8 km × 8 km footprint and ~7 km vertical scale**. These are deliberately treated as placeholder dimensions for feasibility modeling, not construction specifications. Bathymetry, geology, ice loads, current changes, ecological effects, international law and lower-impact alternatives must all be evaluated before any construction decision.

**Full concept note:** [Arctic 90°N Research Direction — Build for Good / TerraWater AI](docs/ARCTIC_90N_RESEARCH_DIRECTION.md)

**Interactive mini-experiment lab:** https://terraforming-planet.github.io/Polar-Sun-Moon-Analysis/arctic-90n/mini-experiments-lab.html

**Experiment summary and formulas:** [Arctic 90°N — Mini-Experiment Lab](docs/ARCTIC_90N_MINI_EXPERIMENTS.md)

**Educational lesson:** [Hidden Water Inside Earth — what we know and what we still cannot measure exactly](docs/LESSON_HIDDEN_WATER_INSIDE_EARTH.md)

The lesson explains why planetary water accounting must separate direct measurements from derived, interpolated and model-estimated values. It also explains the 2014 hydrous-ringwoodite result, fractured-rock uncertainty and why a realistic 3D Earth model should display data gaps rather than hide them behind apparently exact values.

## What we built

The first competition version is a new, standalone application built from lessons learned in the existing [Terraforming Planet — Polar Sun Moon Analysis](https://github.com/Terraforming-Planet/Polar-Sun-Moon-Analysis) project.

TerraWater AI is designed around a simple workflow:

1. **Find a water body or watershed.**
2. **Load real observations** from official/public sources.
3. **Compare time periods** to measure changes in surface water, shoreline, vegetation, and radar response.
4. **Trace the watershed** upstream and downstream instead of looking only at the lake itself.
5. **Separate evidence from hypotheses.** A suspected blocked inflow, drainage problem, groundwater decline, siltation, or water diversion is never presented as confirmed without evidence.
6. **Use OpenAI to synthesize the evidence** into alternative explanations, confidence levels, missing-data checks, and a prioritized investigation plan.
7. **Produce a restoration-support report** that clearly distinguishes observed facts, model-derived metrics, candidate causes, and actions that require field/legal/environmental verification.

## Who it helps

The intended users are:

- communities exposed to drought, water shortages, degraded lakes and wetlands;
- communities exposed to flooding where drainage and storage are poorly balanced;
- researchers, students, NGOs and open-science contributors;
- municipalities and water managers who need a transparent first-pass evidence view;
- emergency and environmental teams that need to compare current conditions with historical context.

TerraWater AI is a **decision-support and research tool**, not an authority that orders physical interventions. Any excavation, dredging, gate operation, channel modification, pumping, dam work, or ecological intervention requires local hydrological, environmental, legal, and safety review.

## Evidence model

Every conclusion in the application must carry a status:

- `OBSERVED` — directly visible/measured in a source product;
- `DERIVED` — computed from observations (for example, area change or an index);
- `CANDIDATE_CAUSE` — a hypothesis that fits the evidence but is not confirmed;
- `VERIFICATION_REQUIRED` — needs another sensor, record, survey or field check;
- `CONFIRMED` — supported by authoritative evidence and provenance.

The application must never label synthetic reconstruction, AI-generated imagery, interpolation, or a visualization layer as a real satellite photograph.

## Initial case study — Olszówka / Gardeja, Poland

The first reproducible case study focuses on the Olszówka/Gardeja area and nearby water bodies, including Jezioro Kuchnia, the locally known Jezioro Panieńskie / map-labelled “Staw w lesie”, Jezioro Kamień, Jezioro Nogat and nearby connected or potentially connected water features.

The purpose is not to hard-code a diagnosis. The goal is to teach the system how to:

- compare historical and recent surface-water extent;
- distinguish a shrinking/open-water signal from vegetation and seasonal variation;
- trace possible surface-water connectivity;
- search upstream/downstream for similar anomalies;
- record local observations without converting them into unverified facts;
- compare the case with validated examples from other countries.

## Data sources

Only legal, official and/or openly licensed public sources are intended for analysis. Planned integrations include:

- **Copernicus Data Space Ecosystem (CDSE)** — Sentinel-1 and Sentinel-2;
- **Copernicus / JRC Global Surface Water** — long-term surface-water history;
- **NASA Earthdata / Worldview** — selected global observations and supporting context;
- **USGS Landsat** — long historical optical record;
- **Wody Polskie / Hydroportal and Polish public geodata** for the Polish case study;
- other national hydrology/environment agencies for international case studies;
- OpenStreetMap only as a public reference/label layer where appropriate, never as the sole authority for a scientific claim.

Every stored observation should include source, acquisition time, product identifier, spatial resolution, license/access note, and retrieval timestamp where available.

## OpenAI API

The OpenAI integration runs **server-side**. API keys are never embedded in the web client or committed to GitHub.

The current backend scaffold uses the OpenAI **Responses API** to turn a structured evidence bundle into an analysis that is explicitly instructed to:

- separate observations from hypotheses;
- list competing explanations;
- identify missing evidence;
- assign cautious confidence language;
- avoid fabricating measurements, coordinates, satellite acquisitions or official findings;
- recommend the next data checks before any physical intervention.

The model is configured with the `OPENAI_MODEL` environment variable so the project can adopt newer supported models without rewriting the application.

## How Codex is used

Codex is part of the development workflow from the beginning. We use it for repository exploration, implementation, tests, refactoring, review, CI fixes, documentation and follow-up pull requests. The repository contains `AGENTS.md` with project-specific instructions for Codex.

For challenge traceability we keep development work in reviewable pull requests and record Codex-assisted tasks in PR conversations. Codex is expected to run tests/linters before proposing changes and to preserve evidence provenance as a core invariant.

## Architecture

```text
browser / map UI
      |
      |  evidence bundle (no secrets)
      v
TerraWater API  -----> OpenAI Responses API
      |
      +-----> source adapters / manifests
      +-----> change detection
      +-----> watershed graph
      +-----> provenance ledger
```

Repository layout:

```text
src/                 web application
server/              server-side API and OpenAI integration
data/                 versioned demo/case metadata (not secret)
schemas/              evidence and analysis contracts
docs/                 architecture, provenance and research notes
tests/                application and evidence tests
.github/workflows/    CI and deployment
```

## Run locally

Requirements: Node.js 20+ and npm.

```bash
npm install
cp .env.example .env
npm run dev
```

The web app runs on Vite and the API runs locally on port `8787` by default.

To enable AI analysis, set an OpenAI API key in your local environment:

```bash
OPENAI_API_KEY=your_key_here
OPENAI_MODEL=gpt-5
```

Never commit `.env`, API keys, tokens or private credentials.

## Quality gates

```bash
npm run typecheck
npm test
npm run build
```

Pull requests should stay unmerged while required CI is red.

## Challenge demo plan

The competition demo will show:

1. a real water-loss case selected on the map;
2. historical observations and timestamps;
3. measured surface-water change;
4. upstream/downstream watershed context;
5. visually distinct evidence and candidate-cause layers;
6. an OpenAI evidence synthesis with alternatives and missing-data checks;
7. a reproducible report with links back to source products.

## Current status

**Bootstrap / active development.** The first pull request establishes the application skeleton, evidence contract, OpenAI server endpoint, CI and the Olszówka/Gardeja demonstration seed. Real sensor adapters and automated water-change extraction are the next milestones.

## License

MIT. See [LICENSE](LICENSE).
