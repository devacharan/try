# SPDM - Snow Probability Distributed Model – MATLAB Implementation

This repository contains a MATLAB implementation of a version of the Probability Distributed Moisture (PDM) model, a lumped conceptual hydrological model. The model employs a degree day approach for the snow module and is based on the PDM model's probability distribution of storage capacity for soil moisture accounting, linked to a routing component consisting of two parallel linear reservoirs.  

The implementation follows the concepts described in:  
- Moore, R. J. (1985), *The probability-distributed principle and runoff production at point and basin scales*, Hydrological Sciences Journal, 30 (2), 273–297. 
- Moore, R. J. (2007), *The PDM rainfall–runoff model*, Hydrology and Earth System Sciences,11 (1), 483–499. doi: 10.5194/hess-11-483-2007.
- Book by TW, Rainfall-Runoff Modelling In Gauged And Ungauged Catchments?

---

## Contents
The repository includes MATLAB `.m` files implementing different components of the model:
- **Snow module** – snow_degree.m - uses degree day factor that defines the amount of snow melt per day per unit increase in temperature
- **Soil moisture module** – sma_pd3.m - uses PDM's probability-distributed storage capacity for soil moisture accounting; a Pareto distribution is assumed since it is the one most commonly used
- **Routing module** – r_2par.m - uses PDM's fraction of effective rainfall going through two parallel linear reservoirs for streamflow routing  
- **Performance metrics** – NSE.m, and abias.m - functions for calculating Nash-Sutcliffe Efficiency (NSE) and absolute bias. 
- **Reservoir module** – r_cres.m - simulation of conceptual reservoir behavior
- **Latin hypercube sampling** - lhcube.m - generates a Latin hypercube of N datapoints in the M-dimensional hypercube
- **Info files** –  information about modules
- **Input conditions and parameters** – Step0input.m - function for creating and saving input structure.

---

## Model Inputs and Outputs
- **Inputs**:  
  - Daily precipitation  
  - Daily temperature  
  - Potential evapotranspiration  

- **Output**:  
  - Simulated streamflow at the catchment outlet  

---

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/thorsten1971/pdm-matlab.git
2. Open MATLAB and add the repository folder to the MATLAB path
3. Modify input files and parameter settings as needed for your catchment
