# Experiment 001 — provenance and independence matrix

| Evidence family | Agency / mission | Period | Physics | Status | Independent? |
|---|---|---|---|---|---|
| historical optical | NASA/USGS Landsat 5/7/8 | 1990 onward | optical multispectral | admitted real imagery | yes vs Sentinel |
| modern optical | ESA/Copernicus Sentinel-2 MSI | modern period through 2026 | optical multispectral | admitted real imagery | yes vs Landsat |
| alternate delivery | Google Cloud / Element 84 delivery of Landsat/Sentinel products | 1990–2025 | optical | processing/delivery cross-check; known package errors preserved | **not independent if same acquisition** |
| radar | ESA/Copernicus Sentinel-1 RTC | 2015–2025 May | C-band SAR | admitted independent radar evidence | yes |
| fourth-source preferred | NASA ASTER / Terra | catalog searched 2000–2026 | independent optical/IR | 77 AOI spring/autumn catalog hits; pixels pending admission | yes once official granule is downloaded/validated |
| additional source4 | JAXA ALOS AVNIR-2 / PALSAR | 2006–2011 | optical + L-band SAR | candidate; official G-Portal download workflow requires account | yes once exact AOI product is admitted |
| additional source4 | CNSA Gaofen | modern | optical / mission-dependent | candidate; exact official Poland AOI access not yet verified | not counted yet |
| additional source4 | Roscosmos civil EO holdings | modern | product-dependent | candidate; exact public/legal Poland AOI product not yet verified | not counted yet |

Different website ≠ different observation. Each admitted scene requires exact date/time, mission/sensor, official product ID, official provider, native resolution, processing level, AOI proof, quality metrics, SHA-256, cross-year duplicate test and an independence flag.

Current strongest independent measurement families: **Landsat optical, Sentinel-2 optical, Sentinel-1 radar**. ASTER is the preferred next independent optical family after official granule pixels are retrieved and validated.
