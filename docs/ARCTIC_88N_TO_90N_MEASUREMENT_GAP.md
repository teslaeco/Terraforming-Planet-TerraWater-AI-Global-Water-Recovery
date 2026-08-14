# Arctic 88°N → 90°N Measurement Gap — Scientific Position

## Purpose

This note defines the scientific position used by TerraWater AI for the high-Arctic 90°N research concept.

The goal is **not** to claim that current satellite missions or drifting Arctic observatories are useless or invalid. The goal is to distinguish three different things that are often mixed together:

1. the known orbital coverage limit of a satellite;
2. the uncertainty of the satellite-derived geophysical product;
3. the absence of a permanent, fixed, multi-year in-situ reference observatory exactly at 90°N.

These are different problems and they must be treated separately.

## 1. What 88°N means — and what it does not mean

For ICESat-2 and CryoSat, approximately 88°N/S is a documented consequence of mission orbit geometry. It is **not an estimated location of the pole** and it is not a guess about latitude.

NASA states that ICESat-2 has a 92° orbital inclination and direct coverage to approximately 88° north and south. ESA states that CryoSat reaches approximately 88° north and south on every orbit.

Official references:

- NASA ICESat-2 technical specifications: https://icesat-2.gsfc.nasa.gov/science/specs
- ESA CryoSat satellite/orbit description: https://www.esa.int/Applications/Observing_the_Earth/FutureEO/CryoSat/Satellite

The scientifically important point is different:

> **88°N is the approximate northern limit of direct along-track observation for these missions; it is not a direct physical measurement of environmental conditions at 90°N.**

The angular gap from 88°N to the geographic pole is 2 degrees of latitude, or roughly **222 km along a meridian**. Therefore the region inside the ~88°N ring around the pole must be represented by other sensors, other missions, model fields, gridded products, interpolation/aggregation, drifting in-situ observations, aircraft/ship campaigns, or combinations of these.

## 2. Direct measurement versus derived/gridded product

ICESat-2 makes this distinction especially clear.

NASA/NSIDC list the along-track ATL10 sea-ice freeboard product with spatial coverage from 88°S to 88°N. ATL10 calculates freeboard in along-track segments of about 10 km.

- ATL10 Version 7: https://nsidc.org/data/atl10/versions/7

NASA also distributes gridded sea-ice products derived from the along-track observations. Some gridded products extend closer to the pole than the direct ATL10 coverage because they aggregate observations into grid cells.

That is scientifically useful, but a **gridded value is not the same thing as a laser footprint physically measured at 90°N**.

For TerraWater AI every polar value should therefore retain a provenance class such as:

- `DIRECT_TRACK_MEASUREMENT`
- `IN_SITU_MEASUREMENT`
- `GRIDDED_DERIVED_PRODUCT`
- `INTERPOLATED_OR_ASSIMILATED`
- `MODEL_ESTIMATE`
- `UNMEASURED_FIXED_REFERENCE`

This prevents a visually continuous map from being mistaken for continuous direct measurement.

## 3. Known measurement uncertainty is not zero even where the satellite directly observes

NASA's ICESat-2 technical requirement for monthly sea-ice freeboard is an uncertainty of **≤ 3 cm along 25 km segments**, and only under the specified conditions: clear sky and available sea-surface-height references such as leads.

Official NASA requirement:

- https://icesat-2.gsfc.nasa.gov/pages/icesat-2-technical-requirements

NASA's technical specifications also list pointing knowledge of about **6.5 m**, pointing control of about **45 m**, and expected 100-shot range standard deviations over sea ice of roughly **3–8 cm** depending on beam strength and conditions.

These numbers demonstrate two important facts:

1. satellite altimetry can be extremely precise;
2. the final geophysical product still has non-zero uncertainty and depends on atmosphere, surface state, leads, snow, footprint geometry, processing and spatial averaging.

A few centimetres of freeboard uncertainty can propagate into a much larger uncertainty in derived sea-ice thickness because thickness is not measured directly by the altimeter; it is inferred using hydrostatic and snow/ice assumptions.

## 4. CryoSat validation shows why direct reference measurements remain necessary

ESA's CryoSat validation programme explicitly uses simultaneous ground, airborne and satellite measurements because the uncertainty budget cannot be established from the satellite alone.

Official ESA field-validation description:

- https://blogs.esa.int/cryosat-ice-blog/arctic-campaign/

An ESA CryoSat sea-ice validation summary reported correlations of roughly **0.6–0.8** and RMS differences of approximately **0.3–0.6 m** between CryoSat sea-ice thickness retrievals and independent thickness observations at large spatial/temporal scales in the studies reviewed.

ESA workshop reference:

- https://lps16.esa.int/page_session56.php

These values must not be treated as a single universal error for the entire Arctic. They vary with product, season, ice type, snow conditions, averaging scale and validation method. They are included here to show that **retrieved thickness can differ from independent observations by decimetres even when the satellite system itself is functioning correctly**.

## 5. Drifting observatories are scientifically valid — but they solve a different problem

