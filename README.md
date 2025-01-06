# Earthquake Choropleth Map of New Zealand

## Table of Contents
- [Introduction](#introduction)
- [Objective](#objective)
- [Why Folium?](#why-folium)
- [Dataset Information](#dataset-information)
- [Project Workflow](#project-workflow)
- [Installation](#installation)
- [Directory Structure](#directory-structure)
- [Code Explanation](#code-explanation)
- [Output](#output)
- [License](#license)

---

## Introduction
This project creates a **Choropleth Map** to visualise the frequency of earthquakes in various regions of New Zealand over the past year. Using geospatial data and Python libraries such as **GeoPandas** and **Folium**, we plot earthquake density as a color-coded map, highlighting regional variations in seismic activity.

---

## Objective
To provide a clear and interactive visual representation of earthquake occurrences in New Zealand, enabling researchers and stakeholders to identify patterns and trends in seismic activity.

---

## Why Folium?
**Folium** is a Python library that simplifies the creation of interactive maps. It supports multiple map types and integrates seamlessly with geospatial data formats like GeoJSON and Shapefiles. Folium allows:
- Creating interactive maps with zoom and pan functionality.
- Adding layers, legends, and tooltips for better interpretation.
- Generating HTML-based visualisations, making it easy to share insights.

This project showcases the power of Folium to visualsze earthquake frequency across New Zealand regions interactively.

---

## Dataset Information
1. **Earthquake Data:**
   - **Source:** GeoNet earthquake dataset.
   - **Format:** GeoJSON.
   - **Key Columns:** 
     - `latitude`: Latitude of the earthquake.
     - `longitude`: Longitude of the earthquake.
     - `depth`: Depth of the earthquake.
     - `magnitude`: Magnitude of the earthquake.

2. **Region Shapefile:**
   - **Source:** New Zealand territorial authority regions from Stats NZ.
   - **Format:** Shapefile (`.shp`).
   - **Projection:** NZGD2000 / New Zealand Transverse Mercator 2000 (EPSG:2193).

---

## Project Workflow

### Steps:
1. **Load and Prepare Data:**
   - Import earthquake GeoJSON data and region shapefiles.
   - Reproject shapefiles to EPSG:4326 (WGS 84) for consistency.

2. **Spatial Join:**
   - Assign earthquakes to regions using a spatial join.
   - Aggregate earthquake counts by region.

3. **Prepare GeoJSON for Visualization:**
   - Merge earthquake counts with shapefiles.
   - Fill missing data for regions with no earthquakes.
   - Save the cleaned GeoJSON file.

4. **Visualise Data:**
   - Create an interactive map centered on New Zealand.
   - Add a Choropleth layer to represent earthquake frequency.

5. **Export and Share:**
   - Save the Choropleth map as an HTML file for easy sharing.

---

## Directory Structure


NZ-Earthquake-Choropleth/  
├── data/  
│   ├── earthquake_data.geojson  # Earthquake GeoJSON file  
│   ├── nz_regions.shp           # Shapefile for New Zealand regions  
├── output/  
│   ├── joined_data_cleaned.geojson  # Processed GeoJSON file  
│   ├── earthquake_choropleth_map.html  # Final HTML map  
├── src/  
│   ├── create_choropleth_map.py  # Main script to generate the map  
├── requirements.txt              # Dependencies for the project  
├── README.md                     # Project documentation  
├── LICENSE                       # License information  


---


## Installation

### Prerequisites:
- Python 3.8 or higher
- Required libraries:
  ```bash
  pip install geopandas folium pandas

### Instructions to Set Up a Complete GitHub Project:

1. **Create a New GitHub Repository:**
   - Go to [GitHub](https://github.com/) and create a new repository named `NZ-Earthquake-Choropleth`.

2. **Clone the Repository Locally:**
   ```bash
   git clone https://github.com/username/NZ-Earthquake-Choropleth.git
   cd NZ-Earthquake-Choropleth


---


### Instructions to Use the File:  
1. Save this content in a file named `README.md`.  
2. Ensure the directory structure matches the one mentioned above.  
3. Push the repository to GitHub for public or private access.  

Let me know if you need further help! 😊

For questions or suggestions, feel free to open an issue or contact me at bushra@outlook.co.nz.
