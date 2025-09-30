## Gadget Sales Analysis – Advertising Impact
---

📌 Project Overview

This project explores how advertising expenditure per person influences gadget sales across cities.
Using R we cleaned a raw dataset of 1 000 + records, engineered new variables, removed outliers, transformed skewed data, and built a simple linear regression model to quantify the relationship between advertising spend and sales percentage.

---

🗂 Dataset

Original file: gadget_0.csv (≈ 1 000 rows × 4 columns: name, population, advertising, sales)

Added a row ID column for easier tracking.

Variables include population counts, advertising spend ($) and gadget sales numbers.

---

🛠 Tools & Packages

Language: R

Libraries: tidyverse, dplyr, tidyr, readr, inspectdf, caret, e1071, ggplot2

Visualisations: histograms, scatterplots with linear fit

Box-Cox transformation for normalising skewed data

---

🔑 Key Steps

Data Cleaning & Taming – fixed types, stripped $ signs & commas, converted negatives to positive, handled NAs & duplicates.

Outlier Treatment – used IQR, percentile filters and visual histograms for advertising, population, sales.

Feature Engineering – created:

sales_pct = (sales / population) × 100

adv_exp_pp = (advertising / population)

Sampling & EDA – drew random sample (n = 700) for analysis; produced summary stats & plots.

Box-Cox Transformation – reduced skewness of sales_pct (λ ≈ 0.5) → sales_pct_trans.

Linear Regression – modelled sales_pct_trans ~ adv_exp_pp

Achieved R² ≈ 0.91 indicating strong linear fit.

Model Diagnostics – checked linearity, homoscedasticity, normality & independence assumptions.

Prediction Scenarios – estimated sales % at various advertising-spend levels (e.g. ~$3.14 pp ≈ 25 % expected uptake).

---

📊 Results & Insights

Positive linear relationship: higher ad-spend per person generally increases gadget sales %.

Box-Cox transformation improved normality (skewness ↓ to 0.06).

Extreme low/high ad-spend values may lie outside reliable prediction range.

Recommended focusing on moderate to high ad-spend (~ 3–6 $/person) to achieve higher sales.

---

🚀 How to Run

Clone/download this repo.

Open the R script or R Markdown notebook.

Install required packages listed above.

Place gadget_0.csv in ./data folder.

Knit or run all chunks to reproduce cleaning, EDA, modelling and plots.

---

📂 Project Structure
├── data/               # input CSV
├── scripts/            # R code or Rmd file
├── figures/            # generated histograms & scatterplots
└── README.md

---

📈 Future Work

Compare multiple advertising channels

Extend to multi-variable regression with socio-economic factors

Deploy a Shiny dashboard for interactive insights

---

📜 Author

Md Tauhidul Islam – Master of Data Science, University of Adelaide
