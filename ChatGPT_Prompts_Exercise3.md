## 🧪 Prompt Log Exercise 3: Mapping Drought Indices over Indonesia

In this exercise, you assume the role of a **Climatologist** using the **Google Earth Engine JavaScript API** to monitor and analyze drought conditions in **Indonesia** using several drought indices.

---

### 💡 Prompt 1: Vegetation Condition Index (VCI)

**Objective:**
Calculate the **Vegetation Condition Index (VCI)** for Indonesia.

**Dataset:**
`MODIS/061/MOD13A2` (Terra Vegetation Indices 16-Day Global 1km)

**Steps:**

* Calculate **NDVI minimum** and **NDVI maximum** for 2022.
* Use these values to compute VCI.
* Clip the results using Indonesia's boundary:
  `ee.FeatureCollection("USDOS/LSIB_SIMPLE/2017")`
* Time Interval: January 1, 2022 – December 31, 2022
* Visualize VCI with **10 distinct color representations**

---

### 💡 Prompt 2: Temperature Condition Index (TCI)

**Objective:**
Calculate the **Temperature Condition Index (TCI)** for Indonesia.

**Dataset:**
`MODIS/061/MOD11A1` (Terra Land Surface Temperature and Emissivity Daily Global 1km)

**Steps:**

* Calculate **LST minimum** and **LST maximum** for 2022.
* Use these to derive TCI.
* Clip results with Indonesia’s boundary:
  `ee.FeatureCollection("USDOS/LSIB_SIMPLE/2017")`
* Time Interval: January 1, 2022 – December 31, 2022
* Visualize with **10 distinct colors**

---

### 💡 Prompt 3: Drought Severity Index (DSI)

**Objective:**
Calculate the **Drought Severity Index (DSI)** for Indonesia.

**Datasets:**

* NDVI: `MODIS/061/MOD13A2`
* ET & PET: `MODIS/061/MOD16A2`

**Steps:**

* Calculate DSI using NDVI, ET, and PET.
* Clip the result using Indonesia’s boundary from:
  `ee.FeatureCollection("USDOS/LSIB_SIMPLE/2017")`
* Time Interval: January 1, 2022 – December 31, 2022
* Visualize DSI with **10-color representation**

---

### 💡 Prompt 4: Time Series Chart for VCI

**Objective:**
Generate a **time series chart** using `ui.Chart.image.doySeriesByRegion` for **VCI**.

**Steps:**

* Use the most suitable **band** and appropriate **reducer**.
* Apply it to the **geometry** defined in the code.
* Time duration must match earlier settings.
* Display the chart in the **console**.
* Then, **copy and paste the code** from the editor into ChatGPT for review or improvement.

---
