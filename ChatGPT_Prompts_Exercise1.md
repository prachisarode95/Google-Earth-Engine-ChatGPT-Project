# 📌 Prompt Log

This document contains the prompts used to generate Google Earth Engine scripts with the help of ChatGPT for the course **"Introduction to Geospatial Data Analysis with ChatGPT and Google Earth Engine"**.

---

## 🧪 Exercise 1: Integrating ChatGPT with Google Earth Engine

### 🔹 Prompt 1
Generate a code that displays a satellite image over Vietnam

### 🔹 Prompt 2
Write a JavaScript code using the Google Earth Engine API to display a satellite image over Vietnam

### 🔹 Prompt 3
Write JavaScript code using the Google Earth Engine API to display a median composite image from the USGS Landsat 8 Collection 2 Tier 1 Reflectance dataset (ID: ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")) over Vietnam, with date ranges between 2024 and 2025.

### 🔹 Prompt 4
Write JavaScript code using the Google Earth Engine API to generate a median composite image from the USGS Landsat 8 Collection 2 Tier 1 Reflectance dataset (ID: ee.ImageCollection('LANDSAT/LC08/C02/T1_TOA')) for Vietnam, covering the date range from 2024 to 2025. Extract the shapefile of Vietnam from 'USDOS/LSIB_SIMPLE/2017' and clip the resulting composite image to this shapefile. For visualization, use a False Color Composition of the specified bands.

### 🔹 Prompt 5
As an urban planner, your task is to assess the environmental conditions in Vietnam during the years 2024-2025. You will use satellite imagery and the Google Earth Engine JavaScript API to calculate and visualize key indices, such as the Normalized Difference Vegetation Index (NDVI), the Normalized Difference Built-up Index (NDBI), and the Modified Normalized Difference Water Index (MNDWI).

### 🔹 Prompt 6
Access the USGS Landsat 8 Collection 2 Tier dataset using the collection ID from the Google Earth Engine Data Catalog. For example, you can use the ID: `ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")`. Perform your analysis using a median composite image with a date range of 2024-2025.

To narrow your focus, obtain the shapefile of Vietnam from the large-scale International Boundary Polygons by using the feature collection ID: `USDOS/LSIB_SIMPLE/2017`. Clip the resulting indices to this shapefile.

For visualization purposes, use "green shades" to represent NDVI, "blue shades" for MNDWI, and "red shades" for NDBI.

---
