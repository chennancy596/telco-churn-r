# Telco Customer Churn Analysis in R

An end-to-end analysis of customer churn for a telecom company: data cleaning, visualization, logistic regression and random forest modelling, ending with retention recommendations.

**Full report:** [View the HTML report](https://chennancy596.github.io/telco-churn-r/churn_analysis.html)

## Business Question

About a quarter of the 7,032 customers in this dataset (26.6%) left the company in the last month. Which customers are most likely to leave, what is associated with churn, and how should the company target its retention budget?

## Key Findings

- **Contract type:** month-to-month customers churn at 42.7%, compared with 2.8% for two-year contracts.
- **Tenure:** customers in their first year churn at 47.7%, the highest of any tenure group.
- **Payment method:** customers paying by electronic check churn at 45.3%, versus about 15–17% for automatic payments.
- **Model:** lowering the classification threshold from 0.5 to 0.3 raises the random forest's recall from 0.49 to 0.78, so the retention team catches far more churners at the cost of more false alarms.

## Recommendations

1. Offer annual-contract discounts to month-to-month customers in their first 12 months.
2. Strengthen onboarding during the first year, when churn is highest.
3. Encourage customers to switch from electronic checks to automatic payment.
4. Use the random forest with a 0.3 threshold to build a monthly retention list.

## Methods

- Data cleaning and exploration with `tidyverse`
- Visualization with `ggplot2`
- Logistic regression (odds ratios) with `glm` and `broom`
- Random forest with `ranger`
- Model comparison on a 30% hold-out set using accuracy, recall and precision
- Report written in Quarto

## Files

| File | Description |
|---|---|
| `churn_analysis.qmd` | Source code and analysis (Quarto) |
| `churn_analysis.html` | Rendered report |

## Data

IBM Telco Customer Churn sample dataset (7,043 customers, 21 variables). The report downloads it automatically from IBM's public GitHub repository; 11 new customers with no recorded total charges were removed, leaving 7,032.

## How to Reproduce

1. Install R, RStudio and the packages `tidyverse`, `broom`, `ranger`, `rmarkdown` and `knitr`.
2. Open `churn_analysis.qmd` in RStudio and click **Render**.

## Author

Nanxi Chen
