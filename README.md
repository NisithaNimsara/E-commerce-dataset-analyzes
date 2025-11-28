# E-commerce-dataset-analyzes
This project analyzes a dataset of 2000 e-commerce transactions to study customer purchase behavior. It includes demographics, site engagement, purchase history, transaction details, and promotion usage, helping the company refine marketing strategies and optimize website design for better customer experience.
# E-commerce Dataset Analysis

This repository contains coursework for **Computational Mathematics**, focused on analysing an e-commerce customer purchases dataset using **R**.  
The main goal is to understand customer spending behaviour and explore how factors like time spent on the site and previous purchases relate to purchase amounts.

---

## Project Structure

```text
.
├── 2506755_20240281_Nisitha Nimsara.pdf   # Rendered coursework report
├── README.md                              # Project overview (this file)
└── MathsCourseWork/
    ├── Computational Mathematics.Rmd      # Main R Markdown analysis
    ├── MathsCourseWork.Rproj             # RStudio project file
    └── customer_purchases.csv            # E-commerce dataset
```
## Dataset
File: customer_purchases.csv
Rows: 2,000 e-commerce transactions

Key columns:
- customer_id – Unique ID for each customer
- purchase_amount – Amount spent in a single transaction (in USD)
- time_spent_on_site – Time spent on the website (in minutes)
- region – Customer’s region (e.g. North, East, South, West)
- number_of_previous_purchases – How many times the customer purchased before
- used_discount – Whether the customer used a discount (0 = No, 1 = Yes)

## Analysis Overview

All analysis is done in R via Computational Mathematics.Rmd.
The main steps include:

# Data loading & setup
- Importing customer_purchases.csv
- Using the tidyverse ecosystem for data manipulation and plotting

#Exploratory Data Analysis (EDA)
- Summary statistics for all numerical variables (summary(df))
- Histograms of key variables (e.g. purchase_amount, time_spent_on_site)
- Boxplots to identify potential outliers
- Basic interpretation of central tendency and spread

# Distribution analysis
- Visual inspection of the distribution of purchase_amount
- Discussion of whether a normal distribution is a reasonable model for spending behaviour

# Predictive modelling
- Simple linear regression:
```
model <- lm(purchase_amount ~ time_spent_on_site, data = df)
```
- Visualising the relationship (scatter plot + regression line)
- Fitted equation (approx.):
```
\text{purchase_amount} \approx 73.50 + 0.12 \times \text{time_spent_on_site}
```
- Example prediction for a customer who spends 12 minutes on the site

# Interpretation
- Discussion of what the model suggests about the relationship between time on site and spending
- Comment on how strong/weak the relationship is and possible limitations
