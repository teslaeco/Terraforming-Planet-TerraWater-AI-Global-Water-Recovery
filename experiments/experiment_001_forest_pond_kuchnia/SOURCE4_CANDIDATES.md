# Experiment 001 — Fourth-source candidates

The fourth-source requirement is evidence-driven, not quota-driven. A mission is included only when its data for the AOI can be traced to an official/public provider and the spatial resolution is useful for the forest pond or Lake Kuchnia.

## 1. JAXA ALOS — preferred fourth-source candidate for 2006–2011

Official JAXA G-Portal states that ALOS data are available for **2006-05-15 through 2011-04-13** and that **AVNIR-2 and PALSAR** are part of the ALOS-series Open and Free Data offering.

- AVNIR-2 is attractive as an independent optical sensor for the middle of the Landsat record.
- PALSAR provides independent L-band radar physics, complementary to Sentinel-1 C-band radar.
- G-Portal search is public, but product download requires a G-Portal user login. Therefore the pipeline must not pretend anonymous download is available.

Official references:
- https://gportal.jaxa.jp/gpr/information/product?lang=en
- https://gportal.jaxa.jp/gpr/search?lang=en
- https://www.eorc.jaxa.jp/ALOS/en/dataset/alos_open_and_free_e.htm

Status: **selected candidate; catalog/provenance can be audited now, imagery download requires JAXA account credentials.**

## 2. NASA ASTER — strong independent optical candidate from 2000 onward

NASA Earthdata/LP DAAC archives and distributes ASTER products. ASTER is carried on NASA's Terra spacecraft and is a separate instrument from Landsat and Sentinel. ASTER VNIR is useful for higher-detail historical control, but it does not provide a normal blue band, so imagery must be labelled as false-color where appropriate rather than presented as true RGB.

NASA CMR lists products including ASTER Level 1T and Level-2 VNIR/SWIR products.

Official references:
- https://www.earthdata.nasa.gov/centers/lp-daac
- https://cmr.earthdata.nasa.gov/search/site/collections/directory/LPCLOUD/gov.nasa.eosdis

Status: **selected candidate; Earthdata/LP DAAC access is official and free, but automated granule download may require Earthdata Login authentication.**

## 3. CNSA Gaofen — potentially excellent modern independent source

CNSA documents an international data-sharing platform for Gaofen data. The official CNSA announcement states that Gaofen-1/Gaofen-6 16 m multispectral data can be searched/downloaded through its global sharing platform, and registered international users can access Gaofen imagery. CNSA also documents higher-resolution Gaofen missions, including Gaofen-1 2 m panchromatic/8 m multispectral and Gaofen-3 SAR.

Official references:
- https://www.cnsa.gov.cn/english/n6465652/n6465653/c6808065/content.html
- https://www.cnsa.gov.cn/n6758824/n6759008/n6759012/c6794271/content.html

Status: **promising candidate for modern cross-checks; exact Poland AOI availability and current download/API requirements must be verified before imagery is admitted as evidence.**

## 4. Roscosmos / Russian federal remote-sensing holdings

Roscosmos documents a federal Earth remote-sensing data fund and use of Russian governmental Earth-observation spacecraft. Candidate missions include Kanopus-V / Resurs-P where appropriate.

Official reference:
- https://www.roscosmos.ru/39803/

Status: **candidate only. No Experiment 001 image is accepted from this family until an official public product for the exact Poland AOI can be independently retrieved with date, product identifier and legal-use provenance.**

## Admission rule

A fourth-source image is admitted only when all of these fields are available:

1. mission/sensor;
2. exact acquisition date/time;
3. official product or granule identifier;
4. official provider URL/catalog;
5. AOI intersection proof;
6. native spatial resolution;
7. processing level;
8. download/provenance record;
9. image-integrity SHA-256;
10. no cross-year duplicate conflict.

Until then, it stays in the candidate registry and cannot strengthen the numerical water-loss claim.
