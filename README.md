# DC Urban Heat & Climate OSINT Analysis (2015–2025)

This project combines geospatial analysis, open-source intelligence (OSINT), and AI-assisted interpretation to assess heat wave patterns and urban heat island (UHI) effects in Washington, D.C. between 2015 and 2025.

It integrates:

- **Satellite-derived urban heat island changes**
- **Scraped news headlines about extreme heat events** (via GNews API)
- **U.S. Census tract-level household income data**
- **Statistical regression and GPT-4 interpretation**

---

![Urban Heat Map – Washington DC](temporal-heat-map-dc.png)

---

## Objectives

- Detect spatial and temporal heat changes from 2015 to 2025
- Link those changes to real-world reported events
- Analyze correlation between median income and temperature change
- Use AI to interpret complex patterns for urban resilience planning

---

## Technologies Used

- Python (Google Colab, Jupyter)
- Libraries: `geopandas`, `requests`, `statsmodels`, `seaborn`, `matplotlib`
- APIs: GNews, OpenAI GPT-4, U.S. Census API
- Data: TIGER/Line shapefiles, NLCD & Landsat-derived heat rasters

---

## Repository Contents

| File | Description |
|------|-------------|
| [`dc-heat-osint.ipynb`](./dc-heat-osint.ipynb) | Merges OSINT headlines, satellite data, and regression |
| [`dc_heat_analysis.ipynb`](./dc_heat_analysis.ipynb) | Exploratory analysis of temperature change across neighborhoods |
| `temporal-heat-map-dc.png` | Visualization of heat hotspots over time |

---

## Data Access

Due to GitHub file size limitations, shapefiles and satellite rasters are hosted on Google Drive:

📁 **[Download Full Dataset (Shapefiles + TIGER/Line + Merged CSVs)](https://drive.google.com/drive/folders/1YKCJtaHW_XrL2SuLIOhImUCbyeQlTM-B?usp=drive_link)**

Includes:
- `uhi_temp_change_2015_2025_fahrenheit.shp`
- TIGER/Line shapefiles for DC census tracts
- Merged GeoDataFrame with heat and income
- Intermediate raster and land cover data used for UHI analysis

---

## Data Sources

- **Landsat 8 Surface Temperature**  
  Source: `LC08_L2SP_015033_20150614_20201015_02_T1_ST_B10`
  
- **National Land Cover Dataset (NLCD)**  
  Source: `Annual_NLCD_LndCov_2024_CU_C1V1.tif.aux`  
  Used for masking urban features and refining UHI estimates

- **TIGER/Line Census Tracts (2021)**  
  https://www2.census.gov/geo/tiger/TIGER2021/TRACT/

- **Median Household Income**  
  Pulled using U.S. Census API for tract-level variable `B19013_001E`

- **News Headlines**  
  Scraped via GNews API for heat-related reports 2015–2025

---

## Summary of Findings

- **Frequent heatwaves** occurred in DC, especially during July/August.
- **Top 10 zones** experienced temperature increases of up to 63.52°F.
- **Regression analysis** found **no statistically significant relationship** between median household income and temperature change.
- **GPT-4 analysis** recommends further exploration using land cover, vegetation, and zoning data for more robust insights.

---

## 🏙️ Future Work

- Integrate tree cover, impervious surface, and zoning layers
- Apply spatial lag or geographically weighted regression (GWR)
- Expand to a multi-city comparative analysis
- Time-series forecasting of heat events and social vulnerability

---

## ✍️ Author

**Your Name**  
Climate OSINT & Urban Analytics  
📧 [your.email@example.com]

---

> *"This repository was developed to demonstrate how open data and AI can be combined for climate resilience and equity-focused urban planning."*
