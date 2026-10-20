# Capstone Retail Analytics

## Milestone 1: Problem Framing and Data Acquisition

### Problem Statement

A growing Kenyan retail chain operating across multiple counties needs data-driven intelligence to optimize branch operations, customer retention, promotional efficiency, and inventory planning.

### Business Questions

1. **Customer Behavior:** Who buys what, where, and when across different payment channels (M-Pesa vs. Cash/Card)?
2. **Revenue & Margin Drivers:** Which stores, counties, and product categories generate the highest revenue and gross profit margins?
3. **Customer Retention:** Which customer segments are drifting away (churn risk), and which high-value customers belong in premium loyalty tiers?
4. **External Drivers:** How do macro-economic factors (KNBS CPI/inflation, county population, public holidays) affect purchasing behavior?
5. **Demand Forecasting:** What item-level and store-level demand can be expected next month, to guide inventory replenishment?

### Success Metrics

| Type | Metrics |
|------|---------|
| Financial KPIs | Gross Revenue (KES), Net Revenue (KES), Gross Margin %, Average Basket Value (KES) |
| Customer KPIs | Monthly Active Customers, Customer Lifetime Value (CLV), RFM segment distribution, Churn Rate |
| Operational KPIs | Demand Forecast Accuracy (MAPE < 15%), Promotional Lift % |

### Data Inventory & Provenance Log

The dataset covers 24 full months (1 Jan 2023 to 31 Dec 2024). It combines internal transaction data with official Kenyan context data.

| Table | Description | Rows x Cols | Key Fields | Acquisition Method | License / Terms |
|-------|-------------|-------------|------------|--------------------|-----------------|
| sales_transactions.csv | Transaction line items | 123, 927 x 15 | transaction_id, transaction_date, customer_id, store_id, product_id, quantity, unit_price_kes, gross_sales_kes, discount_amount_kes, net_sales_kes, cogs_kes, gross_profit_kes, payment_method, promo_id | Synthetic, generated | Synthetic data, free to use for this project |
| customers.csv | Customer master directory | 1,200 x 8 | customer_id, customer_name, gender, age, county, signup_date, preferred_payment_method, loyalty_tier | Synthetic, generated | Synthetic data, free to use for this project |
| stores.csv | Retail branch network | 10 x 7 | store_id, store_name, county, sub_county, store_format, sqft, opening_date | Synthetic, generated | Synthetic data, free to use for this project |
| products.csv | FMCG product catalog | 15 x 6 | product_id, product_name, category, sub_category, unit_cost_kes, unit_price_kes | Synthetic, generated | Synthetic data, free to use for this project |
| promotions.csv | Marketing and seasonal promos | 9 x 3 | promo_id, promo_name, discount_pct | Synthetic, generated | Synthetic data, free to use for this project |
| knbs_county_demographics.csv | County demographics | 6 x 5 | county, population_2019, projected_pop_2024, gdp_share_pct, urban_pct | Public KNBS data | KNBS public data terms (check KNBS site) |
| knbs_cpi_inflation.csv | CPI and inflation | 24 x 4 | year_month, knbs_cpi_index, headline_inflation_pct, food_inflation_pct | Public KNBS data | KNBS public data terms (check KNBS site) |
| kenya_public_holidays.csv | Official public holidays | 18 x 3 | holiday_date, holiday_name, is_major_shopping | Public holiday calendar | Public information |
