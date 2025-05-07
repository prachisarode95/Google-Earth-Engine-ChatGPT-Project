# 📌 Prompt Log

This document contains the prompts used to generate Google Earth Engine scripts with the help of ChatGPT for the course **"Introduction to Geospatial Data Analysis with ChatGPT and Google Earth Engine"**.

---

## 🧪 Exercise 1: Integrating ChatGPT with Google Earth Engine

### 🔹 Prompt 1
Generate a code that displays a satellite image over Vietnam

### 🔹 Prompt 2
Write a JavaScript code using the Google Earth Engine API to display a satellite image over Vietnam

### 🔹 Prompt 3
Write JavaScript code using the Google Earth Engine API to display a median composite image from the USGS Landsat 8 Collection 2 Tier 1 TOA Reflectance dataset (ID: `ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")`) over Vietnam.

### 🔹 Prompt 4
Write a JavaScript code using the Google Earth Engine API to generate a median composite image from the USGS Landsat 8 Collection 2 Tier 1 TOA Reflectance dataset (ID: `ee.ImageCollection('LANDSAT/LC08/C02/T1_TOA')`) over Vietnam. Extract the shapefile of Vietnam from `'USDOS/LSIB_SIMPLE/2017'` and clip the resulting composite image over the shapefile. For visualisation, employ a False Color Composition of bands.

### 🔹 Prompt 5
Act as an urban planner tasked with assessing environmental conditions in Vietnam for 2021 using satellite imagery.

### 🔹 Prompt 6
Utilize the Google Earth Engine JavaScript API to calculate and visualize key indices such as NDVI (Normalized Difference Vegetation Index), NDBI (Normalized Difference Built-up Index), and MNDWI (Modified Normalized Difference Water Index).

### 🔹 Prompt 7
Access the USGS Landsat 8 Collection 2 Tier 1 TOA Reflectance dataset with its collection ID (`ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")`) and use a median composite image for your analysis. To focus the study, establish the geographic boundary by extracting the shapefile of Vietnam from large-scale International Boundary Polygons (Feature Collection ID: `'USDOS/LSIB_SIMPLE/2017'`) and clip the resulting indices over this shapefile. For visualization purposes, represent NDVI with "green shades," MNDWI with "blue shades," and NDBI with "red shades."

---
