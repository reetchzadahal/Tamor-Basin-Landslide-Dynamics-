# Spatiotemporal Assessment of Landslide Dynamics in the Tamor River Basin (2000–2024)

An investigation into the relationship between climatic variability and landslide events in a critical Himalayan watershed using Google Earth Engine (GEE), Python, and QGIS.

## Project Overview
This repository contains the data and spatial outputs generated during a 3-month research mentorship cohort. The project evaluates 25 years of land use/land cover (LULC) changes within the Tamor River Basin, Nepal—specifically tracking the transitions of barren land and landslide scarring.

### Key Finding: The Statistical Paradox
While seasonal monsoon precipitation is traditionally modeled as the primary driver of Himalayan landslides, statistical analysis of this 25-year dataset yielded a near-zero correlation (**$r = 0.06$**) between annual rainfall totals and basin-wide landslide surface area. 

* **2006 Anomaly:** A massive spike of **12,678.30 Hectares** occurred during a climatologically average rainfall year, indicating heavy *anthropogenic priming* (such as regional infrastructure and road construction projects).

---

## Data & Methodology
* **Data Core:** Google Earth Engine (GEE) API & Python (Pandas, NumPy) used for time-series extraction.
* **Classification Technique:** Pixel-based spectral thresholding to isolate barren surfaces and landslide scars.
* **Spatial Processing:** QGIS used for watershed boundary delineation, vector masking, and final cartographic mapping.
* **Data Inputs:** CHIRPS & GPM (Satellite Precipitation), Landsat/Sentinel Time-Series (LULC).

---

## Spatial Outputs

### Final Clipped Basin Analysis
The map below demonstrates the watershed-clipped LULC output for the Tamor Basin. High-altitude barren areas are clearly isolated along the northern elevation gradient.

![Tamor Basin LULC](maps/tamor_basin_lulc_clipped.png)

---

## Data Summary (2000–2024)
The complete time-series historical data sheet is available in `data/TamorBasin_25Year_Trend(in).csv`. 

---

## Proposed Future Roadmap & Validation Framework
To build upon this baseline dataset, the established next steps for the research include:

1. **Ground Meteorological Validation:** Incorporating daily-log data from the **5 Department of Hydrology and Meteorology (DHM) Nepal Stations** (Dhankuta, Lungthung, Taplejung, Phidim, and Dovan) to check for localized cloudbursts that satellite sensors may smooth out.
2. **Hydrological Class Separation:** Utilizing target indices such as **NDWI** (Water) and **NDSI** (Snow) to explicitly separate the active river channel and glacial caps from the broader barren landscape class.
3. **Proximity Buffer Modeling:** Constructing a Euclidean Distance buffer around regional road vectors in QGIS to mathematically quantify human impact on slope failures.

## Acknowledgments
Developed as the final project for the 3-Month Research Mentorship Cohort closing. Deep gratitude to my mentor for providing invaluable guidance on geospatial data logic, CV refinement, and professional academic development.

## Author
Richa Dahal
