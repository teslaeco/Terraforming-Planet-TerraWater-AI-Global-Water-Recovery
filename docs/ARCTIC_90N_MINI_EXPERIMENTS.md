# Arctic 90°N — Mini-Experiment Lab

**Status:** interactive screening/demo only — not CFD, FEM, tsunami forecasting, geotechnical certification, or a construction design.

Public interactive laboratory:

- https://terraforming-planet.github.io/Polar-Sun-Moon-Analysis/arctic-90n/mini-experiments-lab.html

The concept is deliberately split into small experiments so that each assumption can be changed independently and its first-order consequence can be inspected.

## Experiment 1 — base-width sweep

Baseline assumptions: total height 8 km, summit width 0.5 km, water depth 4 km, square-frustum geometry.

| Base width | Volume | Rock mass | Mean effective base pressure | Mean flank angle |
|---:|---:|---:|---:|---:|
| 8 km | 182.0 km³ | 4.914×10¹⁴ kg | 51.0 MPa | 64.9° |
| 12 km | 400.7 km³ | 1.082×10¹⁵ kg | 49.7 MPa | 54.3° |
| 16 km | 704.7 km³ | 1.903×10¹⁵ kg | 49.0 MPa | 45.9° |
| 20 km | 1094.0 km³ | 2.954×10¹⁵ kg | 48.6 MPa | 39.4° |
| 24 km | 1568.7 km³ | 4.235×10¹⁵ kg | 48.4 MPa | 34.2° |

**First useful finding:** widening the base strongly reduces the geometric flank angle, but average base pressure drops only slightly because a wider mountain requires much more rock mass.

## Experiment 2 — target flank angle

The lab solves the geometric base width required for a chosen flank angle. This is intentionally labeled as geometry only; it is not a safe-angle criterion.

For h=8 km and summit width 0.5 km, approximate base widths are:

- 45° → ~16.5 km;
- 35° → ~23.4 km;
- 30° → ~28.2 km;
- 25° → ~34.8 km;
- 20° → ~44.5 km.

## Experiment 3 — source excavation

The user selects the diameter of a circular source area and the lab calculates the mean excavation depth required to supply the currently selected mountain volume.

This immediately shows why an 8 km source crater is not a realistic first-pass source for the baseline 182 km³ mountain: the mean depth would be roughly 3.6 km before accounting for side slopes, unusable material, bulking, environmental buffers, geology or construction losses.

## Experiment 4 — current-drag proxy

The page sweeps current speed and applies a simple `0.5 rho Cd A v²` proxy. It is useful for seeing the square-law sensitivity to velocity, but it is explicitly not a CFD load result.

## Experiment 5 — sea-ice encounter proxy

No absolute ice force is claimed. The lab uses a dimensionless sensitivity index proportional to `base width × ice-drift speed²`, normalized to the 8 km / 0.08 m/s baseline. The purpose is to show how quickly a simple encounter proxy grows with drift speed while making clear that real pressure-ridge mechanics require a dedicated sea-ice model.

## Experiment 6 — rapid-failure source volume

The user changes the rapid-failure fraction and the page reports only the corresponding moving rock volume plus the shallow-water long-wave propagation speed for the selected water depth.

It does **not** infer tsunami height. NOAA notes that landslide-tsunami generation depends on displaced material, motion speed and depth; a coupled landslide–water model is required.

## Experiment 7 — static submerged-volume equivalent

The lab shows the submerged structure volume and a simple global mean sea-level equivalent only for the thought experiment where that solid volume is added from outside the ocean basin. If construction material comes from the same seabed, this is not a net sea-level model.

## Experiment 8 — material-vs-slope trade-off

This experiment visualizes the central design conflict: progressively wider bases make the mountain geometrically gentler but increase the required rock volume very rapidly.

The current lesson is therefore **not** “make the base wider and the problem is solved.” The useful design question is how to jointly optimize:

- total height;
- above-water height;
- summit size;
- terraces;
- buttressing/cellular architecture;
- source-material volume;
- foundation loading;
- ice interaction;
- hydrodynamic wake;
- failure consequences.

## Scientific references used by the screening page

- NOAA — Tsunami Generation: Landslides.
- NSIDC — Science of Sea Ice / pressure ridges.
- USACE EM 1110-2-1902 — Slope Stability.
- USGS — submarine landslide and tsunami studies.

The experiment lab is designed to expose uncertainty and trade-offs. A result from the page should remain `SCREENING_SCENARIO` until replaced by validated numerical or observational evidence.
