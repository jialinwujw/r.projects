# About The Analysis
Survival analysis is used to analyze time-to-event data and to identify factors that contribute to the occurrence of events of interest. It is used in a wide range of fields, including medical research, economics, engineering, and social sciences, to make informed decisions based on the analysis of such data.

## Project

[R code HTML version](https://htmlpreview.github.io/?https://github.com/jialinwujw/sharing_projects/blob/main/mi_survival_analysis/mi_survival_analysis.html)

### Data
The data set available from the R Package (smoothHR), including 500 observations with 22 variables.
For my analysis, I created two response variables: 
* Survival Time (Date of Last Follow-Up - Hospital Admission Date)
* Censoring Status (Death Within 1 Year After Hospitalization)

### Discription
A group of researchers in the Department of Cardiology at the University of Massachusetts Medical School has collected data from 500 myocardial infarction (MI) patients from 1975 to 2001 in Worcester, Massachusetts. This project aims to identify factors associated with survival rate after hospitalization for acute MI.

Myocardial Infarction (MI) = Heart Attack

### R Packages
```sh
library(dplyr)
library(tidyr)
library(ggplot2)
library(survival)
library(survminer)
library(ggfortify) # Hazard ratio table and plot
library(pROC) # ROC curve

library(smoothHR) # Data
```

### Outputs
Assess which covariates are the most strongly associated with the outcome, and then implement interventions to increase survival rates:
* **Cox Regression (Survival Time)**
  - Estimate the hazard ratio
  - Make predictions about survival probabilities for new individuals
* **Logistic Regression (Censor)**
  - Identify all patients who are at risk of death
