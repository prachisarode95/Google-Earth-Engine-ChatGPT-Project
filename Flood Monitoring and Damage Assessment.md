# 🌊 Flood Monitoring and Damage Assessment

This project demonstrates the use of **Google Earth Engine JavaScript API** to map floods and assess the damage using **Sentinel-1 SAR** data over an area of interest (AOI). The analysis includes the extraction of flood masks, water bodies, and the assessment of affected populations using **GHS population data**.

---

## 📅 Analysis Period

- **Before Flood Period:** March 1, 2024 to March 30, 2024  
- **After Flood Period:** July 1, 2024 to July 30, 2024

---

## 🌍 Study Area

- **Region of Interest:** Area of Interest (AOI) (user-defined polygon)
- **Boundary Source:** `'COPERNICUS/S1_GRD'` (Sentinel-1 SAR GRD dataset)

---

## 🛰️ Datasets Used

| Dataset ID                  | Description |
|-----------------------------|-------------|
| `COPERNICUS/S1_GRD`          | Sentinel-1 SAR GRD dataset (for flood mapping) |
| `JRC/GHSL/P2023A/GHS_POP`    | GHS Population Grid (for damage assessment) |
| `USDOS/LSIB_SIMPLE/2017`     | Simplified country boundaries dataset |

---

## 💬 Prompt Log

These prompts were used to guide the project development using ChatGPT. Each prompt was carefully crafted to perform specific geospatial analysis tasks in GEE.

---

### 💡 **Prompt 1: Flood Mapping using Sentinel-1 SAR**

```

As a climatologist working on the Google Earth Engine JavaScript API, your assignment is to monitor flood conditions using Sentinel-1 SAR data. The specific tasks are outlined below:

✅ Utilize the Sentinel-1 SAR GRD dataset: 'COPERNICUS/S1\_GRD'.

✅ Apply filters for the following:

* Band: 'VH'.
* Instrument Mode: 'IW'.
* Orbit Properties: 'ASCENDING' and 'DESCENDING'.

✅ Set the time intervals:

* "Before Flood": March 1, 2024 to March 30, 2024.
* "After Flood": July 1, 2024 to July 30, 2024.

✅ Create "before" and "after" images by selecting the 'VH' band, creating mosaics, and clipping over the AOI.

✅ Extract flood pixels by applying a threshold of -20 for both periods, and create binary images where pixels are set to 1 for flooded areas and 0 for non-flooded areas.

✅ Create a flood mask (flood\_mask) by applying the flood image as a mask, retaining only flooded areas and masking out non-flooded areas.

```

---

### 💡 **Prompt 2: Visualization of Flood Mask and Water Bodies**

```

Your task is to visualize the flood mask and water bodies for the area of interest:

✅ Display the flood mask on the map with a "red" color.

✅ Extract the water bodies by applying a threshold of < -20 for both before and after images, and display the masked water bodies on the map with a "blue" color.

✅ Calculate flood statistics by applying `ee.Image.pixelArea()` algorithm with `.reduceRegion()` and use the "sum" reducer to calculate the statistics over the AOI.

✅ Divide the flood statistics by 1,000,000 to get the area in square kilometers and print the result in the console.

✅ Add a legend to display both the flood mask and water body.

```

---

### 💡 **Prompt 3: Damage Assessment using Population Data**

```

Next, assess the damage caused by the flood using population data:

✅ Use the GHS Population Grid dataset: 'JRC/GHSL/P2023A/GHS\_POP'.

✅ Apply the same date filters as used for Sentinel-1 to get the population data for the specific period.

✅ Create a mask based on the population data where the population is affected by the flood.

✅ Apply the population mask to the flood mask and visualize the result to show affected populations.

```

# View code in engine
[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)](https://code.earthengine.google.com/ff3c3e3013aeab89a248a99a5b848de2?noload=true)

---

## 🗂️ Output Summary

- ✅ Flood Mask (before and after the flood)
- ✅ Water Body Extraction (masked areas displayed in blue)
- ✅ Flood Area Calculation (in square kilometers)
- ✅ Damage Assessment Visualization (affected population areas overlaid on flood mask)
