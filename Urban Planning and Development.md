# 🌆🌳 Urban Green Space Analysis in Indonesian Cities

This project leverages the power of the **Google Earth Engine JavaScript API** to map and quantify green spaces across selected Indonesian cities. The analysis focuses on Sentinel-2-based EVI estimation and proximity analysis of green areas from buildings.

---

## 🏙️ Selected Cities for Analysis

- Kota Cirebon  
- Kota Tangerang  
- Kota Bekasi  
- Kota Depok  
- Kota Bogor  

These administrative boundaries are sourced from:

- Dataset ID: `FAO/GAUL/2015/level2`

---

## 📅 Analysis Period

- **Start Date:** January 1, 2022  
- **End Date:** December 31, 2022

---

## 🛰️ Datasets Used

| Dataset ID | Description |
|------------|-------------|
| `COPERNICUS/S2_SR_HARMONIZED` | Sentinel-2 Surface Reflectance data for green space analysis |
| `FAO/GAUL/2015/level2` | Global Administrative Unit Layers for city boundaries |
| `GOOGLE/Research/open-buildings/v3/polygons` | Open Buildings V3 – global building footprint dataset |

---

## 💬 Prompt Log

These prompts were used during the development of this exercise to guide the implementation of each step using the Google Earth Engine JavaScript API.

---

### 💡 Prompt 1: Green Space Mapping & Statistics

```

Generate a Google Earth Engine JavaScript API code to map green spaces over selected cities. Utilize the following steps:

✅ City Selection:

Use the predefined list of cities, including 'Kota Cirebon,' 'Kota Tangerang,' 'Kota Bekasi,' 'Kota Depok,' and 'Kota Bogor.'

Extract the administrative boundary of these cities from the following dataset: ee.FeatureCollection("FAO/GAUL/2015/level2")

✅ Loop Over Cities:

For each city, process Sentinel-2 imagery with ID: ee.ImageCollection("COPERNICUS/S2_SR_HARMONIZED") to map green spaces.

✅ Image Processing:

Define each city's Region of Interest (ROI) based on administrative boundaries.

Generate a Sentinel-2 composite free imagery for the specified date range (2022-01-01 to 2022-12-31).

Create a composite image and scale values to 0 - 1.

✅ Visualization:

Add the composite image to the map for visual inspection.

Calculate and visualize the Enhanced Vegetation Index (EVI).

Visualize urban green space using a threshold for EVI (>=0.35) with .selfMask() and display the green spaces on the map with green color.

✅ Area Calculation:

Calculate the area of the city and urban green space.

✅ Percentage Calculation:

Calculate the percentage of green area compared to the total city area.

✅ Printing Results:

Print the city name, total area, green area, and percentage of green area.

```

---

### 💡 Prompt 2: Green Space Proximity to Buildings

```

✅ In the Code given below and check the distance of green spaces from buildings in the selected cities.

To extract building use the Open Buildings V3 Polygons with ID: ee.FeatureCollection("GOOGLE/Research/open-buildings/v3/polygons")

Clip out the buildings in the selected cities and then display them on the map, and calculate the distance of the Green Space Area from the buildings in each city.

```

# View code in engine
[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)]()

---

## 📈 Output Summary

- ✅ EVI Composite Map for each city
- ✅ Green space visualization using EVI ≥ 0.35
- ✅ Green space vs total city area statistics printed
- ✅ Buildings clipped per city and visualized
- ✅ Distance-to-building analysis performed for green areas
