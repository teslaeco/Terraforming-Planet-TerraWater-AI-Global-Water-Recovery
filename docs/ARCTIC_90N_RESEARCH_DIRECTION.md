# Arctic 90°N Research Direction — Build for Good / TerraWater AI

## Status

Concept note connected to the **TerraWater AI — Global Water Recovery Observatory** project for the current **Build for Good** developer challenge.

This is a research and engineering direction, not a claim that a finished station design already exists.

## Core idea

A permanently positioned or dynamically station-kept scientific platform near the geographic North Pole (90°N) could provide continuous in-situ measurements that complement official satellite Earth-observation products.

For TerraWater AI, the main relevance is the coupled monitoring of:

- sea ice and snow,
- melt ponds and open leads,
- ocean temperature and salinity,
- under-ice currents,
- ocean-to-ice heat exchange,
- atmospheric conditions,
- long-term water and ice change.

The station would not replace satellites. Its value would be to provide a carefully characterized physical reference point that can be synchronized with selected satellite overpasses and products.

## Why AI matters

A 90°N station could generate synchronized streams from many instruments: GNSS, meteorological sensors, radiometers, optical and thermal cameras, LiDAR, radar, snow and ice probes, CTD chains, ADCP current profilers and upward-looking sonar.

AI can help by:

1. aligning measurements in time and space with satellite observations;
2. detecting disagreement between satellite-derived products and direct measurements;
3. distinguishing snow, ridged ice, melt ponds, leads and open water;
4. estimating uncertainty instead of returning only one predicted value;
5. detecting sensor drift, dropout or calibration problems;
6. building multimodal training and validation datasets;
7. generating evidence summaries that separate observed facts from hypotheses.

## Connection to TerraWater AI

TerraWater AI is designed around evidence provenance: observed data, derived metrics, candidate causes, verification requirements and confirmed findings are kept separate.

The same evidence model can be used for polar monitoring. A future station could feed TerraWater AI with direct measurements and compare them against official products from missions and services such as:

- ESA CryoSat,
- NASA ICESat-2,
- Sentinel-1,
- Sentinel-2 where illumination and cloud conditions permit,
- SMOS and other microwave products,
- Copernicus environmental and climate products.

Coverage near 90°N depends on orbital inclination, sensor swath and product design. The North Pole should therefore not be described as a universal blind spot for every satellite.

## Engineering questions before feasibility can be claimed

A station intended to remain close to 90°N would require quantitative analysis of:

- pack-ice drift and deformation,
- pressure ridges and underwater ice keels,
- structural ice loads,
- station-keeping force and propulsion power,
- redundancy and failure modes,
- polar-night energy management,
- communications,
- maintenance, evacuation and environmental safety.

Possible architectures could include an ice-capable dynamically positioned vessel, a semi-submersible platform below the deepest ice keels, or another hybrid concept. No architecture should be selected before force, energy and reliability models are complete.

## Data principles

Only legal, official and publicly available scientific data should be used wherever possible. Every measurement and AI output should preserve provenance, including:

- source sensor,
- acquisition time,
- product or instrument identifier,
- processing version,
- uncertainty,
- calibration state,
- model version,
- link to the original or authoritative source where available.

Synthetic imagery, interpolation and AI-generated visualizations must never be presented as real satellite observations.

## Next technical deliverable

The next useful step is a quantitative feasibility model rather than a visual rendering. It should contain:

1. environmental design envelope;
2. ice-load assumptions;
3. station-keeping force model;
4. propulsion and energy budget;
5. sensor architecture;
6. satellite-overpass synchronization plan;
7. TerraWater evidence schema mapping;
8. AI validation workflow;
9. failure-mode analysis;
10. staged prototype and test plan.
