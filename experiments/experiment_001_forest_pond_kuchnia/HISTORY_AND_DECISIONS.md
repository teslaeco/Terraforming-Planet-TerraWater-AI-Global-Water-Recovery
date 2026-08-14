# Experiment 001 — research history and decisions

This file mirrors the evidence-history record maintained in the Polar satellite repository so TerraWater preserves not only the final result but also the decisions, corrections and hypotheses that led to it.

## AOI and period

- **53.591400, 19.010717**
- standard comparison crop: **2 km × 2 km**
- **1990–2026**
- targets: forest pond + Lake Kuchnia

## Initial observation

Repeated inspection of real satellite imagery showed a much larger historical open-water footprint in the forest-pond area than in recent imagery. Recent scenes show the pond strongly reduced or apparently absent.

## Causal hypothesis — not established

The user proposed that local water decline may involve more than the simple explanation “it did not rain,” including possible effects of water routing, drainage, blocked/altered channels, retention, river/lake connectivity and management of water ultimately moving toward the Vistula/basin system.

This remains a **hypothesis to test**, not a finding. Causation requires hydrological, meteorological, groundwater and infrastructure evidence independent of satellite appearance.

## Why spring and autumn

Spring was selected to observe wetter/early-season conditions before strongest summer drying. Poor April scenes led to a May-focused series, with replacement searches when imagery was cloudy/broken.

Autumn was added to examine likely post-summer contraction:

- spring priority: May → April → June fallback;
- autumn priority: September → October → November fallback.

Every fallback is explicitly documented.

## Resolution rule

Native detail is never equalized by pretending upscaling creates information. Older Landsat imagery is mostly 30 m multispectral; Sentinel-2 provides 10 m natural-color bands in the modern period. Cross-era quantitative measurement therefore uses a common **30 m grid**, while display products retain best available native detail.

## Three-source history

1. USGS/NASA Landsat + ESA Sentinel-2 primary optical record.
2. Alternate public delivery-path optical record. Later forensic audit showed many years were the same underlying observation and found package corruption in 2002/2012/2013.
3. Sentinel-1 RTC VV/VH radar, a genuinely different measurement physics control for 2015–2025.

## Image-first forensic decision

Dates are not trusted merely because a filename/manifest says they are correct. The audit checks pixels first: hashes, cross-year duplicates, structural alignment, orientation, broken/blank patterns and optical/radar geographic agreement.

Key retained findings:

- alternate 2002/2012/2013 = exact duplicate file corruption;
- alternate 1993 = broken/path-row conflict;
- 1995 = poor optical quality;
- 2010 = problematic imagery;
- 1997 = image agreement but QA disagreement;
- no exact cross-year duplicate in the audited primary or Sentinel-1 sets;
- no evidence that official operators falsified imagery; the confirmed concrete errors were in our generated package/pipeline.

## Error policy

Bad/suspect images are preserved rather than deleted. The Polar repository stores copies under `errors/do_wyjasnienia/` with SHA-256, original path and reason. Originals remain untouched for reproducibility.

## Corrected spring examples

The corrected build found better seasonal replacements, including:

- 1995 → 1995-04-23 Landsat-5;
- 1997 → 1997-04-19 Landsat-5;
- 2010 → 2010-06-18 Landsat-7 after bad May/April candidates;
- 2011 → 2011-04-19 Landsat-5.

## Working Evidence 001 statement

Strong visual observation: the forest pond has undergone a very large state transition and recent imagery shows little or no persistent open-water footprint compared with historical scenes.

Working magnitude only: **~2.5 ha / 25,000 m², near 100% open-water loss**. This remains **provisional**, because some historical scenes appear larger and the final number requires common-grid spectral measurement, manual pond geometry verification and uncertainty bounds.

If confirmed, TerraWater should flag this as a high-priority environmental monitoring anomaly requiring investigation. The alarm does not diagnose a cause.

## Fourth-source search

- NASA ASTER: official CMR catalog search found 77 spring/autumn AOI granule hits; pixels not yet admitted until official download and integrity validation.
- JAXA ALOS AVNIR-2/PALSAR: strong 2006–2011 candidate; official download requires G-Portal login.
- CNSA Gaofen: candidate pending exact official Poland AOI access/product verification.
- Roscosmos EO holdings: candidate pending exact official public/legal Poland AOI product verification.

The experiment will not add an agency merely to make the source count look larger.

## Longer-term TerraWater/Test-512 plan

After Evidence 001 is closed rigorously, collect about five similarly documented evidence sites, build human-verified labels while preserving untouched originals, then test/train on NVIDIA L4. The next local deployment target is systematic review of lakes, ponds, rivers and canals within **100 km** of Evidence 001. The broader TerraWater/Test-512 concept can then scale verified examples across many regions/countries rather than assuming one local case generalizes globally.

Authoritative image-heavy record:

https://github.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/tree/annual-best-53-591400-19-010717/experiments/experiment_001_pond_forest_kuchnia
