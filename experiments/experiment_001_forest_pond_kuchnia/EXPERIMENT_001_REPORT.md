# Experiment 001 — Forest Pond and Lake Kuchnia Water Loss (1990–2026)

## Purpose

This is the first formal evidence experiment for TerraWater AI. The experiment documents a suspected long-term loss of open water in a forest pond near Lake Kuchnia and uses Lake Kuchnia as an additional comparison target.

The project goal is to build an evidence-first, reproducible workflow that can later be repeated at several other sites. Only after approximately five independently documented evidence cases will the project consider L4 training and a systematic survey of lakes, ponds, rivers and canals within 100 km of Evidence 001.

## Exact area of interest

- Main analysis center: **53.591400, 19.010717**
- Standard image crop: **2 km × 2 km**, centered exactly on the coordinate above
- Study interval: **1990–2026 inclusive**
- Spring comparison: preferred **May**, with April/June fallback only when necessary and explicitly documented
- Autumn comparison: preferred **September**, with October/November fallback only when necessary and explicitly documented

## Scientific separation of statements

### OBSERVED

- Historical satellite imagery shows a clearly larger open-water signal in the forest-pond area than recent imagery.
- Recent imagery shows the pond as strongly reduced and in some scenes with little or no stable open-water signal.
- The change is large enough to justify formal monitoring and independent-source verification.
- The water state does not evolve monotonically every year; seasonal and interannual rebounds are possible.

### WORKING ESTIMATE — NOT YET FINAL

The current image-based working estimate is approximately **2.5 ha (25,000 m²) of lost open-water footprint**, with the forest pond appearing to have lost **close to 100%** of its earlier visible open-water area across roughly 36 years. Some older scenes visually suggest that the historic maximum may have been larger.

This number is deliberately labelled provisional. It must not be presented as a final measured value until corrected endpoint segmentation, pond geometry verification, seasonal comparison and uncertainty bounds are completed.

### NOT ESTABLISHED

The satellite imagery alone does **not** establish why the pond changed. Hypotheses involving drought, precipitation, drainage, blocked/altered connections, groundwater, river-management effects or other causes require independent hydrological and meteorological evidence.

## Evidence archive in Polar-Sun-Moon-Analysis

The image-heavy evidence is maintained on the dedicated branch:

`Terraforming-Planet/Polar-Sun-Moon-Analysis@annual-best-53-591400-19-010717`

Existing evidence products:

1. **Primary May series 1990–2026 (37 years)** — USGS/NASA Landsat + ESA/Copernicus Sentinel-2.
2. **Alternate delivery-path May series 1990–2025 (36 years)** — Google Cloud public Landsat + Element 84 Sentinel-2; 2022 is explicitly a non-independent fallback copied from the primary series.
3. **Sentinel-1 RTC radar series 2015–2025** — VV/VH, descending relative orbit 124, monthly May median composites.
4. **Image-first forensic audit** — hashes, cross-year duplicates, structural image registration, orientation, broken-image detection and optical/radar consistency checks.
5. **Experiment 001 corrected spring + autumn seasonal build** — generated under `experiments/experiment_001_pond_forest_kuchnia/` on the same Polar branch.

## Forensic audit findings that must remain part of the evidence record

The audit intentionally checked the image pixels before trusting dates or metadata.

### Alternate optical package errors

- **2002, 2012 and 2013:** exact byte-for-byte image duplication was found in the generated alternate-source package. These records are invalid as independent year observations and must not be used quantitatively until replaced.
- **1993:** alternate image was flagged as visually broken/blank and also conflicted in Landsat path/row with the primary record.
- **1995:** both optical deliveries were too cloudy/low-confidence for reliable water-area measurement.
- **2010:** primary image showed a broken/blank visual pattern; alternate scene had low local clear fraction.
- **1997:** the image itself strongly agrees across delivery paths, but provider/local QA values disagree substantially. This is treated as a QA/provenance issue, not evidence that the scene is fake.
- **2014:** path/row differs across products, but structural image agreement is good; likely overlapping valid Landsat scenes rather than falsification.
- **2023:** optical products agree strongly with each other, while one automatic radar-water-footprint test differs; this requires manual/seasonal review and is not labelled fake.

### Independence warning

Twenty-one years in the first two optical packages use the same acquisition date, platform and scene/path-row. They therefore verify delivery/processing consistency but are **not two independent observations of Earth**.

### Sentinel-1 integrity

No exact cross-year duplicate was found in the Sentinel-1 RTC series and no acquisition-date integrity failure was detected. Sentinel-1 provides genuinely different measurement physics from the optical series, although the small pond is challenging because tree canopy, wet soil and 10 m mixed pixels can contaminate the radar signal.

## Error-preservation policy

