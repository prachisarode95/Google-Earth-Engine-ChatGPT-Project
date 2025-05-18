# 🌇🌱 Urban and Vegetation Dynamics in Vietnam (2024)

This project explores satellite-based analysis of urban and vegetation changes over Vietnam using the Google Earth Engine JavaScript API. The exercise was developed as part of the course:

📘 "Introduction to Geospatial Data Analysis with ChatGPT and Google Earth Engine"

---

## 📅 Analysis Period

- Start Date: January 1, 2024

- End Date: December 31, 2024

---

## 🌍 Study Area

- Region: Vietnam
- Boundary Source: `USDOS/LSIB_SIMPLE/2017`

---

## 🛰️ Datasets Used

| Dataset ID | Description |
|------------|-------------|
| `LANDSAT/LC08/C02/T1_TOA` | USGS Landsat 8 Collection 2 Tier 1 TOA Reflectance |
| `USDOS/LSIB_SIMPLE/2017` | Simplified international boundaries (used to clip Vietnam) |

---

## 💬 Prompt Log

These prompts were used to generate Google Earth Engine scripts for exploring land cover, urbanization, and vegetation indices.

### 💡 Prompt 1

```
✅ Generate a code that displays a satellite image over Vietnam
```

### 💡 Prompt 2

```
✅ Write a JavaScript code using the Google Earth Engine API to display a satellite image over Vietnam
```

### 💡 Prompt 3

```
✅ Write JavaScript code using the Google Earth Engine API to display a median composite image from the USGS Landsat 8 Collection 2 Tier 1 Reflectance dataset (ID: ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")) over Vietnam, with date ranges between 2024 and 2025.
```

### 💡 Prompt 4

```
✅ Write JavaScript code using the Google Earth Engine API to generate a median composite image from the USGS Landsat 8 Collection 2 Tier 1 Reflectance dataset (ID: ee.ImageCollection('LANDSAT/LC08/C02/T1_TOA')) for Vietnam, covering the date range from 2024 to 2025. Extract the shapefile of Vietnam from 'USDOS/LSIB_SIMPLE/2017' and clip the resulting composite image to this shapefile. For visualization, use a False Color Composition of the specified bands.
```

### 💡 Prompt 5

```
✅ As an urban planner, your task is to assess the environmental conditions in Vietnam during the years 2024-2025. You will use satellite imagery and the Google Earth Engine JavaScript API to calculate and visualize key indices, such as the Normalized Difference Vegetation Index (NDVI), the Normalized Difference Built-up Index (NDBI), and the Modified Normalized Difference Water Index (MNDWI).
```

### 💡 Prompt 6

```
✅ Access the USGS Landsat 8 Collection 2 Tier dataset using the collection ID from the Google Earth Engine Data Catalog. For example, you can use the ID: `ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")`. Perform your analysis using a median composite image with a date range of 2024-2025.

✅ To narrow your focus, obtain the shapefile of Vietnam from the large-scale International Boundary Polygons by using the feature collection ID: `USDOS/LSIB_SIMPLE/2017`. Clip the resulting indices to this shapefile.

✅ For visualization purposes, use "green shades" to represent NDVI, "blue shades" for MNDWI, and "red shades" for NDBI.
```

## ⚙️ View Live Code in Earth Engine

[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)](https://code.earthengine.google.com/2bd11572ec2350a2adaca9646ad0e97d?noload=true)

---

## 🗂️ Output Summary

- ✅ Satellite imagery displayed over Vietnam
- ✅ Median composite created for Landsat 8 imagery (2024–2025)
- ✅ NDVI, NDBI, and MNDWI calculated and visualized
- ✅ All outputs clipped to Vietnam boundaries
