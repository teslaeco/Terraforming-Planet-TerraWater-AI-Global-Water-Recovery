# Arctic 90°N Research Direction — Build for Good / TerraWater AI

## Status

Concept note connected to the **TerraWater AI — Global Water Recovery Observatory** project for the current **Build for Good** developer challenge.

This is a research and engineering direction, not a claim that a finished station design already exists.

## Core idea

A permanently fixed scientific reference station at the geographic North Pole (90°N) could provide a type of long-duration, repeatable in-situ reference that drifting ice camps cannot provide by geometry alone.

The station would not replace satellites, drifting observatories, buoys, ships or aircraft. Its value would be to add a **fixed geodetic reference point** that can be revisited continuously for years and synchronized with selected satellite products.

For TerraWater AI, the main relevance is the coupled monitoring of:

- sea ice and snow,
- melt ponds and open leads,
- ocean temperature and salinity,
- under-ice currents,
- ocean-to-ice heat exchange,
- atmospheric conditions,
- long-term water and ice change,
- meteorology and air-quality measurements,
- communications experiments for high-latitude scientific infrastructure.

## Critical scientific note — what 88°N actually means

This distinction must be explicit.

**ESA CryoSat reaches approximately 88° north and south on every orbit.** That is a documented orbital coverage property of CryoSat; it is not a theory about where the North Pole is and it is not proof that all satellites have the same polar gap.

Official ESA reference:

- https://www.esa.int/Applications/Observing_the_Earth/FutureEO/CryoSat/Satellite

The area between the maximum latitude reached by a specific satellite and the exact geographic pole therefore has to be treated according to that mission's orbit, sensor swath and product design. TerraWater AI must never generalize the CryoSat 88° limit to every Earth-observation mission.

At the same time, a second issue is different from satellite orbital coverage: **the lack of a permanent, fixed, long-duration physical reference station exactly at 90°N.**

Drifting observatories and autonomous buoys are scientifically valuable and can produce calibrated measurements. The MOSAiC expedition, for example, deliberately used the drifting ice as a research platform and produced coordinated atmosphere–snow–ice–ocean measurements. Those data should not be described as invalid.

Official AWI references:

- https://www.awi.de/en/focus/mosaic-expedition.html
- https://www.awi.de/en/science/climate-sciences/physical-oceanography/projects/mido.html

However, a drifting platform is **not equivalent to a fixed geodetic benchmark**. Its position, orientation, local ice geometry and surrounding surface conditions change with time. These changes can be measured and corrected with GNSS and calibration procedures, but they add another layer of geometry, collocation and representativeness that a truly fixed reference site would reduce.

Therefore the scientifically defensible statement for this project is:

> Existing drifting stations provide real and valuable measurements, but humanity still lacks a permanent, fixed, multi-year in-situ reference observatory located exactly at the geographic North Pole. Such a station could reduce an important class of uncertainty in long-term satellite/ground comparison, although it would not eliminate all measurement uncertainty and would not make every satellite product automatically exact.

The objective is **not to claim that current Arctic science is wrong**. The objective is to create an additional reference standard that current observing systems do not provide.

## Why AI matters

A 90°N station could generate synchronized streams from many instruments: GNSS, meteorological sensors, radiometers, optical and thermal cameras, LiDAR, radar, snow and ice probes, CTD chains, ADCP current profilers and upward-looking sonar.

AI can help by:

1. aligning measurements in time and space with satellite observations;
2. detecting disagreement between satellite-derived products and direct measurements;
3. distinguishing snow, ridged ice, melt ponds, leads and open water;
4. estimating uncertainty instead of returning only one predicted value;
5. detecting sensor drift, dropout or calibration problems;
6. building multimodal training and validation datasets;
7. generating evidence summaries that separate observed facts from hypotheses;
8. tracking how changing local geometry affects comparison between drifting and fixed measurements;
9. maintaining a long-term provenance ledger for every calibration event, sensor replacement and processing revision.

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

## Megastructure concept — fixed artificial research island at 90°N

A second concept to investigate is more ambitious than a dynamically positioned vessel: **constructing a permanent artificial research island / seabed-supported megastructure whose geometric reference point is fixed at 90°N.**

The purpose would be scientific, environmental and civilizational: create a stable location from which the same atmosphere, ocean, ice and Earth-observation measurements can be repeated for decades with a known reference geometry.

### Initial geometry for simulation — not an approved design

The current conceptual starting envelope is:

- geographic reference: **90°N**;
- nominal seabed footprint: approximately **8 km × 8 km**;
- conceptual total vertical scale: approximately **7 km**;
- working assumption for first simulations: roughly **4 km below mean sea level plus up to 3 km above sea level**;
- external form: **tapered pyramid / truncated-pyramid (frustum) geometry** intended to avoid vertical walls and distribute environmental loads over a large area;
- construction material concept: primarily mineral/rock material sourced only if future geological, legal and environmental studies show extraction can be performed acceptably.

