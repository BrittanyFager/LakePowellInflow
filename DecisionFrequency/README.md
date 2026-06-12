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


5. Run the notebook interactively in your browser using [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/YOUR-USER/YOUR-REPO/HEAD)

Binder requires:

- no installation  
- no Python setup  
- no package management  

Everything runs in a temporary cloud environment.

---

## 📦 Do Binder Users Need to Install Packages?

**No.**  
Binder automatically installs all required Python packages using the environment files in this repository (e.g., `requirements.txt` or `environment.yml`).

Users do **not** need to install:

- Python  
- Jupyter  
- pandas  
- numpy  
- matplotlib  

Everything is handled by Binder.


