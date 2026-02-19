# Analysis of Fatal Police Shootings in the US

A comprehensive data analysis project examining fatal police shootings in the United States from 2015, including demographic patterns, geographic distribution, and socioeconomic correlations.

## 📊 Project Overview

This project analyzes The Washington Post's database of fatal police shootings in the US, combined with US Census data to explore relationships between police violence, poverty rates, education levels, and racial demographics across different states and cities.

**Data Sources:**
- **Fatal Police Shootings Database** (The Washington Post, 2015-2017)
- **US Census Data 2015:**
  - Median Household Income
  - Poverty Rates
  - High School Graduation Rates
  - Racial Demographics by City

## 🔧 Technologies Used

- **Python** - Primary programming language
- **Pandas** - Data manipulation and analysis
- **Plotly** - Interactive visualizations (choropleth maps, bar charts, pie charts, box plots)
- **Seaborn** - Statistical visualizations (KDE plots, regression plots, joint plots)
- **Matplotlib** - Static plotting and customization
- **NumPy** - Numerical computations

## 📈 Key Findings

### Demographics of Victims
- **Gender:** Overwhelming majority of victims are male (~95%)
- **Age:** 21% of victims were under 25 years old; most common age range 22-39 years
- **Race:** Nearly half of victims were White, followed by Black and Hispanic individuals
- **Mental Health:** 25% of victims showed signs of mental illness

### Geographic Patterns
- **Poverty:** Highest rates in Southern states (Mississippi ~27%), lowest on East Coast
- **Police Killings by City:** Los Angeles, Phoenix, Houston, and Chicago lead in total numbers
- **Regional Correlation:** Southern states show higher poverty and lower high school graduation rates

### Armed vs. Unarmed
- The vast majority of victims were armed (most commonly with guns)
- Unarmed victims represent a significant minority of cases

### Temporal Trends
- Data spans 2015-2017 showing a decreasing trend in fatal shootings over this period

## 🗂️ Project Structure
├── data/
│   ├── Deaths_by_Police_US.csv          # Main fatalities dataset
│   ├── Median_Household_Income_2015.csv # Income data by city
│   ├── Pct_People_Below_Poverty_Level.csv
│   ├── Pct_Over_25_Completed_High_School.csv
│   └── Share_of_Race_By_City.csv        # Demographic composition
├── notebooks/
│   └── police_shootings_analysis.ipynb  # Main analysis notebook
└── README.md
plain
Copy

## 🚀 Getting Started

### Prerequisites
# 📦 Installation

```bash
pip install pandas numpy plotly seaborn matplotlib
```

## Setup

1. Clone the repository
2. Ensure all CSV files are in the `data/` directory
3. Open the Jupyter notebook or run the Python script

---

# ▶️ Running the Analysis

```python
# Load required libraries
import pandas as pd
import numpy as np
import plotly.express as px
import seaborn as sns
import matplotlib.pyplot as plt

# Load datasets
df_fatalities = pd.read_csv('Deaths_by_Police_US.csv', encoding="windows-1252")
df_hh_income = pd.read_csv('Median_Household_Income_2015.csv', encoding="windows-1252")
# ... load additional datasets
```

---

# 📊 Visualizations Created

* **Choropleth Maps** – Poverty rates and police killings by US state
* **Interactive Bar Charts** – State rankings for various metrics
* **Dual-Axis Line Charts** – Relationship between poverty and education
* **KDE Plots** – Age distributions by race
* **Box Plots** – Age and manner of death by gender
* **Pie Charts** – Racial composition and mental health status
* **Stacked Bar Charts** – Racial makeup by state
* **Regression Plots** – Correlation analysis between variables

---

# 🔍 Methodology

## Data Cleaning

* Handled missing values (`NaN`) by substitution with `0` where appropriate
* Converted data types for numerical analysis
* Removed duplicates (none found in original datasets)
* Standardized geographic area names for merging datasets

## Analysis Techniques

* **Descriptive Statistics** – Groupby operations, aggregations
* **Correlation Analysis** – Linear regression between poverty and education
* **Geographic Analysis** – State and city-level aggregations
* **Demographic Analysis** – Race and gender breakdowns
* **Temporal Analysis** – Year-over-year trend analysis

---

# 💡 Key Insights

## Socioeconomic Correlations

* Inverse relationship between high school graduation rates and poverty rates
* States with higher education levels tend to have lower poverty rates
* Southern states consistently show worse outcomes on both metrics

## Racial Disparities

* Different age distributions across racial groups
* Black and Hispanic victims tend to be younger on average
* White victims show wider age distribution, including elderly individuals

## Law Enforcement Patterns

* Most dangerous cities don't always align with highest poverty rates
* Armed status significantly affects encounter outcomes
* Mental illness factor present in 1/4 of all cases

---

# 📝 Notes

* Data covers the period from January 1, 2015, with most analysis focused on 2015–2017
* The Washington Post database is continuously updated; this analysis uses a specific snapshot
* Census data from 2015 provides socioeconomic context but may not reflect current conditions

---

# 📚 Data Source Attribution

Data compiled by **The Washington Post** from:

* Law enforcement websites
* Local news reports
* Social media
* Independent databases (*"Killed by Police"*, *"Fatal Encounters"*)

US Census data provides demographic and socioeconomic context.