These numbers are **placeholders for numerical modeling**, not construction dimensions. The exact bathymetry and geology at the selected reference point must be surveyed before any geometry can be accepted. An 8 km × 8 km base and 7 km height represents an extreme megastructure; if it were a perfect pyramid tapering to a point, its geometric volume alone would be about **149 km³**, before foundations, voids, protection layers or a usable summit are considered. A truncated pyramid with a substantial top platform would require even more volume.

### Why a tapered form is being considered

The hypothesis is that a wide, sloped structure may distribute ice, wave and current interactions differently from a narrow vertical tower. This is only a design hypothesis. It must be tested with computational fluid dynamics, ice–structure interaction models, physical basin tests and geotechnical analysis.

The project must not state in advance that this geometry will reduce hydrodynamic or ice loads enough to be feasible.

### Seabed and foundation concept

The first engineering study should evaluate:

1. high-resolution bathymetry around the exact 90°N reference;
2. sediment thickness and mechanical properties;
3. bedrock depth and composition;
4. slope stability and possible excavation geometry;
5. foundation settlement over decades;
6. seismic and tectonic environment;
7. scour from currents;
8. thermal effects on seabed and permafrost-like sediments if present;
9. how the structure would alter local and regional circulation.

The idea of excavating a recessed foundation and building upward from the seabed can be kept as one candidate architecture, but no excavation should be proposed until the environmental and geotechnical model is complete.

### Redundant reinforcement concept

If one central summit or core is structurally unrealistic, the alternative research path is a **broader, lower-gradient artificial landform** with multiple structural cells, buttresses or satellite foundation zones connected through a ring-like support system.

This must remain a modeling concept until engineers can show that it improves safety without creating unacceptable impacts on ocean circulation, habitat, sediment transport or ice dynamics.

## Why the project must not 'build first and see what happens'

The environmental objective requires the opposite approach:

**model → measure → simulate → independently review → prototype at small scale → reassess → only then consider construction.**

A structure of this scale could itself alter water circulation, sea-ice movement, sediment transport, ecosystems and atmospheric boundary conditions. Those effects are scientifically interesting, but they must be predicted and bounded before construction rather than discovered through an irreversible full-scale experiment.

This project therefore treats environmental protection as a hard design constraint, not as a secondary feature.

## International scientific governance

A permanent 90°N installation cannot be treated as an ordinary private construction project. It would require international legal, environmental, safety and scientific governance.

UNCLOS contains specific rules concerning artificial islands, installations, continental-shelf rights and marine scientific research. Artificial installations do not automatically become sovereign natural islands, and the legal status of the seabed and any applicable coastal-state rights would need to be resolved before development.

Official UN references:

- https://www.un.org/depts/los/convention_agreements/texts/unclos/part5.htm
- https://www.un.org/depts/los/convention_agreements/texts/unclos/part6.htm
- https://www.un.org/depts/los/convention_agreements/texts/unclos/part7.htm
- https://www.un.org/depts/los/convention_agreements/texts/unclos/part13.htm

A realistic governance concept would therefore involve an international scientific consortium rather than unilateral construction.

## Environmental and polar safety framework

Any ship-based construction phase, logistics fleet or mobile support system would need to account for applicable polar safety and pollution-prevention requirements. The IMO Polar Code covers design, construction, equipment, operations, training, search and rescue and environmental protection for ships operating in polar waters.

Official IMO reference:

- https://www.imo.org/en/ourwork/safety/pages/polar-code.aspx

The fixed megastructure itself would also require a broader project-specific environmental assessment beyond ship regulations.

## Scientific measurement architecture

A mature station concept should include vertically distributed sensing from the seabed to the upper atmosphere.

### Seabed and deep ocean

- pressure and sea-level reference sensors;
- seismology and geotechnical monitoring;
- deep CTD and temperature chains;
- ADCP current profilers;
- acoustic tomography research;
- sediment and benthic monitoring;
- long-term heat-flux measurements.

### Water column and under-ice zone

- current profiling at multiple depths;
- temperature, salinity and dissolved oxygen;
- upward-looking sonar for ice draft;
- under-ice optical/acoustic systems;
- biogeochemical sensors;
- autonomous underwater vehicle docking and calibration points.

### Surface and ice

- precision GNSS reference monuments;
- radar and laser altimetry reference targets;
- snow depth and density;
- ice thickness and temperature;
- melt-pond/open-water classification cameras;
- radiometers and albedo measurements.

### Atmosphere

- full meteorological station;
- wind profiles;
- cloud and aerosol measurements;
- radiation balance;
- atmospheric chemistry and air-quality sensors;
- radiosonde / drone / tethered-platform support.

## Communications and polar data relay research

A permanent 90°N facility could also be studied as a high-latitude communications and data-relay node for science. Potential research includes:

