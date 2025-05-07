## 🧪 Preprocessing Task Before Start Prompting: Preparing NO₂ Data for Air Quality Analysis over New Delhi

As an **Air Quality Researcher** specializing in remote sensing, the objective is to proficiently employ the **Google Earth Engine JavaScript API** for air quality assessments over New Delhi. This initial task sets the stage for further analysis and classification.

---

### 🔹 Task 1: Retrieve Sentinel-5P NO₂ Imagery

**Dataset:**  
`ee.ImageCollection("COPERNICUS/S5P/NRTI/L3_NO2")`

---

### 🔹 Task 2: Filter and Extract Suitable Bands

- Focus on selecting the appropriate band from the Sentinel-5P dataset to ensure accurate representation of NO₂ over the surface.

---

### 🔹 Task 3: Apply Date Filter

- Temporal Range: **November 1, 2023 – November 30, 2023**

---

### 🔹 Task 4: Visualization Parameters

- Use the following color palette for displaying NO₂ concentration:
  - `"white", "blue", "green", "orange", "red"`

---

### 🔹 Task 5: Spatial Representation

- Extract the **administrative boundary of New Delhi**.
- Use this FeatureCollection to clip the imagery:
  ```javascript
  ee.FeatureCollection("projects/sat-io/open-datasets/geoboundaries/CGAZ_ADM1")
    .filter(ee.Filter.eq('shapeName', 'Delhi'));

---

## 🧪 Prompt Log Exercise 2: Air Quality Assessment over New Delhi using NO₂ Data

### 🔹 Prompt 1: Composite Images & Statistics

Continuing your role as an Air Quality Researcher, your next task is to display different composites of NO₂ images in the Google Earth Engine JavaScript API for advanced air quality assessments over New Delhi.

**Task: Retrieve Composite Image Statistics**

From the previous code, select the band used again and obtain the **mean**, **median**, **mode**, **maximum**, and **minimum** composite images for NO₂. Display each composite by clipping them over the New Delhi Boundary in the map to understand the NO₂ distribution and concentration comprehensively.

**Task: Print Results**

Print out all the **mean values** from the Mean Composite in the console.

---

### 🔹 Prompt 2: Image Classification

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

### 🔹 Prompt 3: Print Classified Results

**Task: Output Classified Values**

Print out the results of the classified image into the console, focusing on printing the **NO₂ concentration values** of each class separately with a **description** from the classified image.

---

## 🧪 Prompt Log Continued Exercise 2: Daily NO₂ Analysis and Time Series Visualization over New Delhi

In this exercise, you continue your role as an **Air Quality Researcher** using the **Google Earth Engine JavaScript API** to assess NO₂ concentration patterns over New Delhi throughout November 2023.

---

### 🔹 Prompt 4: Continuing from Code

Following is the code you are working on as an Air Quality Researcher specializing in remote sensing, proficient in utilizing Google Earth Engine JavaScript API for air quality assessments over New Delhi.

*(Code was reused or adapted here for further analysis)*

---

### 🔹 Prompt 5: Display Daily NO₂ Level Classes

**Task:**  
Display **daily level classes** of NO₂ values based on the entire month of November over New Delhi.

---

### 🔹 Prompt 6: Time Series Chart and Export

**Task:**  
Generate a **time series chart** illustrating the **daily concentration values** of NO₂ over New Delhi for **November 2023**.

**Additional Output:**  
Export the **daily NO₂ values** over New Delhi in **CSV format** for further offline analysis.

---
