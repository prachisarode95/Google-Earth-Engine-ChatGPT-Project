# 🌍 Geospatial Data Analysis with ChatGPT and Google Earth Engine

This project demonstrates how to use **ChatGPT-generated prompts** and the **Google Earth Engine JavaScript API** to build a series of practical geospatial analyses. It follows exercises from the course *"Introduction to Geospatial Data Analysis with ChatGPT and Google Earth Engine"*, applying real-world use cases like vegetation monitoring, air quality assessment, drought mapping, and flood detection.

---

## 📦 Project Structure

### ✅ Completed Exercises
1. **Integrating ChatGPT with Google Earth Engine**  
2. **Pre-processing Geospatial Data**  
3. **Air Quality Analysis using NO2**  
4. **Mapping Drought Indices**  
5. **Flood Monitoring and Damage Assessment**
6. **Urban Planning and Development**

---

## ✨ Tools Used
- [Google Earth Engine (JavaScript API)](https://code.earthengine.google.com/)
- [ChatGPT Prompt Engineering](https://chat.openai.com/)
- Remote sensing datasets: MODIS, Landsat 8, Sentinel-1, Sentinel-5P, GHS POP, etc.

---

## 💡 Prompt Logs

### 1. 📌 Integrating ChatGPT with Google Earth Engine
Prompts used:
- Display satellite image over Vietnam
- Median composite using Landsat 8 TOA
- Clip using Vietnam boundary from `USDOS/LSIB_SIMPLE/2017`
- Visualize NDVI, NDBI, MNDWI with custom color schemes

---

### 2. 📌 Pre-processing Geospatial Data for NO2 over New Delhi
Prompts used:
- Use Sentinel-5P NO2 dataset
- Filter by date: `2023-11-01` to `2023-11-30`
- Extract band, apply color palette: white, blue, green, orange, red
- Clip with New Delhi boundary from `CGAZ_ADM1`

---

### 3. 📌 Air Quality Analysis (Composites, Classification, Time Series)
Prompts used:
- Generate mean, median, mode, min, max composites for NO2
- Classify NO2 into 4 classes using a threshold
- Display with legend and color codes
- Plot time series using `ui.Chart.image.series`
- Export results to CSV

---

### 4. 📌 Mapping Drought Indices over Indonesia
Prompts used:
- Compute **VCI** using MODIS NDVI (`MOD13A2`)
- Compute **TCI** using MODIS LST (`MOD11A1`)
- Compute **DSI** using NDVI, ET & PET (`MOD16A2`)
- Visualize all indices with color scales
- Clip using Indonesia shapefile from `USDOS/LSIB_SIMPLE/2017`
- Generate time series chart using `ui.Chart.image.doySeriesByRegion`

---

### 5. 📌 Applying ChatGPT and GEE in Flood Monitoring
Prompts used:
- Use Sentinel-1 SAR GRD dataset
- Filter ASCENDING/DESCENDING orbit data
- Compare pre- and post-flood (March vs July 2022)
- Create VH mosaics, extract flood areas with threshold `-20 dB`
- Visualize flood mask (red), water (blue)
- Calculate flood area in sq.km
- Perform **damage assessment** using GHS_POP dataset (`JRC/GHSL/P2023A/GHS_POP`)
- Visualize flood-affected population

---

## 📁 Dataset References

- **Landsat 8 TOA**: `LANDSAT/LC08/C02/T1_TOA`  
- **MODIS NDVI**: `MODIS/061/MOD13A2`  
- **MODIS LST**: `MODIS/061/MOD11A1`  
- **MODIS ET & PET**: `MODIS/061/MOD16A2`  
- **Sentinel-5P NO2**: `COPERNICUS/S5P/NRTI/L3_NO2`  
- **Sentinel-1 SAR GRD**: `COPERNICUS/S1_GRD`  
- **GHS Population**: `JRC/GHSL/P2023A/GHS_POP`  
- **Country boundaries**: `USDOS/LSIB_SIMPLE/2017`, `CGAZ_ADM1`

---

## 📊 Output

Each script outputs:
- Satellite image visualizations
- Statistical summaries (mean, min, max, etc.)
- Time series graphs
- Exported CSV files
- Damage/flood masks and legends

---

## 🙌 Credits

- **Course**: [Introduction to Geospatial Data Analysis with ChatGPT and Google Earth Engine](https://www.earthdatascience.org/)
- **Platform**: [EO College](https://eo-college.org/)
- **Instructor**: [Your Instructor Name if known]
- **Prompt-based Analysis**: Powered by ChatGPT + GEE JavaScript API

---

## 🧠 Author's Note

This project is a hands-on effort to blend AI tools with geospatial science. All results were derived using AI-generated coding prompts and GEE best practices. Feel free to fork and expand it!

---

## 🔗 License

[MIT License](LICENSE)
