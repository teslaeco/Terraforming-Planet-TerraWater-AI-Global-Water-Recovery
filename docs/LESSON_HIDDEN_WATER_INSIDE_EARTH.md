# Lesson — Hidden Water Inside Earth: What We Know and What We Still Cannot Measure Exactly

## Core idea

No scientific inventory describes every litre of water on Earth with perfect certainty. Large surface reservoirs are comparatively well constrained, but water stored in fractured rock, deep crust and the mantle is much harder to quantify and map in three dimensions.

This does **not** mean that subsurface science is guesswork. It means that different parts of the water system are known with very different levels of uncertainty and from different types of evidence.

## Water in rock is not always a hidden underground river

Subsurface water exists in several forms:

- liquid water in pores and fractures;
- groundwater in sedimentary and fractured-rock aquifers;
- fluids under pressure in faults and fracture systems;
- water or hydroxyl structurally bound in minerals;
- water transported through the mantle over geological time.

Crystalline rock is not automatically a giant sponge. USGS notes that its primary pore space can be extremely small; meaningful groundwater flow commonly depends on connected fractures. In fractured-rock aquifers, hydraulic properties can vary by orders of magnitude over short distances and the three-dimensional fracture network can be difficult to reconstruct.

## The 2014 ringwoodite result

In 2014, Pearson et al. reported hydrous ringwoodite preserved inside a diamond derived from the deep mantle. Spectroscopic measurements showed that the inclusion contained water and provided direct evidence that **at least locally** the mantle transition zone is hydrous, at about **1 wt%** in that sample.

The mantle transition zone lies roughly between **410 and 660 km** depth. Laboratory studies show that high-pressure minerals such as wadsleyite and ringwoodite can store substantial amounts of water — up to about **2.5 wt%** under some conditions.

### Important correction to the popular “third ocean” phrase

Descriptions such as “one to several oceans of water inside Earth” are **model- and storage-capacity estimates**, not a direct measurement of a continuous hidden liquid ocean.

The 2014 Nature paper itself states that the global abundance of water in the transition zone remains controversial. A hydrous mineral inclusion proves that water can be present there and that at least some regions are wet; it does not determine the exact global inventory.

## Why deep water is difficult to map

### Ground-penetrating radar

GPR penetration is strongly site dependent. Conductive materials, clay, water content and mineralogy can attenuate radar severely. USGS studies show useful penetration ranging from only a few metres in difficult material to tens of metres or more in favourable settings. Therefore statements such as “radar always reaches X metres” are scientifically unsafe.

### Seismology

Seismic waves are essential for imaging deep Earth structure, but they measure physical contrasts indirectly. Large layers and broad anomalies can be resolved much better than very small fractures or complicated fluid pathways. Interpretations depend on resolution, geometry and the physical model used.

### Boreholes and mines

A borehole gives high-value direct local evidence, but it samples only a very small part of a three-dimensional rock mass. In fractured rock, nearby boreholes can intersect different fracture systems. Unexpected groundwater inflows in engineering and mining are one practical demonstration that local subsurface flow pathways can remain poorly constrained until they are intersected.

## What science can and cannot currently say

Science **can** measure many aquifers, water levels, pressures, flow rates, rock properties and geophysical signals very accurately at specific locations.

Science **cannot** currently provide a globally exact litre-by-litre map of all water held in every fracture, pore, deep crustal system and hydrous mineral throughout Earth.

The scientifically useful statement is therefore:

> The uncertainty of Earth’s water inventory is not uniform. Surface oceans and major ice reservoirs are relatively well constrained, while some deep subsurface and mantle reservoirs remain inferred from sparse direct samples, geophysics, laboratory mineral physics and numerical models.

## Why this matters for TerraWater AI

A trustworthy planetary water model must distinguish **measurement type and uncertainty**, rather than render every pixel as equally certain.

Recommended evidence classes:

- `DIRECT_MEASUREMENT`
- `DERIVED`
- `MODEL_ESTIMATE`
- `INTERPOLATED`
- `REMOTE_SENSING`
- `IN_SITU`
- `UNKNOWN`
- `DATA_GAP`

Each value should retain:

- source;
- acquisition time;
- spatial support / resolution;
- uncertainty;
- method;
- model version where applicable;
- calibration state;
- whether the value is direct or inferred.

## Connection to the 90°N observatory concept

A fixed 90°N observatory would not solve the unknown global deep-water inventory by itself. Its scientific value would be narrower but important: provide one stable, continuously instrumented reference column from seabed through ocean, sea ice and atmosphere, connected to satellite observations.

The broader Terraforming Planet objective should be to build a 3D Earth model that makes uncertainty visible. A missing measurement should remain a **data gap**, not be silently turned into an apparently exact value.

## Primary references

1. Pearson, D. G. et al. (2014), *Hydrous mantle transition zone indicated by ringwoodite included within diamond*, Nature 507, 221–224. DOI: https://doi.org/10.1038/nature13080
2. Schmandt, B. et al. (2014), *Dehydration melting at the top of the lower mantle*, Science 344, 1265–1268. DOI: https://doi.org/10.1126/science.1253358
3. U.S. Geological Survey, *Fractured-rock aquifers, understanding an increasingly important source of water*. DOI: https://doi.org/10.3133/fs11202
4. U.S. Geological Survey studies on ground-penetrating radar performance and attenuation in different hydrogeological settings.
