# Project 1: Motor Insurance Pricing and Risk Modeling

## Overview

This project explores motor insurance claim frequency modeling using a real-world insurance portfolio dataset.

The objective is to study how policyholder, vehicle, and geographic characteristics influence insurance risk and expected claim frequency.

The project follows a pricing-oriented actuarial workflow:

1. Understand the dataset structure
2. Perform exploratory data analysis (EDA)
3. Clean and prepare insurance exposure data
4. Model claim frequency using a Poisson Generalized Linear Model (GLM)
5. Interpret rating factors and risk segmentation
6. Estimate scenario-based premiums
7. Prepare the project for future severity and pure premium modeling


## Business Context

In property and casualty insurance, insurers must estimate the expected future cost of each policy.

A simplified pricing framework is:

Pure Premium = Claim Frequency × Claim Severity

Where:

- Claim Frequency measures how often claims occur
- Claim Severity measures how costly those claims are

This notebook focuses primarily on the frequency component because the current dataset contains:

- policy exposure
- claim counts
- driver characteristics
- vehicle characteristics
- regional information

but does not yet include detailed claim amount severity information.

---

## Dataset Description

The dataset contains motor insurance policy records.

Each row represents a single insurance policy.

Key variables include:

| Variable | Description |
|---|---|
| ClaimNb | Number of claims |
| Exposure | Policy exposure duration |
| DrivAge | Driver age |
| VehAge | Vehicle age |
| VehPower | Vehicle power category |
| BonusMalus | Risk/bonus score |
| Area | Area category |
| Region | Geographic region |
| Density | Population density |
| VehGas | Fuel type |
| VehBrand | Vehicle brand category |

---

## Modeling Objective

The primary modeling objective is to estimate expected claim frequency using a Poisson GLM with exposure adjustment.

The project also aims to:

- identify major insurance risk drivers
- understand relationships between rating variables and claims
- create interpretable risk segmentation
- simulate pricing-oriented outputs
- build a foundation for future severity and pure premium modeling

---

## Statistical Background

Insurance claim counts are discrete count outcomes:

0, 1, 2, 3, ...

Most policyholders generate no claims, while a smaller number generate one or more claims.

Because of this structure, Poisson regression is commonly used as a baseline actuarial frequency model.

Exposure is included as a log offset so the model estimates claim frequency rather than raw claim count.

---

## Future Extensions

Planned future extensions include:

- Severity modeling using Gamma GLMs
- Pure premium modeling
- Tweedie GLMs
- XGBoost comparison models
- Train/test validation
- Advanced residual diagnostics
- Dashboard visualization

---

## Technical Stack

- Python
- Pandas
- NumPy
- Statsmodels
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## References and Study Sources

This project is conceptually aligned with:

- CAS Exam 5: Basic Ratemaking
- SOA SRM / CAS MAS-I GLM concepts
- Generalized Linear Models for Insurance Rating (CAS Monograph)
- Basic Ratemaking by Werner and Modlin

---