No suspect image is silently deleted. Copies are archived under:

`errors/do_wyjasnienia/`

with:

- source identifier,
- year,
- original path,
- archived path,
- SHA-256,
- reason for rejection/review,
- preservation status.

The original generated packages remain untouched for reproducibility.

## Corrected seasonal evidence design

### Spring

Target order:

1. May
2. April fallback
3. June fallback

The best locally usable scene is selected. A fallback month is permitted only when the preferred month cannot supply sufficiently reliable imagery, and that decision is written into the manifest.

### Autumn

Target order:

1. September
2. October fallback
3. November fallback

Autumn is added specifically to compare post-summer low-water conditions against spring conditions and to identify years where seasonal contraction was strongest.

### File naming

Every evidence image starts with year and date:

`YYYY_YYYY-MM-DD_satellite_resolution_...`

### Automatic integrity gate

- real public satellite pixels only;
- no generative AI gap filling;
- no AI super-resolution represented as observed detail;
- exact SHA-256 duplicate across different years is automatically rejected;
- visually blank/broken imagery is automatically rejected;
- cloud/valid-pixel quality is stored in the manifest;
- fallback months are explicit.

## Source families

| Family | Missions | Role | Limitations |
|---|---|---|---|
| NASA/USGS | Landsat 5/7/8/9 | long optical record | 30 m multispectral for older years; Landsat-7 SLC-off after 31 May 2003 |
| ESA/Copernicus optical | Sentinel-2 A/B/C | 10 m optical control | begins in 2015; no Sentinel-2 May 2015 because Sentinel-2A launched in June 2015 |
| ESA/Copernicus radar | Sentinel-1 RTC | radar control independent of cloud/optical appearance | pond is small and partly forested, so radar water classification can be low-confidence |
| Fourth-source candidates | NASA ASTER, JAXA ALOS/AVNIR-2/PALSAR, and only verifiable official Roscosmos/CNSA products | extra independent control | used only where legal public access, exact provenance and usable spatial resolution can be verified |

A source is never included merely to reach a target count of four. If an official Roscosmos or CNSA product cannot be independently downloaded and traced for this AOI, it remains a documented candidate rather than being represented as evidence.

## Measurement plan

The final area calculation will use original spectral/radar bands rather than display PNGs wherever possible.

For optical imagery:

- NDWI and/or MNDWI;
- cloud/shadow/snow masks;
- connected-component water extraction constrained to verified object geometry;
- m² and hectares;
- perimeter/pixel uncertainty;
- confidence classification.

For radar:

- consistent orbit/processing where possible;
- VV/VH thresholds/composite stability;
- radar used as independent confirmation rather than forcing agreement with optical masks.

## Endpoint evidence gate: 1990 versus 2026

The experiment will be considered quantitatively complete only after:

1. the forest-pond geometry is manually verified against the actual imagery;
2. corrected spring 1990 and 2026 endpoints are segmented;
3. autumn endpoints are segmented where usable;
4. the result includes uncertainty bounds;
5. independent sensor evidence is compared;
6. rejected/ambiguous scenes are excluded transparently;
7. the final conclusion is labelled **supported**, **not supported** or **inconclusive**.

## Alarm criterion

If the corrected analysis confirms near-total disappearance of a previously persistent ~hectare-scale open-water body, that state transition should be flagged by TerraWater as a **high-priority environmental monitoring anomaly**. An alarm means “requires investigation”; it does not by itself assign cause or blame.

## Planned next phase

After Evidence 001 is closed:

- identify approximately four additional evidence sites;
- repeat the same provenance, seasonal and cross-sensor protocol;
- build labelled training examples only from verified observations;
- later test the model on NVIDIA L4;
- then scan lakes, ponds, rivers and canals within **100 km** of Evidence 001 for similar long-term state transitions.

## Reproducibility links

Polar repository branch:

`https://github.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/tree/annual-best-53-591400-19-010717`

Primary May ZIP:

`https://raw.githubusercontent.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/annual-best-53-591400-19-010717/satellite_may_1990_2026/53.591400_19.010717/MAY_1990_2026_37_YEARS_2km_53.591400_19.010717.zip`

Alternate May ZIP:

`https://raw.githubusercontent.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/annual-best-53-591400-19-010717/satellite_alternate_source_may_1990_2025/53.591400_19.010717/ALT_SOURCE_MAY_1990_2025_36_YEARS_2km_53.591400_19.010717.zip`

Sentinel-1 RTC ZIP:

`https://raw.githubusercontent.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/annual-best-53-591400-19-010717/satellite_third_source_sentinel1_rtc_may_2015_2025/53.591400_19.010717/THIRD_SOURCE_SENTINEL1_RTC_MAY_2015_2025_WATER_2km_53.591400_19.010717.zip`
