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
Detailed descriptions of the main folders :
- **Example4.1_exact_rate_test**
This folder corresponds to *Example 4.1* in the paper.  
  It contains FreeFem++ scripts that use both the **PCSAV-ECT** and **PCSAV** schemes with a constructed exact solution to verify the **temporal convergence rate** of the proposed method.  
  - `Example4.1_test_exact_rate_BDF2_NSPROSAV.edp`:  
    Uses the PCSAV-ECT scheme for convergence rate testing.
  - `Example4.1_test_exact_rate_BDF2_SAV.edp`:  
    Uses the PCSAV scheme for convergence rate testing.
    
- **Example4.3_annihilation_of_singularities/**
  This folder corresponds to *Example 4.3* in the paper.  
  It contains the FreeFem++ script:
  - `Example4.3_test_BDF2_NSPROSAV_Simple_annihilation_of_singularities.edp`:  
    Performs a numerical simulation demonstrating the **annihilation of singularities** in the director field using the PCSAV-ECT scheme.

- **Other numerical tests**
  Additional experiments discussed in the paper can be reproduced by modifying the **initial conditions** and **parameters** in the above `.edp` scripts.  
  Each script includes a clearly marked parameter section specifying the **mesh resolution**, **time step**, **physical parameters**, and **initial data**.



