# Analysing Pharmaceutical Sales Data

This project provides a comprehensive analysis of daily pharmaceutical sales data. Using Python and data science libraries, it processes sales records to identify top-performing drug categories and seasonal trends, specifically focusing on respiratory medications. this project is from roadmap.sh 

[roadmap.sh/projects/pharmaceutical-sales-data
](https://roadmap.sh/projects/pharmaceutical-sales-data)
---

## 📋 Project Overview

The goal of this analysis is to transform raw sales data into actionable insights. The script processes a dataset containing various drug categories classified by **ATC (Anatomical Therapeutic Chemical)** codes.

### Key Features:
* **Total Sales Calculation:** Aggregates sales for all major drug categories.
* **Trend Identification:** Visualizes the monthly sales flow for Respiratory drugs (R03).
* **Performance Benchmarking:** Identifies the highest-selling products and specific monthly leaders.
* **Data Visualization:** Generates professional bar charts and line graphs for report usage.

---

## 🛠️ Technical Stack

* **Language:** Python
* **Libraries:** * `Pandas`: For data manipulation and CSV processing.
    * `Matplotlib`: For generating high-quality visualizations.
    * `OS`: For directory and file management.

---

## 📖 Code Explanation

The script `Analysis.py` follows a logical data science workflow:

### 1. Data Loading & Preprocessing
The code begins by checking if `salesdaily.csv` exists. Once confirmed, it loads the data and converts the `datum` column into a `datetime` object. This is crucial for accurate time-series analysis (grouping by month/year).

### 2. Aggregation Logic
* **Total Sales:** It sums the columns representing different ATC codes (M01AB, N02BE, etc.) and sorts them to find the "Best Seller."
* **Custom Functions:** The `get_top_3_monthly` function filters the dataframe for a specific year and month, then returns the three most popular drugs for that period.

### 3. Visualization Engine
The script generates two primary plots:
* **Bar Chart:** Uses `kind='bar'` to compare the volume of different drug categories.
* **Line Plot:** Specifically targets the 'R03' category, plotting its sales over time to show seasonality.

---

## 📊 Visualization & Data Insights

Based on the generated images, here is the analysis:

### 1. Total Sales Analysis (Bar Chart)
This chart displays the total quantity sold across different ATC categories.
* **Dominant Category:** **N02BE** (typically Paracetamol/Analgesics) shows the highest volume by a significant margin.
* **Observation:** The high volume of N02BE suggests a high-frequency demand for over-the-counter pain relief compared to specialized medications like N05C (Hypnotics/Sedatives).

### 2. Monthly Sales Trend for R03 (Line Graph)
This graph tracks Respiratory drug sales (R03) throughout the months.
* **Trend Analysis:** There is noticeable fluctuation in sales. Typically, R03 drugs (often used for asthma or coughs) show peaks during specific seasons (e.g., winter or high-allergy seasons).
* **Insight:** The dips and peaks indicate that stock levels for respiratory medicine should be managed seasonally rather than kept at a constant level year-round.

---

## 🗂️ Data Dictionary (ATC Codes)
| Code | Category |
| :--- | :--- |
| **M01AB/AE** | Anti-inflammatory and antirheumatic products |
| **N02BA/BE** | Analgesics (Painkillers) |
| **N05B/C** | Psycholeptics (Anxiolytics/Hypnotics) |
| **R03** | Drugs for obstructive airway diseases (Respiratory) |
| **R06** | Antihistamines for systemic use |
