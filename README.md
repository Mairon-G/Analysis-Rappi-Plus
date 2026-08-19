# 📊 RappiPlus Business & Customer Behavior Analysis

## Overview

This project evaluates the performance of **RappiPlus** to support **data-driven business decisions**.

The analysis combines transactional, product, marketing, user behavior, retention, and A/B testing data to understand business profitability, customer behavior, conversion performance, and opportunities for optimization.

The project follows a progressive analytical approach:

- 🔍 Data quality assessment and cleaning
- 💰 Revenue, cost, and profitability analysis
- 🛒 Conversion funnel analysis
- 🔁 Customer retention and cohort analysis
- 🧪 Statistical validation through A/B testing
- 📊 Business intelligence dashboard preparation

## Objectives

- Assess and improve **data quality**
- Analyze **revenue, costs, and profitability**
- Understand customer behavior throughout the purchase funnel
- Identify conversion bottlenecks
- Measure customer retention through cohort analysis
- Evaluate the impact of checkout UI changes
- Generate actionable **business recommendations**

## Tools Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SQL / SQLAlchemy**
- **Statsmodels**
- **Power BI / Tableau**

## Datasets

The analysis works with several business datasets:

- `rappiplus_orders_raw.csv` — orders, prices, discounts, products, and revenue
- `rappiplus_catalog.csv` — product costs, categories, and suppliers
- `rappiplus_marketing_spend.csv` — marketing investment by channel and country
- `events` — user events throughout the platform
- `users` — user registration information
- `user_activity` — user activity and retention data
- `experiment_checkout_ui.csv` — checkout UI A/B experiment results

## Analysis Highlights

### Data Cleaning

The data quality process included:

- Converted date fields to the appropriate datetime format
- Identified and removed invalid negative quantities and transaction amounts
- Handled missing numerical values
- Reconstructed missing `cantidad` or `precio_unitario` values when sufficient information was available
- Removed duplicate records
- Validated duplicated order IDs
- Filled missing categorical values with appropriate generic labels
- Removed records missing essential product information
- Exported cleaned datasets for subsequent analysis

The orders dataset initially contained **25,100 records**, including missing values and anomalous numerical observations. Four records contained negative quantities and negative total amounts, while 100 exact duplicate rows were identified and removed.

### Profitability Analysis

The business was evaluated using revenue, product costs, and marketing investment.

Key results:

- **Total Revenue:** $51,954,718.94
- **Product Costs:** $43,124,069.01
- **Marketing Investment:** $2,871,843.53
- **Combined Costs:** $45,995,912.54
- **Net Profit:** $5,958,806.40
- **Profit Margin:** 11.47%

The analysis shows that RappiPlus is profitable during the analyzed period.

### Sales & Marketing Analysis

The analysis examined transaction metrics, product performance, and marketing investment by channel.

Key findings:

- **Average Order Value:** $2,085.20
- **Average Products per Order:** 7.12 units
- **Best-Selling Product:** `Laptop-Gaming-16GB`
- **Units Sold:** 144,198
- **Marketing Spend:** concentrated relatively evenly across Social, Organic, and Paid Search

Marketing investment was distributed as follows:

- **Social:** $918,043.21
- **Organic:** $913,533.01
- **Paid Search:** $863,088.21
- **Other:** $177,179.10

### Conversion Funnel Analysis

The customer journey was analyzed using platform events, from the first visit through completed purchase.

The funnel included:

1. `first_visit`
2. `select_item`
3. `add_to_cart`
4. `begin_checkout`
5. `add_payment_info`
6. `purchase`

The final observed conversion rate was **80.04%**, with 7,796 users at the initial stage and 6,240 users reaching purchase.

The main conversion bottleneck was identified at the **`add_payment_info`** stage, where conversion from the previous step fell to **86.71%**.

### Customer Retention & Cohort Analysis

Customer retention was evaluated by grouping users according to their registration month and measuring weekly activity.

The analysis measured:

- Week 1 retention
- Week 2 retention
- Week 3 retention

Retention remained relatively stable across the analyzed monthly cohorts, generally ranging around **41%–43% in Week 1**.

For example, the January 2025 cohort showed:

- **Week 1:** 42.84%
- **Week 2:** 41.06%
- **Week 3:** 40.32%

The results indicate a significant initial drop after registration, followed by comparatively stable engagement among users who remain active.

### A/B Testing

An A/B test was performed to evaluate whether a new checkout interface improved purchase conversion.

The experiment compared:

- **Control:** 15.69% conversion
- **Treatment:** 16.29% conversion
- **p-value:** 0.41606
- **Significance level:** α = 0.05

Because the p-value is greater than 0.05, the difference between the two groups was **not statistically significant**.

Therefore, the analysis does not provide sufficient evidence that the new checkout UI improves conversion.

## Key Findings

- RappiPlus generated **$51.95M in revenue** and **$5.96M in net profit**.
- The business achieved an **11.47% profit margin**.
- The **Laptop-Gaming-16GB** was the dominant product, with 144,198 units sold.
- Electronics was the strongest product category in terms of profitability.
- Marketing investment was relatively balanced across Social, Organic, and Paid Search.
- The purchase funnel shows a strong overall conversion rate, but **payment information** represents the main friction point.
- Customer retention drops substantially during the first week but becomes comparatively stable afterward.
- The checkout UI experiment did **not** produce a statistically significant improvement in conversion.
- The business has a high dependence on the Laptop-Gaming-16GB and the Electronics category.

## Business Recommendations

- **Optimize the payment process:** Investigate payment failures, simplify required checkout fields, and evaluate additional fast-payment options.
- **Focus on checkout functionality rather than visual changes:** The A/B test did not demonstrate a significant benefit from the new UI.
- **Diversify the product portfolio:** Promote complementary products from Home and Fashion alongside Electronics purchases.
- **Use cross-selling strategies:** Leverage the high traffic and sales volume of the leading laptop product to increase purchases from secondary categories.
- **Monitor customer retention:** Focus acquisition and onboarding strategies on reducing the significant drop during the first week.
- **Optimize marketing investment:** Continue monitoring channel performance and connect marketing spend with revenue and conversion outcomes.
- **Improve supplier negotiations:** Product costs represent the largest component of total costs, creating an opportunity to improve margins through volume negotiations and cost optimization.

## Dashboard

The project includes a business intelligence dashboard designed to communicate:

- Revenue
- Profit
- Marketing spend
- Average order value
- Average products per order
- Revenue and profit by product or category
- Detailed order-level information

Dashboard:

https://drive.google.com/drive/folders/1KzFH62D8OwzSksDPSoW5MAVTb7VJcaoZ?usp=drive_link

## Open notebook in Colab:
https://colab.research.google.com/drive/1-xI3PcTAW0aDvMGJ5_n4M92RkGibqGlu?usp=sharing

## Repository Structure

```text
├── Analysis Rappi Plus.ipynb
├── data/
│   ├── rappiplus_orders_raw.csv
│   ├── rappiplus_catalog.csv
│   ├── rappiplus_marketing_spend.csv
│   └── experiment_checkout_ui.csv
├── output/
│   ├── orders_clean.csv
│   ├── catalog_clean.csv
│   └── marketing_clean.csv
└── README.md



Author

Data Analytics project focused on business performance, customer behavior, conversion analysis, retention, A/B testing, and business intelligence within the RappiPlus e-commerce ecosystem.
