# PCSAV Method for the Ericksen–Leslie Model

This repository contains the **FreeFem++ (version 4.5)** source files used in the paper

> Ruonan Cao, *A linear, unconditionally stable, second order decoupled method for the Ericksen-Leslie model with SAV approach*, Computers & Mathematics with Applications, 2025.

These files are provided to ensure reproducibility of the numerical experiments, including verification of temporal convergence rates and simulation of singularity dynamics in the Ericksen–Leslie liquid crystal model.

---

## 🧩 Software Environment
- **Software:** [FreeFem++](https://freefem.org/)  
- **Version:** 4.5   
- **Language:** `.edp` (FreeFem++ scripts)  
- **Platform:** Linux / macOS / Windows  
- **Dependencies:** No external packages required (only a standard FreeFem++ 4.5 installation)

## 🧩 File Descriptions
Detailed descriptions of the main files :
- **Example4.1_test_exact_rate_BDF2_NSPROSAV.edp**
This file corresponds to Example 4.1 in the paper. Uses the PCSAV-ECT scheme with an exact solution to verify the temporal convergence rate.

- **Example4.1_test_exact_rate_BDF2_SAV.edp**
This file also corresponds to Example 4.1 in the paper. Uses the PCSAV scheme with an exact solution for convergence rate testing.

- **Example4.3_test_BDF2_NSPROSAV_Simple_annihilation_of_singularities.edp**
This file corresponds to Example 4.3 in the paper. It performs a numerical simulation demonstrating the annihilation of singularities in the director field using the PCSAV-ECT scheme.

- **Other scripts / notes**
Additional numerical experiments reported in the paper can be reproduced by modifying the initial conditions and parameters in the above files. Each script contains a header section where mesh resolution, time step, physical parameters, and initial data are specified.

## 🧩 How to Run
Each .edp file is self-contained. Run from the command line:
FreeFem++ Example4.1_test_exact_rate_BDF2_NSPROSAV.edp

## 🧩 Parameter settings (where to change)
Open the .edp file and edit the parameter block near the top. Common parameters:
# Domain parameters
real H    = 1.;     # width of channel (y-direction)
real L    = 1.;     # length of channel (x-direction)

# spatial mesh size (example formula)
Ny = 200   # Number of mesh divisions in the y-direction (channel width)
Nx = 200   # Number of mesh divisions in the x-direction (channel length)

# time step 
dt = 0.005

# final time
Tf = 0.1

# physical parameters
nu = 0.001         # viscosity
lambda = 1.0       # elastic constant
M = 1.0            # relaxation time constant
eta = 0.05         # penalty parameter

# initial condition selector or definition:
- ## func dirXinitial , dirYinitial , uXinitial , uYinitial , pinitial  #depends on the test case



