# Experiment 001 — Forest Pond and Lake Kuchnia Water Loss (1990–2026)

## TerraWater evidence status

**State-transition evidence: SUPPORTED. Exact 2026 residual open-water area and exact percentage loss: UNCERTAINTY-GATED. Cause: NOT ESTABLISHED.**

Experiment 001 is the first formal positive evidence case for TerraWater AI. The evidence-building pipeline is now sufficiently documented and reproducible to begin additional independent examples. This does **not** mean that every numerical endpoint is known: the project explicitly preserves uncertainty rather than forcing a false percentage.

Heavy imagery, spectral outputs and source catalogs remain in:

`Terraforming-Planet/Polar-Sun-Moon-Analysis@annual-best-53-591400-19-010717`

This TerraWater repository records the research conclusion, methodology, decision gates and future AI-label policy.

## Area of interest

- Main analysis center: **53.591400, 19.010717**
- Standard image crop: **2 km × 2 km**
- Study interval: **1990–2026 inclusive**
- Corrected forest-pond measurement seed: approximately **53.594595, 19.000140**
- Secondary/control object: **Lake Kuchnia**

## Current authoritative forest-pond result

The earlier ~2.5 ha / 25,000 m² visual estimate has been superseded as the central result by a repeatable multi-year visible-footprint consensus built from seven clear historical primary images: **1998, 1999, 2000, 2004, 2005, 2006 and 2008**.

- central persistent historical footprint: **17,722.2 m² = 1.7722 ha**;
- conservative lower footprint: **16,269.3 m² = 1.6269 ha**;
- repeat-supported upper footprint: **21,642.0 m² = 2.1642 ha**;
- broad one-or-more-year union envelope: **23,978.3 m² = 2.3978 ha**;
- 1990 overlap with the central footprint: **16,398.1 m² = 92.528%**.

Individual historical visible components in the selected clear years range roughly **1.55–2.08 ha**.

The old 2.5 ha estimate is preserved as an earlier upper visual hypothesis only. It must not be presented as the central measured result.

## 2026 state

The historical consensus footprint overlays a visibly changed/drier basin in 2026, with no comparable persistent dark-water shape. May 2026 and the separately documented 7 August 2026 Sentinel-2B proxy show non-water-like diagnostics at the corrected location.

The project deliberately does **not** force a residual 2026 open-water area in square metres. Canopy, shadow, wet soil and mixed pixels can make a strict spectral water classifier fail for a small forest pond. The strongest defensible conclusion is therefore a **near-total state transition of the historical visible-water feature**, while the exact loss percentage stays uncertainty-gated.

## Seasonal evidence and missing-month policy

Spring acquisition order:
1. May;
2. April fallback;
3. June fallback.

Autumn acquisition order:
1. September;
2. October fallback;
3. November fallback.

Every fallback records its true acquisition date and month. A fallback is never relabelled as the preferred month.

As of **14 August 2026**, September–November 2026 have not occurred. Therefore the autumn series legitimately contains **1990–2025**, while 2026 is marked missing rather than invented. A real Sentinel-2B scene from **7 August 2026** is stored separately as `late_summer_proxy_only_not_autumn` and is explicitly forbidden from being represented as autumn 2026.

## Common-grid spectral workflow

The v3 seasonal spectral pipeline now completes successfully and CI is green:

- measured records: **73**;
- execution failures: **0**;
- comparison grid: **30 m**;
- exact source product IDs are required.

The workflow correctly refuses unreliable endpoint percentages:

- spring / forest pond: `not_quantifiable_by_current_strict_spectral_classifier`;
- spring / Lake Kuchnia: `not_quantifiable_sanity_gate_failed`;
- autumn / both objects: `endpoint_pending_missing_observation` because 2026 autumn does not yet exist.

This diagnostic failure is not hidden. TerraWater uses the stronger multi-year visible-footprint consensus for the current state-transition conclusion and keeps the strict spectral output as an uncertainty signal.

## Satellite evidence matrix

### Source 1 — NASA / USGS Landsat 5/7/8/9
Long historical optical record. Older multispectral detail is approximately 30 m and is never presented as true higher-resolution observation.

### Source 2 — ESA / Copernicus Sentinel-2
Recent optical control with relevant 10 m bands.

### Source 3 — ESA / Copernicus Sentinel-1 RTC
Independent radar measurement physics. Useful as a control but challenging for a small forested pond because canopy, wet soil and mixed pixels affect the return.

