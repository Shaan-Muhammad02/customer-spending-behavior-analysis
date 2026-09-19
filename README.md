# Customer Spending Behavior Analysis

## Project Overview

Customer spending behavior was analyzed in an e-commerce and retail environment using the **Retail Analysis Large Dataset** from Kaggle.

The goal of the analysis was to determine what factors influence customer spending and whether spending patterns could be better explained by demographic variables, such as age and income, or by behavioral variables such as purchase frequency, transaction value, product preferences, and customer ratings.

The project included data cleaning, exploratory data analysis, regression modeling, classification modeling, and customer segmentation using **K-Means clustering**.

After the supervised learning models showed limited predictive performance, customer segmentation was explored to identify more meaningful behavior-based customer groups.

## Business Problem

Retail businesses often rely on demographic information such as age and income when analyzing or targeting customers.

However, demographic characteristics alone may not fully explain how customers actually behave.

In this analysis, customer spending patterns were examined to determine whether purchasing behavior and customer satisfaction provided more useful information than demographic variables alone.

The analysis was designed to support areas such as customer segmentation, retention strategies, targeted promotions, upselling opportunities, and customer satisfaction improvement.

## Dataset

The project uses the **Retail Analysis Large Dataset** from Kaggle.

The dataset contains more than **300,000 transaction records** and approximately **30 variables** related to:

- Customer demographics
- Transaction details
- Product categories
- Product brands
- Customer locations
- Purchase behavior
- Customer feedback
- Customer ratings

**Target Variable:** `Total_Amount`

The full dataset is not stored in this repository because of its size.

To reproduce the analysis, the dataset can be downloaded from Kaggle and the file `new_retail_data.csv` can be placed inside the `data/` folder.

## Methodology

### 1. Data Cleaning and Preparation

The dataset was prepared before analysis and modeling.

The following steps were completed:

- Irrelevant personal identifier columns were removed
- Records with missing key identifiers were removed
- Missing numerical values were handled using median imputation
- Duplicate records were removed
- Categorical variables were encoded
- Numerical variables were scaled where required
- Training and testing datasets were prepared

### 2. Exploratory Data Analysis

Exploratory data analysis was performed to understand customer spending patterns across different variables and customer groups.

The analysis examined relationships involving:

- Age
- Income
- Customer groups
- Product categories
- Transaction behavior
- Purchase frequency
- Customer ratings
- Spending levels

Considerable overlap was observed between demographic groups.

This suggested that demographic characteristics such as age and income alone were not strong indicators of customer spending behavior.

## Regression Modeling

Customer spending was first analyzed as a continuous prediction problem.

Two regression models were tested:

- **Linear Regression**
- **Random Forest Regressor**

The models achieved an **R² of approximately 0.42**.

This indicated that the available variables explained only part of the variation in customer spending.

The results suggested that additional behavioral relationships or other factors may be required to explain spending more effectively.

## Classification Modeling

Customer spending was then divided into three spending categories:

- **Low Spender**
- **Medium Spender**
- **High Spender**

Two classification models were tested:

- **Logistic Regression**
- **Random Forest Classifier**

The classification approach provided another way to examine spending behavior.

However, the models still had difficulty clearly separating some customer groups, particularly medium spenders.

This suggested that predefined spending categories did not fully capture the underlying structure of customer behavior.

## Customer Segmentation with K-Means

Because the supervised learning models showed limited predictive performance, the analysis was shifted toward **unsupervised customer segmentation**.

K-Means clustering was applied using customer and behavioral features such as:

- `Total_Amount`
- `Total_Purchases`
- `Ratings`
- `Age`

The **Elbow Method** was used to determine an appropriate number of clusters.

The analysis suggested using **8 customer clusters**.

These clusters provided a more useful way to identify different customer behavior patterns and interpret them from a business perspective.

## Key Findings

Several important findings were identified:

- Demographic variables such as age and income were weak predictors of customer spending
- Behavioral variables provided more useful information about customer differences
- Regression models had limited ability to explain overall spending behavior
- Classification models also struggled to clearly distinguish some spending groups
- K-Means clustering produced more meaningful customer segments
- High spending did not always correspond with high customer satisfaction
- Loyal high-spending customers represented important retention opportunities
- Satisfied lower-spending customers represented potential upselling opportunities

## Business Recommendations

Based on the analysis, several business strategies can be considered:

1. Behavior-based segmentation can be used instead of relying primarily on demographic characteristics.
2. Loyal and high-value customers can be prioritized through retention programs, rewards, and personalized offers.
3. Dissatisfied high-spending customers should be investigated because losing these customers may have a larger financial impact.
4. Satisfied lower-spending customers may be targeted through personalized promotions and upselling strategies.
5. Low-spending and low-satisfaction customers may be re-engaged through targeted campaigns and improved customer experiences.
6. Customer purchasing behavior and satisfaction can be considered together when developing marketing and retention strategies.

## Repository Structure

```text
customer-spending-behavior-analysis/
│
├── data/
│   └── README.md
│
├── docs/
│   ├── Business Analytics Final Project.pptx
│   └── Business_Analytics_Final_Report.docx
│
├── notebooks/
│   └── customer_spending_behavior_analysis.ipynb
│
├── .gitignore
├── README.md
└── requirements.txt
```