A drifting buoy, ice camp or ship can have excellent GNSS position knowledge and well-calibrated sensors. The fact that it moves does not automatically make its measurement wrong.

However, a drifting platform changes:

- geographic position;
- orientation;
- surrounding ice geometry;
- snow distribution;
- distance to leads/ridges;
- local ocean current regime;
- collocation with satellite ground tracks;
- local representativeness of the sampled surface.

These changes can be measured and modeled, but they mean that the experiment does **not** repeatedly sample the same fixed physical/geodetic reference location over many years.

This is why a drifting observatory and a permanent 90°N benchmark should be treated as complementary systems rather than competing ones.

## 6. The key gap we want to test

The project therefore makes the following falsifiable claim:

> **Humanity has high-quality satellite observations and high-quality drifting/expedition measurements in the central Arctic, but it does not currently have a permanent, fixed, multi-year in-situ observatory exactly at the geographic North Pole that continuously measures the atmosphere–snow–ice–ocean column from the same geodetic reference point.**

The scientific question is not "are current measurements wrong?"

The scientific question is:

> **How much additional uncertainty is introduced when long-term polar products are validated with moving, episodic or spatially separated reference measurements instead of a continuously maintained fixed 90°N reference?**

That number should be measured, not assumed.

## 7. Why the error between 88°N and 90°N cannot be represented by one honest percentage today

It would be scientifically incorrect to write that the entire polar region is "wrong by X percent".

There are multiple uncertainty components:

- instrument ranging/noise;
- orbit and pointing knowledge;
- atmospheric corrections;
- sea-surface reference detection;
- snow depth and density;
- ice density;
- melt ponds and wet snow;
- surface roughness and ridging;
- spatial averaging;
- temporal mismatch;
- interpolation/gridding/model assimilation;
- mismatch between a drifting point measurement and a satellite footprint or grid cell.

The total error depends on the variable being measured. Sea-ice concentration, freeboard, thickness, snow depth, ocean heat flux and atmospheric variables all have different error budgets.

Therefore TerraWater AI will not invent one percentage for the entire 88°N–90°N region. Instead, it will build an **uncertainty ledger per variable, sensor, product, time and location**.

## 8. What a fixed 90°N station could improve

A permanent reference station could reduce or directly characterize several uncertainty components:

- repeated measurements at exactly the same geodetic location;
- continuous calibration history;
- synchronized atmosphere/ice/ocean measurements;
- stable GNSS reference monument;
- repeatable radar/LiDAR reference geometry;
- direct snow depth/density and ice-thickness observations;
- continuous local sea-level and pressure reference;
- long-term ocean current/temperature/salinity profiles;
- direct comparison with satellite overpasses and derived grid products.

It would **not** eliminate satellite noise, cloud effects, snow physics, spatial-representativeness errors or model uncertainty. It would add an independent physical anchor against which these errors can be quantified.

## 9. Proposed experiment before any megastructure decision

Before arguing for a full artificial island, the project should run a smaller scientific proof:

1. establish a high-precision temporary reference close to 90°N;
2. deploy redundant GNSS, meteorology, snow, ice, ocean and radiation sensors;
3. maintain a strict calibration/provenance ledger;
4. compare direct observations with ICESat-2, CryoSat, Sentinel, SMOS and relevant gridded products;
5. compare the fixed/controlled reference with nearby drifting instruments;
6. quantify collocation, temporal, spatial and retrieval errors separately;
7. publish the result whether it supports or weakens the case for a permanent station.

Only if the fixed-reference experiment demonstrates substantial scientific value should the large seabed-supported station/island concept advance to deeper engineering analysis.

## Scientific conclusion

**The 88° orbital limit is known. The environmental state of the unmeasured fixed point at 90°N is not obtained by simply extending that orbital number by two degrees.**

Modern satellite and drifting-observatory science is valuable and often highly precise. But a continuous map or model near the pole can include direct measurements, spatial aggregation, interpolation and physical modeling. These categories must not be treated as identical.

A permanent 90°N observatory would be valuable if — and only if — it measurably reduces uncertainty that cannot be reduced more safely and efficiently by lower-impact observing systems.

## Official references

- NASA ICESat-2 technical specifications: https://icesat-2.gsfc.nasa.gov/science/specs
- NASA ICESat-2 technical requirements: https://icesat-2.gsfc.nasa.gov/pages/icesat-2-technical-requirements
- NASA/NSIDC ATL10 Sea Ice Freeboard V7: https://nsidc.org/data/atl10/versions/7
- NASA ICESat-2 sea-ice products: https://icesat-2.gsfc.nasa.gov/sea-ice-data
- ESA CryoSat orbit/coverage: https://www.esa.int/Applications/Observing_the_Earth/FutureEO/CryoSat/Satellite
- ESA CryoSat Arctic validation campaign: https://blogs.esa.int/cryosat-ice-blog/arctic-campaign/
- ESA CryoSat sea-ice validation summary: https://lps16.esa.int/page_session56.php
