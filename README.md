# Healthcare Claims Frequency–Severity Modeling

## Overview
This repository contains an actuarial-style healthcare analytics project that models **medical claim frequency and severity** using real-world **CMS Medicare inpatient data**. The project applies classical statistical modeling techniques to estimate **expected losses (pure premiums)** and is structured as a **trainee-ready Agile project** with clear epics, sprints, and deliverables.

The goal is to demonstrate how separating claim frequency and claim severity leads to more accurate risk estimation than aggregate averages, while also providing a realistic learning framework for junior analysts.



## Business Context
Healthcare insurers must accurately estimate expected medical costs to:
- Set appropriate premiums
- Allocate reserves efficiently
- Identify high-risk services and regions
- Support utilization management decisions

Traditional average-based approaches obscure risk heterogeneity. This project implements a **frequency–severity framework**, the industry standard in actuarial science, to address these limitations.



## Data Source
The analysis uses the **2023 Medicare Inpatient Hospitals by Provider and Service** dataset published by the Centers for Medicare & Medicaid Services (CMS).

Each observation represents a **Hospital × Diagnosis-Related Group (DRG)** combination.

Key variables include:
- `discharges`: Total inpatient discharges (claim frequency proxy)
- `avg_covered_charges`: Average submitted covered charges (claim severity)
- `state`: Provider state
- `drg`: Diagnosis-Related Group description

To ensure computational stability, the analysis focuses on **high-volume DRGs**, a standard dimensionality-reduction practice in healthcare analytics.



## Analytical Framework

### 1. Exploratory Data Analysis (EDA)
- Distribution analysis of claim frequency and severity
- Overdispersion testing for count data
- Assessment of skewness and tail behavior in costs
- Validation of frequency–severity separation

### 2. Claim Frequency Modeling
- **Poisson regression** (baseline)
- Formal overdispersion diagnostics
- **Negative Binomial regression** (final model)
- Model comparison using likelihood-based metrics

### 3. Claim Severity Modeling
- **Gamma Generalized Linear Model (GLM)** with log link
- Interpretation of multiplicative cost effects
- Model adequacy and dispersion assessment

### 4. Pure Premium Estimation
Expected loss is computed as:

\[
\text{Pure Premium} = \mathbb{E}(\text{Frequency}) \times \mathbb{E}(\text{Severity})
\]

This provides a decision-ready estimate of expected healthcare costs per hospital–DRG combination.



## Agile Project Structure

### Sprints
- **Sprint 1:** Data preparation, EDA, and model development
- **Sprint 2:** Model integration, pure premium estimation, and reporting

### Epics
1. Data Preparation & Exploration  
2. Frequency & Severity Modeling  
3. Reporting & Business Insights  

Tasks are distributed across two trainee groups to simulate real-world collaborative analytics workflows.




## Tools & Technologies
- Python
- pandas, numpy
- statsmodels (GLM)
- matplotlib
- Google Colab (execution environment)



## Key Outputs
- Negative Binomial frequency model
- Gamma severity model
- Expected loss (pure premium) estimates
- Risk ranking of DRGs and states
- Report-ready tables and visualizations



## Learning Objectives (For Trainees)
By completing this project, trainees will learn how to:
- Work with real-world healthcare claims data
- Validate statistical modeling assumptions
- Apply frequency–severity modeling correctly
- Interpret model outputs in business terms
- Deliver decision-ready analytics using Agile workflows



## Disclaimer
This project uses publicly available CMS data for educational and analytical purposes only. Results do not represent official pricing recommendations.



Joshua  
Healthcare & Risk Analytics



