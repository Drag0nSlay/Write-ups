# OSINT Investigation: Locating the "Skyline of North Bhubaneswar"
![Poster]()

**Investigator:** Aman Kothari

**Target:** Geographic location of a nighttime city skyline photo.

**Tools Used:** Reverse Image Search (RIS), X (Twitter) Advanced Search, Google Earth, Sentinel Hub (EO Browser), Copernicus.

## 1. Executive Summary

The objective was to identify the exact coordinates of a photograph provided as an OSINT challenge. Through a combination of **social media intelligence (SOCMINT)** and **satellite imagery analysis (IMINT)**, the location was identified as the **Lalchnd Jewellers** building in **Raghunathpur, North Bhubaneswar**, within approximately 5 minutes.

## 2. Phase I: Source Identification & Metadata

The investigation began by performing a Reverse Image Search to find the original source of the image.

- **Discovery:** The image was traced to a post on X (formerly Twitter).

- **Source Handle:** @manas_muduli

- **Timestamp:** 22nd September 2024 | 18:49 IST

- **Key Contextual Clues:** * "The Skyline of North Bhubaneswar :)"
  - "Constructions happening all around."
 
## 3. Phase II: Filtering & Branch Identification

A search for "Lalchnd Jewellers" in Bhubaneswar returned multiple results. To narrow the search, the clues from the post were applied:

1. **Branch Selection:** The prominent neon sign was the primary anchor. While the Master Canteen branch is more famous, the "North Bhubaneswar" caption pointed toward the **Raghunathpur/Nandankanan Road** area.
2. **Visual Matching:** The skyline in the photo featured several high-rise skeletons under construction, which is characteristic of the rapidly developing North Bhubaneswar corridor.

## 4. Phase III: Geospatial Verification (IMINT)

Initial verification via Google Earth and Google Maps showed a discrepancy; the base maps were outdated and did not show the level of construction progress seen in the photo.

- **Pivot to Satellite Data:** To verify the "constructions happening all around," **Sentinel Hub (EO Browser)** and **Copernicus** data were used.

- **Analysis:** By generating a timelapse and viewing recent Sentinel-2 imagery, I confirmed the footprint of the new high-rise structures (such as the developments near Falcon Residencia/Nawah Emporio) that matched the photo's perspective.

- **Point of Origin:** The photo was likely taken from an elevated position (likely a nearby high-rise or apartment complex) facing North toward the Lalchnd building in Raghunathpur.

## 5. Conclusion

The target location is confirmed as **Lalchnd Jewellers, Raghunathpur, Bhubaneswar**.

**Coordinates (Accurate):** Lalchnd Jewellers – Jewellery Shop in Bhubaneswar, 2149.2149/2880, Raghunathpur, Bhubaneswar, Odisha 751024

## Technical Note

*While **SunCalc** was considered for chronolocation (verifying the time via shadows), it was deemed redundant for this specific case as the source timestamp and geographical landmarks provided a definitive match within a high-confidence interval.*