### Source 4 — NASA Terra ASTER
Selected fourth sensor family. The automated official NASA CMR query for `AST_L1T V004` found **77 spring/autumn catalog hits** for Experiment 001. ASTER is currently **catalog-verified**; each candidate granule still requires official pixel download and scene-level AOI/date/product/resolution/quality/SHA validation before it is counted as environmental evidence.

### Supplementary source — JAXA ALOS
AVNIR-2/PALSAR remains a useful candidate for the 2006–2011 era where exact official products can be retrieved and checked.

### Roscosmos / CNSA
These remain candidate agencies only. TerraWater will not claim a Roscosmos or CNSA observation unless an exact official, public, reproducible product for the AOI can be identified with date, mission/sensor, product ID, processing level, native resolution, access path and QA.

Four logos are not the objective. Four verifiable observations are.

## Arctic 90°N relation

The Polar repository's `docs/arctic-90n/` research module uses CryoSat, ICESat-2, Sentinel and SMOS concepts for polar validation. Those missions remain valuable for the 90°N hypothesis, but they are not automatically better evidence for a tiny forest pond. TerraWater selects sensors per scientific question and scale rather than reusing a satellite simply because it exists elsewhere on the site.

## Forensic findings retained

The evidence archive preserves rather than deletes problematic material. Known review cases include:

- 2002, 2012, 2013 alternate optical package: exact duplicate imagery assigned to different years;
- 1993: blank/broken alternate image and path/row concern;
- 1995: weak/cloudy imagery;
- 2010: broken/low-quality candidate imagery;
- 1997: visual agreement with contradictory QA/provenance;
- 2014: differing path/row with structural agreement, likely overlapping valid scenes;
- 2023: optical agreement with differing automated Sentinel-1 response.

Rejected or suspect material remains under `errors/do_wyjasnienia/` in the evidence repository with hashes and reasons. Two delivery servers for the same underlying acquisition are not counted as two independent observations of Earth.

## Current scientific conclusion

**Supported:** the long image record supports disappearance/near-total state transition of a historically persistent forest-pond visible-water feature. The repeat-supported historical footprint is on the order of **~1.6–2.2 ha**, with a central consensus of **~1.77 ha**.

**Not yet exactly quantified:** residual 2026 open-water m² and therefore exact percentage loss.

**Not established:** cause. Drought, precipitation, groundwater, drainage, blocked/altered connections, melioration, river-management effects, local channels and land-use change remain hypotheses requiring independent hydrological and meteorological evidence.

## AI training policy

Experiment 001 can be retained as the first **positive state-transition evidence case**, including its uncertainty metadata. It is not sufficient on its own to train a general water-recovery model.

The next research step is to document approximately **four additional independent cases** using the same provenance, seasonal, integrity and uncertainty rules. Only then should the project assemble the first multi-case training set, test on NVIDIA L4 and later scan the approximately 100 km region around Experiment 001 for similar state transitions.

## Authoritative evidence files in Polar-Sun-Moon-Analysis

- `experiments/experiment_001_pond_forest_kuchnia/EVIDENCE_POLICY.json`
- `experiments/experiment_001_pond_forest_kuchnia/measurements_visible_pond_consensus/visible_pond_consensus_measurement.json`
- `experiments/experiment_001_pond_forest_kuchnia/measurements_visible_pond_consensus/2000_historical_consensus_overlay.png`
- `experiments/experiment_001_pond_forest_kuchnia/measurements_visible_pond_consensus/2026_historical_consensus_on_recent_basin.png`
- `experiments/experiment_001_pond_forest_kuchnia/measurements/seasonal_water_measurements.json`
- `experiments/experiment_001_pond_forest_kuchnia/measurements/endpoint_1990_vs_2026.json`
- `experiments/experiment_001_pond_forest_kuchnia/seasonal_evidence/spring/manifest.json`
- `experiments/experiment_001_pond_forest_kuchnia/seasonal_evidence/autumn/manifest.json`
- `experiments/experiment_001_pond_forest_kuchnia/seasonal_evidence/late_summer_2026_proxy/manifest.json`
- `experiments/experiment_001_pond_forest_kuchnia/source4/nasa_aster/nasa_aster_scene_catalog.json`

## Experiment 001 phase decision

**Evidence phase closed sufficiently to start the next examples.** The exact 2026 autumn observation can be appended after the season occurs, and independent ASTER/ALOS pixels can strengthen the record later without blocking work on Experiment 002–005.

**Najpierw dowody, potem AI.**
