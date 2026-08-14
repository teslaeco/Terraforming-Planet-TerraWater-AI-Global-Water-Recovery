# Experiment 001 — suitability of satellites already planned on the Polar site

The Polar near-real-time control-center design includes EUMETSAT Meteosat-12/FCI, NOAA GOES ABI, JMA Himawari AHI, NASA GIBS/Worldview and optional NASA DSCOVR EPIC.

For the hectare-scale forest pond, these are mainly **meteorological/context sources**, not final shoreline-measurement sources:

- Meteosat/GOES/Himawari: useful for cloud/weather context, far too coarse for ~2.5 ha water-area measurement.
- DSCOVR EPIC: whole-Earth context, not local shoreline measurement.
- NASA GIBS: useful only when a specific layer has sufficient native spatial resolution and independent sensor provenance; otherwise contextual.

Preferred fourth-source quantitative candidates remain:

1. NASA ASTER / Terra — separate optical instrument, 15 m-class VNIR; official CMR catalog contains many AOI hits.
2. JAXA ALOS AVNIR-2 / PALSAR — separate optical + L-band radar source for 2006–2011, official open/free products with G-Portal access.
3. CNSA Gaofen — candidate after exact official Poland AOI products are verified.
4. Roscosmos governmental EO products — candidate after exact official public/legal Poland AOI products are verified.

The experiment will never count a coarse/context image as hectare-scale quantitative confirmation merely to increase the source count.
