# Global Development Statistics Explorer

Statistics and probability case study using a country-level dataset with demographic, economic, environmental, and infrastructure indicators to understand global development patterns.

## Overview

This project uses a dataset of 229 countries and territories, each described by around 50 variables such as population, GDP, sectoral shares, connectivity, CO₂ emissions, energy, water, and sanitation indicators. [file:13]  
The goal is to apply core statistics and probability concepts to explore distributions, compare regions, and analyze relationships between development indicators using Python. [file:13]

## Dataset

- **Source:** `country_profile_variables.csv` (UN-style country profile data). [file:13]  
- **Rows:** 229 countries/territories. [file:13]  
- **Columns:** ~50 indicators. [file:13]

Example columns: [file:13]

- Identification and geography:  
  - `country`, `Region`, `Surface area (km2)`  
- Demographics:  
  - `Population in thousands (2017)`, `Population density (per km2, 2017)`, `Sex ratio (m per 100 f, 2017)`  
- Economy:  
  - `GDP: Gross domestic product (million current US$)`  
  - `GDP growth rate (annual %, const. 2005 prices)`  
  - `GDP per capita (current US$)`  
  - `Economy: Agriculture (% of GVA)` and other sectoral shares  
- Connectivity & technology:  
  - `Mobile-cellular subscriptions (per 100 inhabitants).1`  
  - `Individuals using the Internet (per 100 inhabitants)`  
- Environment:  
  - `Threatened species (number)`  
  - `Forested area (% of land area)`  
  - `CO2 emission estimates (million tons/tons per capita)`  
  - `Energy production, primary (Petajoules)`  
  - `Energy supply per capita (Gigajoules)`  
- Water & sanitation:  
  - `Pop. using improved drinking water (urban/rural, %)`  
  - `Pop. using improved sanitation facilities (urban/rural, %)`  
- Aid:  
  - `Net Official Development Assist. received (% of GNI)`  

Some variables use codes like `-99` for missing data and combined values like `x/y` that need parsing before analysis. [file:13]

## Objectives

- Use descriptive statistics to summarize key development indicators by country and region. [file:13]  
- Apply probability and statistics concepts to real data (e.g., distributions, quantiles, conditional subsets). [file:13]  
- Explore relationships between GDP, population, environment, and infrastructure variables. [file:13]  
- Visualize global patterns and regional differences in development metrics. [file:13]

## Methods and Analysis

The notebook typically covers:

- **Data loading and inspection**  
  - Load `country_profile_variables.csv` into a Pandas DataFrame. [file:13]  
  - Inspect head, shape, and schema to understand variable types. [file:13]

- **Data cleaning and preparation**  
  - Handle missing values coded as `-99`. [file:13]  
  - Select and clean numeric columns (e.g., GDP, population, density). [file:13]  
  - Optionally parse compound fields like `X/Y` into separate numeric columns.

- **Descriptive statistics & probability**  
  - Compute mean, median, variance, and quantiles for GDP per capita, population, and density. [file:13]  
  - Explore distributions (histograms/KDE plots) for key variables. [file:13]  
  - Analyze regional distributions (e.g., GDP per capita by `Region`). [file:13]

- **Relationships and visualizations**  
  - Scatter plots of GDP per capita vs. population, density, or internet usage. [file:13]  
  - Boxplots/violin plots by region to compare development levels. [file:13]  
  - Correlation heatmaps for selected numeric features. [file:13]

These steps illustrate how statistics and probability support reasoning about real-world development questions.

## Tech Stack

- **Language:** Python 3  
- **Libraries:**  
  - `numpy`, `pandas` for data and calculations  
  - `matplotlib`, `seaborn` for visualizations [file:13]  
- **Environment:** Jupyter / Google Colab [file:13]

## How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/<your-username>/global-development-stats-explorer.git
   cd global-development-stats-explorer

2. Create and activate a virtual environment (optional but recommended):
   python -m venv .venv
   source .venv/bin/activate   # On Windows: .venv\Scripts\activate

3. Install dependencies:
   pip install -r requirements.txt

4. Place the dataset file in the project folder (for example: data/US_honey_dataset.csv) and      update the path in the notebook if needed.

5. Open the notebook: Jupyter Notebook 10_Case_Study_Statistics_and_Probability.ipynb
   or upload it to Google Colab and make sure the CSV path   (/content/country_profile_variables.csv) is correct.

