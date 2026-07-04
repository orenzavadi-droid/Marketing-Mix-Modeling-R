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
* `Sales` (Target Variable): Sales of the product (in thousands of units).

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

## 📊 Key Findings & Statistical Outputs

### 1. Correlation Insights
* **TV & Sales:** Strong positive correlation (**0.78**), indicating it is the primary volume driver for the business.
* **Radio & Sales:** Moderate-to-strong positive correlation (**0.58**).
* **Newspaper & Sales:** Very weak correlation (**0.23**), signaling potential advertising inefficiency.

### 2. Multiple Linear Regression Model Results
The trained OLS regression model yielded an exceptional fit, capturing **89.72%** of the variance in sales:
* **Multiple R-squared:** 0.8972
* **Adjusted R-squared:** 0.8956
* **F-statistic:** 570.3 ($p$-value < 2.2e-16)

#### Model Coefficients & Coefficients Table:
| Variable | Estimate (Weight) | Std. Error | t value | Pr(>\|t\|) | Significance |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **(Intercept)** | 2.9389 | 0.3119 | 9.422 | < 2e-16 | `***` (Highly Significant) |
| **TV** | 0.0458 | 0.0014 | 32.809 | < 2e-16 | `***` (Highly Significant) |
| **Radio** | 0.1885 | 0.0086 | 21.893 | < 2e-16 | `***` (Highly Significant) |
| **Newspaper** | -0.0010 | 0.0059 | -0.177 | 0.8600 | (Not Significant) |

### 📈 The Predictive Marketing Equation
Based on the empirical outputs, the optimization formula for future sales prediction is:
$$\text{Sales} = 2.94 + 0.046 \times \text{TV} + 0.189 \times \text{Radio} - 0.001 \times \text{Newspaper}$$

---

## 🚀 Strategic Recommendations for Marketing Leadership
1. **Eliminate Newspaper Spend (Stop Ad Waste):** With a coefficient near zero ($-0.001$) and a non-significant $p$-value ($0.86$), spending on newspapers does not drive sales. This budget should be cut immediately.
2. **Capitalize on Radio Effectiveness (High ROI):** Every \$1,000 invested in Radio yields **188.5 additional units sold**—nearly 4x the marginal impact of TV (\$0.046). Reallocating the discarded newspaper budget directly into Radio will maximize immediate ROI.
3. **Maintain TV for Volume Scaling:** While Radio provides higher efficiency per dollar, TV remains crucial due to its scale, acting as the bedrock of overall transactional volume.

## 🛠️ Tools & Packages Used
* **Language:** R
* **Environment:** RStudio
* **Key Packages:** `tidyverse`, `ggplot2`, `corrplot`