- continuous scientific data uplink/downlink;
- redundant satellite communications;
- optical communications experiments;
- relay support for polar-orbiting observation missions where technically and legally appropriate;
- emergency communications for Arctic science and logistics;
- distributed data caching and edge AI processing.

The project must not claim that one powerful transmitter would automatically 'fix the Internet in space'. Spectrum coordination, interference limits, orbital geometry, network architecture and international telecommunications rules would determine what is actually possible.

## Water-cycle and planetary understanding

The long-term scientific goal is larger than sea ice alone. A fixed polar observatory could contribute to understanding how water moves through the coupled Earth system:

- ocean circulation and freshwater storage;
- sea-ice formation and melt;
- atmospheric moisture transport;
- precipitation and evaporation;
- river inflow to the Arctic Ocean;
- groundwater and subsurface storage where measurable through other global networks;
- links between polar processes and global weather/climate models.

No single station can directly measure the total water stored inside all mountains, aquifers or continents. The value of the 90°N station would be to provide one exceptionally stable reference node within a much larger global observing network.

The same evidence-first principle can then support practical water-management research elsewhere: drought, flood retention, wetlands, reservoirs, agriculture and restoration in arid regions. TerraWater AI should use these data to improve understanding and decision support, not to promise that a single intervention can solve global drought or flood problems.

## Engineering questions before feasibility can be claimed

A fixed 90°N island or station would require quantitative analysis of:

- bathymetry and seabed geology;
- material availability and transport;
- foundation loads and settlement;
- pack-ice drift and deformation;
- pressure ridges and underwater ice keels;
- structural ice loads;
- waves and currents;
- ocean-circulation perturbation;
- sediment transport and scour;
- ecological impact;
- construction emissions and pollution risk;
- polar-night energy management;
- communications;
- maintenance, evacuation and environmental safety;
- multi-decade inspection and repair;
- decommissioning or long-term stewardship.

## Data principles

Only legal, official and publicly available scientific data should be used wherever possible. Every measurement and AI output should preserve provenance, including:

- source sensor,
- acquisition time,
- product or instrument identifier,
- processing version,
- uncertainty,
- calibration state,
- platform position/orientation where relevant,
- model version,
- link to the original or authoritative source where available.

Synthetic imagery, interpolation and AI-generated visualizations must never be presented as real satellite observations.

## Execution roadmap — research before construction

This is the proposed staged path for turning the idea into a falsifiable engineering program.

### Phase 0 — Scientific question definition

- define exactly which current measurements are insufficient;
- identify which uncertainty would be reduced by a fixed 90°N reference;
- compare against existing satellites, MOSAiC, buoys, aircraft and icebreakers;
- define success metrics before designing the structure.

### Phase 1 — 90°N digital site model

- compile official bathymetry, gravity, geology, currents, sea ice and weather data;
- create a 3D digital twin of the candidate area;
- quantify uncertainty in every input dataset;
- identify additional surveys required.

### Phase 2 — Megastructure feasibility models

Compare at minimum:

- fixed seabed tower;
- wide tapered pyramid/frustum island;
- broad low-gradient artificial landform;
- multiple connected foundation cells;
- semi-submersible station;
- dynamically positioned ice-capable platform;
- hybrid fixed/mobile observatory.

Reject architectures that cannot meet environmental, structural or legal constraints.

### Phase 3 — Environmental impact simulation

Before excavation or material placement, model:

- local and regional current changes;
- sea-ice drift and pressure redistribution;
- sediment plumes and seabed disturbance;
- habitat impact;
- air and water pollution risks;
- construction noise;
- cumulative multi-decade effects.

Independent scientific review should be mandatory.

### Phase 4 — Scaled physical testing

- wave/ice basin models;
- material and freeze-thaw testing;
- foundation prototypes in non-sensitive test environments;
- sensor calibration network tests;
- autonomous maintenance experiments.

### Phase 5 — Small Arctic demonstrator

Only after prior phases pass:

- deploy a small removable scientific platform;
- validate sensors and communications;
- compare fixed-reference and drifting measurements;
- measure actual environmental disturbance;
- update models with observed data.

### Phase 6 — International decision gate

A full artificial island should proceed only if independent science demonstrates that:

- the measurement benefit is real and substantial;
- no lower-impact architecture can deliver the same scientific value;
- structural feasibility is demonstrated;
- environmental risk is acceptable and mitigated;
- legal authority and international agreements are clear;
- long-term funding, safety and stewardship are secured.

Only after this gate should detailed construction design begin.

## Project principle

The motivation is the long-term safety and knowledge of future generations. That goal requires more than dramatic construction: it requires **measurements that can be trusted, uncertainty that is visible, engineering that can be independently checked, and environmental effects that are understood before they are imposed.**

The 90°N concept should therefore be judged by one standard: does it create scientifically valuable information that cannot be obtained more safely, accurately and efficiently by a lower-impact system?

If the answer is eventually yes, the project can progress. If the answer is no, TerraWater AI should preserve the scientific objective and choose the better architecture.
