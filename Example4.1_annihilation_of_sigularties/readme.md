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
Detailed descriptions of the Example4.1_annihilation_of_sigularties file :
- **Example4.3_test_BDF2_NSPROSAV_Simple_annihilation_of_singularities.edp**
This file corresponds to Example 4.3 in the paper. It performs a numerical simulation demonstrating the annihilation of singularities in the director field using the PCSAV-ECT scheme.

## 🧩 How to Run
Each .edp file is self-contained. Run from the command line:
FreeFem++ Example4.3_test_BDF2_NSPROSAV_Simple_annihilation_of_singularities.edp

## 🧩 Parameter settings (where to change)
Open the .edp file and edit the parameter block near the top. Common parameters:
# Domain parameters
real H    = 2.;     # width of channel (y-direction)
real L    = 2.;     # length of channel (x-direction)

# spatial mesh size (example formula)
Ny = 32   # Number of mesh divisions in the y-direction (channel width)
Nx = 32   # Number of mesh divisions in the x-direction (channel length)

# time step 
dt = 0.0005

# final time
Tf = 1.0

# physical parameters
nu = 1.0         # viscosity
lambda = 0.01       # elastic constant
M = 1.0            # relaxation time constant
eta = 0.05         # penalty parameter

