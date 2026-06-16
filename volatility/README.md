
# Lake Powell Flow Volatility Analysis

This folder contains the workflow for analyzing **year‑to‑year volatility in annual natural inflow to Lake Powell** across all hydrology scenario ensembles.  
The analysis quantifies how often large drops occur, how many ensembles experience them, and where historical events (e.g., 2005–2006, 2019–2020, 2025–2026) fall within the distribution.

---

## Files in This Folder

volatility/
│
├── Volatility.ipynb
├── HydrologyScenarios.xlsx
└── README.md


### File Descriptions

- **Volatility.ipynb**  
  Main notebook performing:
  - Extraction of annual flows from all ensembles and traces  
  - Construction of year‑to‑year flow pairs  
  - Computation of annual flow drops (MAF)  
  - Binning of drops into 1‑MAF categories  
  - Counting how many ensembles experience drops of each magnitude  
  - Plotting the distribution of flow declines  
  - Highlighting historical drops (2005–2006, 2019–2020, 2025–2026)

- **HydrologyScenarios.xlsx**  
  Contains all hydrology scenario ensembles.  
  Each sheet represents one ensemble, with:
  - Column 1 = Year  
  - Columns 2+ = individual traces  

- **Lake_Powell_2018_ElevAreaCap_calc.csv**  
  Elevation–area–capacity table (not directly used in volatility plots, but included for completeness).

---

## What the Code Does

### 1. Load all hydrology scenario ensembles  
The notebook reads every sheet in `HydrologyScenarios.xlsx` except metadata sheets.  
Each ensemble may contain dozens of traces.

### 2. Extract annual flows  
For every ensemble and every trace, the notebook builds a long dataframe of:

- Ensemble  
- Trace  
- YearIndex  
- Year  
- Annual natural flow (MAF)

### 3. Compute year‑to‑year flow pairs  
For each trace:

- `Inflow_MAF` (year t)  
- `NextFlow_MAF` (year t+1)  
- `Difference_MAF = NextFlow_MAF – Inflow_MAF`  

Only valid consecutive years are kept.

### 4. Filter to meaningful hydrologic cases  
The notebook keeps only:

- Starting flow < 12.5 MAF  
- Negative differences (drops)  
- Next year flow > 0  

### 5. Bin drop magnitudes  
Drops are grouped into **1‑MAF bins** from 0 to 13 MAF.

### 6. Count ensembles per drop magnitude  
The notebook counts how many ensembles experience a drop of each size.

### 7. Plot the distribution  
The final figure shows:

- Bars = number of ensembles experiencing a drop of each magnitude  
- Vertical red lines marking historical drops  
- X‑axis limited to 0–10 MAF for clarity  


---


## Output File

The notebook generates:

- **AllHydrology_YearToYearPairs.csv**  
  Contains every valid year‑to‑year flow pair across all ensembles and traces.

This file is used for volatility analysis and plotting.
---

## Run Online (No Installation Required)
This folders contains  DecisionFrequency.ipynb Jupyter notebooks.
If you do not want to install Python or Jupyter locally, you can run everything online using Binder, a free service from Project Jupyter.

Launching Your Notebook on Binder
Go to [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/BrittanyFager/LakePowellInflow/HEAD)

This link will take you to an instance of jupyter notebooks online.

On the left side of the enviroment you will see 3 folders as seen here on this github along with this readme and the requirements.txt.

Navigate to the volatility folder. 

In this folder is the file volatility.ipynb double click it top open it and you can run and edit it in this instance.

---
## Citations
---
HydrologyScenarios.xlsx Salehabadi, H., et al. (2024). Quantifying and Classifying Streamflow Ensembles Using a Broad Range of Metrics for an Evidence‑Based Analysis: Colorado River Case Study.
Water Resources Research.
https://doi.org/10.1029/2023WR036401 (doi.org)

