# Experiment 001 — current best forest-pond measurement update

## Why the number changed

The earlier **~2.5 ha / near-100%** statement was intentionally kept as a working visual estimate. After the pond geometry was corrected and the same historical feature was extracted independently from several clear older annual images, a repeatable multi-year footprint could be measured.

The central result is now **smaller and better supported** than the original 2.5 ha estimate.

## Method

- fixed 2 km × 2 km geographic crop;
- corrected forest-pond basin around **53.594595, 19.000140**;
- seven clear historical primary images: **1998, 1999, 2000, 2004, 2005, 2006, 2008**;
- deterministic visible-component extraction on each year;
- consensus based on how many years independently reproduce the same footprint;
- 1990 image used as an endpoint consistency check;
- 2026 old footprint overlaid onto the recent changed/drier basin;
- this is an **image-visible footprint measurement**, not a claim of metre-perfect spectrally pure open water.

## Result

- central persistent historical footprint (supported by at least 4 of 7 clear years): **17,722.2 m² = 1.7722 ha**
- conservative lower footprint (>=5 of 7): **16,269.3 m² = 1.6269 ha**
- repeat-supported upper footprint (>=2 of 7): **21,642.0 m² = 2.1642 ha**
- broad one-or-more-year union envelope: **23,978.3 m² = 2.3978 ha**
- 1990 dark component overlaps **16,398.1 m²**, or **92.53%** of the central persistent consensus footprint

Individual older extracted component areas range roughly **1.55–2.08 ha** in the selected clear years.

## 2026 state

The same historical footprint overlays a visibly changed/drier basin in 2026. There is no comparable persistent dark-water shape in the recent image. May and August 2026 spectral diagnostics at the corrected pond location are strongly non-water-like.

The exact residual open-water m² is deliberately **not forced** because forest canopy, wet soil, shadow and mixed pixels can confuse a strict spectral classifier.

## Current evidence statement

The strongest defensible statement at this stage is:

> The image record supports a **near-total state transition** of a historically persistent pond footprint on the order of **~1.6–2.2 ha**, with a central repeatable estimate of **~1.77 ha**. A broad historic envelope can approach **~2.40 ha**. The former ~2.5 ha estimate is retained as an upper visual hypothesis, not the central result.

The exact final percentage remains uncertainty-gated, but the qualitative conclusion — that the old persistent water feature has essentially disappeared as the same type of open-water feature — is strongly supported by the image sequence.

## Authoritative result

JSON:
https://github.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/blob/annual-best-53-591400-19-010717/experiments/experiment_001_pond_forest_kuchnia/measurements_visible_pond_consensus/visible_pond_consensus_measurement.json

2000 historical footprint overlay:
https://raw.githubusercontent.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/annual-best-53-591400-19-010717/experiments/experiment_001_pond_forest_kuchnia/measurements_visible_pond_consensus/2000_historical_consensus_overlay.png

2026 same historical footprint on recent basin:
https://raw.githubusercontent.com/Terraforming-Planet/Polar-Sun-Moon-Analysis/annual-best-53-591400-19-010717/experiments/experiment_001_pond_forest_kuchnia/measurements_visible_pond_consensus/2026_historical_consensus_on_recent_basin.png
