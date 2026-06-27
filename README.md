# Day-11-SIC
colab link - https://colab.research.google.com/drive/1QV1mtZlQ6Ol93O8ATnzLdP2dwjcsy0L8?usp=sharing



# Analysis and Geographic Visualization of NFHS-5 State Health Indicators Using Python

## Overview

This project analyzes state-level health indicators from the **National Family Health Survey (NFHS-5)** using Python. It focuses on cleaning, processing, analyzing, and visualizing public health data to identify patterns across Indian states.

Using **Pandas**, **Matplotlib**, and **Folium**, the project explores relationships between obesity, anaemia, hypertension, and high blood sugar while presenting the results through statistical visualizations and an interactive geographic dashboard.

---

# Objectives

* Load and preprocess the NFHS-5 state-level dataset.
* Clean and transform health indicator data.
* Compare obesity, anaemia, hypertension, and blood sugar prevalence across Indian states.
* Calculate the gender obesity gap for each state.
* Perform exploratory data analysis (EDA) using statistical methods.
* Visualize regional health patterns using interactive geographic maps.
* Develop an interactive Folium dashboard for public health analysis.

---

# Dataset

**Source:** National Family Health Survey (NFHS-5)

The analysis includes the following health indicators:

* Obesity (Women)
* Obesity (Men)
* Anaemia (Children)
* Anaemia (Women)
* High Blood Sugar (Women)
* High Blood Sugar (Men)
* Hypertension (Women)
* Hypertension (Men)

Only **Total** (state-level) records were used for the analysis.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Folium
* Jupyter Notebook / Google Colab

---

# Project Structure

```
Analysis-and-Geographic-Visualization-of-NFHS5/

│── data/
│   ├── NFHS5_State_Data.csv
│   └── cleaned_nfhs5.csv
│
│── notebook/
│   └── NFHS5_Health_Analysis.ipynb
│
│── output/
│   ├── Correlation_Matrix.png
│   ├── Hypertension_BarChart.png
│   ├── Anaemia_vs_Obesity.png
│   └── India_Health_Dashboard.html
│
├── india_states.geojson
├── README.md
├── requirements.txt
└── LICENSE
```

---

# Project Workflow

## Phase 1 – Data Preparation

* Loaded the NFHS-5 dataset
* Selected relevant health indicators
* Converted non-numeric values into numeric format using `pd.to_numeric(errors='coerce')`
* Removed invalid values
* Created a new feature:

```
Gender_Obesity_Gap = Obesity_Women − Obesity_Men
```

---

## Phase 2 – Exploratory Data Analysis (EDA)

Performed statistical analysis including:

* Pearson Correlation Analysis
* Correlation Matrix
* Top 10 Hypertension Comparison (Men vs Women)
* Anaemia vs Obesity Scatter Plot
* Gender Obesity Gap Analysis

### Key Findings

* Strong positive correlation between male and female obesity.
* Strong positive correlation between male and female hypertension.
* Anaemia in children showed a weak negative correlation with adult obesity.
* Several northern states exhibited a larger gender obesity gap.

---

## Phase 3 – Geographic Visualization

Built an interactive health dashboard using **Folium** featuring:

* Interactive India Map
* Choropleth visualization based on Women's Obesity (%)
* State-wise Circle Markers
* Interactive popups displaying:

  * State Name
  * Obesity (Women & Men)
  * Anaemia (Children & Women)
  * High Blood Sugar (Women & Men)
  * Hypertension (Women & Men)

---

# Visualizations

The project generates:

* Correlation Matrix
* Pearson Correlation Analysis
* Hypertension Comparison Bar Chart
* Anaemia vs Obesity Scatter Plot
* Interactive Folium Health Dashboard

---

# Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/Analysis-and-Geographic-Visualization-of-NFHS5.git
```

Move into the project directory:

```bash
cd Analysis-and-Geographic-Visualization-of-NFHS5
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib folium
```

---

# Running the Project

Open the notebook:

```bash
jupyter notebook
```

or upload it to **Google Colab**.

Run all cells sequentially.

The interactive dashboard will be generated as:

```
India_Health_Dashboard.html
```

---

# Results

The project provides:

* Cleaned and structured NFHS-5 health data.
* Statistical insights into obesity, anaemia, hypertension, and blood sugar prevalence.
* Gender-based obesity comparison.
* Correlation analysis among major health indicators.
* Interactive geographic visualization of health trends across Indian states.

---

# Future Improvements

* District-level health analysis
* Comparison with previous NFHS surveys
* Streamlit web dashboard
* Machine Learning models for health-risk prediction
* Time-series visualization of health indicators

---

# Author

**Sagnik Sannigrahi**

B.Tech – Computer Science and Engineering
SRM Institute of Science and Technology

---

# License

This project is developed for educational and academic purposes. The dataset belongs to the National Family Health Survey (NFHS-5), Government of India.
