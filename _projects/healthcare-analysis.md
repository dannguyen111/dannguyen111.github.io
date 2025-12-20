---
layout: project
title: "Healthcare Access Disparities Analysis"
description: "A quantitative research project analyzing healthcare inequity in Pennsylvania using mathematical modeling and regression analysis."
image: "assets/images/healthcare-paper-thumbnail.png"
date: 2024-05-01
---

## Project Overview
For my **Applied Research in Math** capstone, I worked on a challenge prompt provided by **Deloitte** to quantify inequities in healthcare access.

The study investigated the distribution of medical resources across Pennsylvania counties. Unlike standard analyses that look only at provider-to-population ratios, this project utilized advanced economic inequality metrics to measure the *fairness* of distribution relative to socio-economic factors.

## Methodology

### 1. Inequality Indices
We adapted economic models to measure healthcare accessibility:
- **Modified Gini Coefficient:** Calculated to assess the distribution of resources (e.g., hospital beds, physicians) relative to income inequality.
- **Atkinson Index:** Used to quantify the "social welfare loss" caused by inequality, incorporating a parameter ($\epsilon$) for societal aversion to inequality.
- **Weighted Utilitarian Function:** Applied to evaluate overall societal well-being, assigning higher weights to lower-income quintiles to prioritize the most vulnerable populations.

### 2. Statistical Analysis
We conducted **Multiple Regression Analysis** to identify the drivers of inequity.
- **Predictors:** Rural-Urban Continuum Codes (RUCC), median household income, and uninsured rates.
- **Target Variable:** Density of mental health providers per 1000 residents.

## Key Findings

### 1. The Mental Health Gap
Our analysis revealed that **Mental Health Providers** had the highest inequity scores of all indicators tested.
- **Gini Coefficient:** 0.185 (favoring wealthier counties).
- **Atkinson Index:** 0.4399 (indicating a massive potential welfare gain if resources were redistributed).
- **Conclusion:** While physical infrastructure (hospitals) favored lower-income areas slightly, mental health services were disproportionately concentrated in wealthy, urban centers.

### 2. Impact on Outcomes
We found a statistically significant **negative correlation** between the density of mental health providers and suicide rates in rural Pennsylvania. This quantified the real-world cost of the identified access gaps.

### 3. Socio-Economic Drivers
Our regression model accounted for **62.2% of the variance** in provider availability. It confirmed that **rural status** and **lack of insurance** are significant negative predictors for mental health access, independent of income.

## Tools Used
* **Languages:** Python (Pandas, Scikit-Learn, Matplotlib)
* **Math:** Econometrics, Social Welfare Functions, Linear Regression
* **Output:** [Read the Full Paper](/assets/pdfs/Completed-Study-Paper.pdf)