# Earth Engine Data Processing for Lumbini Province

This repository provides a Python script to extract, process, visualize, and export various remote sensing datasets for the **Lumbini Province, Nepal**, using the **Google Earth Engine (GEE) Python API** and **Geemap**.

## Features
The script performs the following tasks:
- **Load Study Area**: Import shapefile of the study area (Lumbini Province).
- **SRTM Elevation**:
  - Load Shuttle Radar Topography Mission (SRTM) elevation data.
  - Visualize and export as GeoTIFF.
- **MODIS Land Surface Temperature (LST)**:
  - Extract MODIS daily LST data (2000–2025).
  - Convert to Celsius, compute mean, visualize, and export.
- **CHIRPS Precipitation**:
  - Calculate yearly total precipitation (2000–2025).
  - Compute average yearly precipitation, visualize, and export.
- **Landsat NDVI**:
  - Load Landsat 8 data (2024) with <20% cloud cover.
  - Calculate NDVI, compute median for 2024, visualize, and export.

## Run the Project
- Install: pip install -r requirements.txt
- Run: jupyter notebook FFRM_Factors.ipynb
- Follow the notebook steps

## Authentication
Before running the script, authenticate with Google Earth Engine:
- import ee
- ee.Authenticate()
- ee.Initialize(project="your-project-id")

## Output
All exported files are saved in the google drive:
- lumbini_elevation.tif - Elevation data (30m)
- lumbini_lst_mean.tif - Mean Land Surface Temperature (1000m)
- lumbini_precipitation.tif - Average yearly precipitation (5500m)
- lumbini_ndvi_2024.tif - Median NDVI for 2024 (30m)