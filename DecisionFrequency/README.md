# Lake Powell Inflow Comparisons
## Comparisons of Lake Powell inflow projections and scenarios

This repository contains tools for analyzing Lake Powell inflow behavior, scenario volatility, and operational decision frequency using CRSS-based hydrologic data.

### Repository Contents

- **DecisionFrequency/DecisionFrequency.ipynb**  
  Models how shifting from monthly to annual operational decision points affects reservoir behavior using CRSS output time series.

- **Powell level analysis.xlsx**  
  Contains inflow, elevation, storage, and outflow time series.

- **elevPowell.csv**  
  USBR elevation–area–capacity lookup table used for converting between elevation, storage, and surface area.

---


### File Descriptions

- **DecisionFrequency.ipynb**  
  Main analysis notebook. Implements three reservoir‑operation scenarios:
  - Monthly release decisions  
  - 6‑month block release decisions  
  - Annual release decisions  

  Each scenario uses a mass‑balance model with:
  - Powell inflow  
  - Elevation–storage conversion  
  - A 95%‑of‑inflow release rule when elevation falls below 3525 ft  
  - A base release of 8.3 MAF/year  

- **Powell level analysis.xlsx**  
  Contains the Powell inflow, elevation, and storage time series used as model inputs.

- **elevPowell.csv**  
  USBR elevation–area–capacity lookup table used to convert between:
  - Elevation → Storage  
  - Storage → Elevation  
  - Elevation → Surface Area  

---

## Run Online (No Installation Required)
This folders contains  DecisionFrequency.ipynb Jupyter notebooks.
If you do not want to install Python or Jupyter locally, you can run everything online using Binder, a free service from Project Jupyter.

Launching Your Notebook on Binder
Go to [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/BrittanyFager/LakePowellInflow/HEAD)

This link will take you to an instance of jupyter notebooks online.

On the left side of the enviroment you will see 3 folders as seen here on this github along with this readme and the requirements.txt.

Navigate to the DecisionFrequency folder. 

In this folder is the file DecisionFrequency.ipynb double click it top open it and you can run and edit it in this instance.


---

## Citations

HydrologyScenarios.xlsx Salehabadi, H., et al. (2024). Quantifying and Classifying Streamflow Ensembles Using a Broad Range of Metrics for an Evidence‑Based Analysis: Colorado River Case Study.
Water Resources Research.
https://doi.org/10.1029/2023WR036401 (doi.org)

Lake_Powell_2018_ElevAreaCap_calc.csv U.S. Geological Survey (2018). Elevation–area–capacity tables for Lake Powell, 2018.
https://doi.org/10.5066/F7X63K0Z

Jupyter et al. (2018). Binder 2.0 – Reproducible, Interactive, Sharable Environments for Science at Scale.  
DOI: 10.25080/Majora‑4af1f417‑011
