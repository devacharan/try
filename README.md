# Probability Distributed Model (PDM) – MATLAB Implementation

This repository contains a MATLAB implementation of the **Probability Distributed Moisture (PDM) model**, a lumped conceptual hydrological model. The model is based on the probability distribution of storage capacity for soil moisture accounting, linked to a routing component consisting of two parallel linear reservoirs.  

The implementation follows the concepts described in:  
- Moore, R. J. (1985), *The probability-distributed principle and runoff production at point and basin scales*, Hydrological Sciences Journal.  
- Moore, R. J. (2007), *The PDM rainfall–runoff model*, Hydrology and Earth System Sciences.  

---

## 📂 Repository Contents
The repository includes MATLAB `.m` files implementing different components of the model:
- **Snow module** – snow_degree.m - handles snow accumulation and melt processes  
- **Soil moisture module** – sma_pd3.m - probability-distributed storage capacity for soil accounting  
- **Routing module** – r_2par.m - two parallel linear reservoirs for streamflow routing  
- **Performance metrics** – NSE.m, abias.m -functions for calculating Nash-Sutcliffe Efficiency (NSE), absolute bias, etc.  
- **Parameter handling** – lhcube.m, Step0input.m, and info.mat  functions for model parameters  
- **Reservoir module** – r_cres.m - simulation of conceptual reservior behavior  

---

## ⚙️ Model Inputs and Outputs
- **Inputs**:  
  - Daily precipitation  
  - Daily temperature  
  - Potential evapotranspiration  

- **Output**:  
  - Simulated streamflow at the catchment outlet  

---

## ▶️ How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/Thorsten1971/pdm-matlab.git
