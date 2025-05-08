## 🏭 Air Quality Assessment over New Delhi

As an **Air Quality Researcher** specializing in remote sensing, the objective is to proficiently employ the **Google Earth Engine JavaScript API** for air quality assessments over New Delhi to retrieve, filter, and visualize Sentinel-5P NO2 images for further analysis and classification. 

### 💡 Preprocessing Steps:

1. **Retrieve Sentinel-5P NO2 Image Collection**
   The Sentinel-5P NO2 data is available in the following collection:

   ```javascript
   var no2Collection = ee.ImageCollection("COPERNICUS/S5P/NRTI/L3_NO2");
   ```

2. **Filter the Collection by Date Range**
   The dataset should be filtered to include images from **November 1, 2023, to November 30, 2024**:

   ```javascript
   var filteredNO2 = no2Collection.filterDate('2024-11-01', '2024-11-30');
   ```

3. **Extract Suitable Bands for NO2 Surface Results**
   To focus on the NO2 data, select the relevant band for nitrogen dioxide:

   ```javascript
   var no2 = filteredNO2.select('NO2_column_number_density');
   ```

4. **Extract Administrative Boundary of New Delhi**
   You will use the provided feature collection to extract the boundary of New Delhi:

   ```javascript
   var newDelhi = ee.FeatureCollection("projects/sat-io/open-datasets/geoboundaries/CGAZ_ADM1")
     .filter(ee.Filter.eq('shapeName', 'Delhi'));
   ```

5. **Apply Visualization Parameters**
   Set the color palette to visualize NO2 levels with a range from "white" to "red" as follows:

   ```javascript
   var visParams = {
     min: 0.0,
     max: 0.0005,
     palette: ['white', 'blue', 'green', 'orange', 'red']
   };
   ```

6. **Visualize the Data**
   Add the filtered NO2 image to the map with the chosen visualization parameters and overlay the boundary of New Delhi:

   ```javascript
   var no2Map = no2.mean().clip(newDelhi);
   Map.centerObject(newDelhi, 10);
   Map.addLayer(no2Map, visParams, 'NO2 Levels');
   Map.addLayer(newDelhi.style({color: 'black', fillColor: '00000000'}), {}, 'New Delhi Boundary');
   ```

7. **Export Image (Optional)**
   Optionally, you can export the processed image for further use:

   ```javascript
   Export.image.toDrive({
     image: no2Map,
     description: 'NO2_Image_NewDelhi',
     scale: 1000,
     region: newDelhi
   });
   ```

---
[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)](https://code.earthengine.google.com/89c41fd70b2b8d23a1bbe7a8f5a1b5d4?noload=true)

---

##  📌 Prompt Log: Air Quality Assessment over New Delhi using preprocessed NO₂ Data

### 💡 Prompt 1: Composite Images & Statistics

Continuing your role as an Air Quality Researcher, your next task is to display different composites of NO₂ images in the Google Earth Engine JavaScript API for advanced air quality assessments over New Delhi.

**Task: Retrieve Composite Image Statistics**

From the previous code, select the band used again and obtain the **mean**, **median**, **mode**, **maximum**, and **minimum** composite images for NO₂. Display each composite by clipping them over the New Delhi Boundary in the map to understand the NO₂ distribution and concentration comprehensively.

**Task: Print Results**

Print out all the **mean values** from the Mean Composite in the console.

---

### 💡 Prompt 2: Image Classification

**Task: Classification of NO₂ Levels**

Based on the statistical values of the mean NO₂ composite, which is `0.00017628374591946718 mol/m²`, create four distinct concentration classes:

- "Low Concentration of NO₂"
- "Moderate Concentration of NO₂"
- "High Concentration of NO₂"
- "Highest Concentration of NO₂"

Use a suitable classification algorithm to define concentration thresholds for each class. Display the classified result on the map, and clip the resulting classified image with the **New Delhi Boundary**.

**Map Visualization**

Use the following colours to represent each class in the classified image:

- Green: Low Concentration of NO₂
- Orange: Moderate Concentration of NO₂
- Red: High Concentration of NO₂
- Black: Highest Concentration of NO₂

Create a **legend** for the following color range to identify the classes on the map.

---

### 💡 Prompt 3: Print Classified Results

**Task: Output Classified Values**

Please print the results of the classified image to the console, specifically highlighting the NO2 concentration values for each class, along with a description of the classified image. Additionally, include a comment labeled "// Step 9: Create a Legend for the Classification" from the previous code, and generate the final code again.

---

[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)](https://code.earthengine.google.com/e0b7188cb089244dd5c20cf704cb3966?noload=true)

---

## 🧪 Prompt Log Continued: Daily NO₂ Analysis and Time Series Visualization over New Delhi

In this exercise, you continue your role as an **Air Quality Researcher** using the **Google Earth Engine JavaScript API** to assess NO₂ concentration patterns over New Delhi throughout November 2024.

---

### 💡 Prompt 4: Continuing from Code

Above is the code from the last prompt you are working on as an Air Quality Researcher, specializing in remote sensing and proficient in utilizing the Google Earth Engine JavaScript API for air quality assessments in New Delhi.

*(Code was reused or adapted here for further analysis)*

---

### 💡 Prompt 5: Display Daily NO₂ Level Classes

**Task:**  
Now display **daily level classes** of NO₂ values based on the entire month of November over New Delhi.

---

### 💡 Prompt 6: Time Series Chart and Export

**Task:**  
Now generate a **time series chart** illustrating the **daily concentration values** of NO₂ over New Delhi for **November 2024**.

**Additional Output:**  
Export the **daily NO₂ values** over New Delhi in **CSV format** for further offline analysis.

---
## ⚙️ View live code in action
[![View in Earth Engine](https://img.shields.io/badge/View%20in-Earth%20Engine-008000?logo=google)](https://code.earthengine.google.com/d5c4caf61e833bc239badc3af01bf34e?noload=true)
