# Marketing-Mix-Modeling-R
A marketing analytics project in R using Linear Regression to evaluate advertising channel performance (TV, Radio, Newspaper) and optimize budget allocation for maximum sales ROI.


# Marketing Mix Modeling & Budget Optimization (R)

## 📌 Project Overview
This project applies statistical modeling and machine learning in R to analyze the impact of different advertising channels on product sales. Using a dataset tracking spending across TV, Radio, and Newspaper mediums, this analysis builds a predictive Linear Regression model to determine marketing ROI and provide data-driven recommendations for future budget allocation.

## 🗂️ Dataset Structure
The analysis utilizes the `Advertising.csv` dataset (~200 records), which contains the following key metrics:
* `TV`: Advertising budget spent on TV (in thousands of dollars).
* `Radio`: Advertising budget spent on Radio (in thousands of dollars).
* `Newspaper`: Advertising budget spent on Newspaper (in thousands of dollars).
* `Sales` (Target Variable): Sales of the product (in thousands of units or millions of dollars).

---

## 🔍 Analytical Goals & R Workflow

### 1. Exploratory Data Analysis (EDA) & Correlation Analysis
* **Objective:** Understand the distribution of spending and identify which marketing channel has the strongest statistical relationship with sales.
* **Method:** Visualizing relationships using correlation matrices and scatter plots (`ggplot2`).

### 2. Linear Regression Modeling (Marketing Mix Model)
* **Objective:** Quantify the exact impact of every dollar spent on each channel and build a predictive formula for revenue.
* **Method:** Training a Multiple Linear Regression model (`lm()`) to assess coefficients, R-squared values, and statistical significance ($p$-values).

### 3. Budget Optimization & ROI Evaluation
* **Objective:** Identify low-performing channels (ad waste) and reallocate resources to high-performing vectors to maximize total Sales.

---

## 🛠️ Tools & Packages Used
* **Language:** R
* **Environment:** RStudio
* **Key Packages:** `tidyverse`, `ggplot2`, `corrplot`, `caret`

---

## 📈 Key Findings & Strategic Insights
*(This section will be dynamically updated with our statistical outputs, coefficients, and visualizations as the analysis progresses).*
