# ☀️🏜️ Spatiotemporal Drought Monitoring in Indonesia

This project demonstrates the use of **Google Earth Engine JavaScript API** to compute and visualize drought-related indices over **Indonesia** for the year **2024**. The analysis includes VCI, TCI, and DSI indices, alongside a time-series visualization of VCI.

---

## 📅 Analysis Period

- **Start Date:** January 1, 2024  
- **End Date:** December 31, 2024

---

## 🌍 Study Area

- **Region of Interest:** Indonesia  
- **Boundary Source:** `'USDOS/LSIB_SIMPLE/2017'` (Simplified international boundaries)

---

## 🛰️ Datasets Used

| Dataset ID | Description |
|------------|-------------|
| `MODIS/061/MOD13A2` | MODIS Terra Vegetation Indices (NDVI) – 16-Day Global 1km |
| `MODIS/061/MOD11A1` | MODIS Terra Land Surface Temperature & Emissivity – Daily Global 1km |
| `MODIS/061/MOD16A2` | MODIS Terra Net Evapotranspiration – 8-Day Global 500m |
| `USDOS/LSIB_SIMPLE/2017` | Simplified country boundaries dataset |

---

## 💬 Prompt Log

These prompts were used to guide the project development using ChatGPT. Each prompt was carefully crafted to perform specific geospatial analysis tasks in GEE.

---

### 💡 **Prompt 1: Calculate Vegetation Condition Index (VCI)**

```

As a climatologist working on the Google Earth Engine JavaScript API, your assignment is to compute an essential drought index for monitoring drought conditions in Indonesia. The specific tasks are outlined below:

✅ Calculate the Vegetation Condition Index (VCI) for Indonesia.

✅ Utilize the 'MODIS/061/MOD13A2' (Terra Vegetation Indices 16-Day Global 1km) dataset for VCI and calculate the formula's NDVI min and NDVI max separately.

✅ Set the time intervals: January 1, 2022, to December 31, 2022.

✅ After computing the index, visualize it on the map with ten distinct color representations.

✅ Clip the visualizations using the boundary of Indonesia. Extract the Indonesia shapefile from the dataset 'USDOS/LSIB\_SIMPLE/2017.' Perform any additional analysis or calculation required to derive VCI accurately.

```

---

### 💡 **Prompt 2: Calculate Temperature Condition Index (TCI)**

```

As a climatologist working on the Google Earth Engine JavaScript API, your assignment is to compute an essential drought index for monitoring drought conditions in Indonesia. The specific tasks are outlined below:

✅ Calculate the Temperature Condition Index (TCI) for Indonesia.

✅ Utilize the 'MODIS/061/MOD11A1' Terra Land Surface Temperature and Emissivity Daily Global 1km dataset for TCI and calculate the LST minimum and LST maximum separately for the formula.

✅ Set the time intervals: January 1, 2022, to December 31, 2022.

✅ After computing the index, visualize it on the map with ten distinct color representations.

✅ Clip the visualizations using the boundary of Indonesia. Extract the Indonesia shapefile from the dataset 'USDOS/LSIB\_SIMPLE/2017.' Perform any additional analysis or calculation required to derive TCI accurately.

```

---

### 💡 **Prompt 3: Calculate Drought Severity Index (DSI)**

```

Your next task is to calculate Drought Severity Index (DSI) for Indonesia:

✅ Utilize the following dataset to calculate DSI:

* For NDVI: 'MODIS/061/MOD13A2'
* For ET and PET: 'MODIS/061/MOD16A2'

✅ Set the time intervals: January 1, 2022, to December 31, 2022.

✅ After computing the index, visualize it on the map with 10 color representations.

✅ Clip the visualizations using the boundary of Indonesia. Extract the Indonesia shapefile from the dataset 'USDOS/LSIB\_SIMPLE/2017.' Perform any additional analysis or calculation required to derive DSI accurately.

```

---

### 💡 **Prompt 4: Create Time Series Chart for VCI**

```

From the following code, create a time series chart using "ui.Chart.image.doySeriesByRegion" (we will define the algorithm to use) of VCI against the variable geometry and display it in the console. Apply the required reducer and use the most suitable band. Also, the time duration should be exact, as used in the code.

```

---

## 🗂️ Output Summary

- ✅ Vegetation Condition Index (VCI) Map
- ✅ Temperature Condition Index (TCI) Map
- ✅ Drought Severity Index (DSI) Map
- ✅ All maps clipped to Indonesia's boundaries
- ✅ VCI Time-Series Chart displayed in GEE Console

---

# View code in engine
[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)](https://code.earthengine.google.com/161144086fe6d17d9e20bd129e03e383?noload=true)
