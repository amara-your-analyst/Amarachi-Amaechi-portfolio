# Weekly Marketplace KPI Dashboard (Olist Data)

A sample dashboard tracking four weekly metrics for an order-based business:
fulfilled order value, repeat buyers, supplier participation and delivery performance.
It is a template for businesses like fresh-produce group-buy platforms.
The data is public and Brazilian, not from any client.

**Live dashboard:** https://datastudio.google.com/reporting/f455263d-6a65-4ebc-924f-37d337a662f7

![Dashboard] (WEEKLY PERFORMANCE DASHBOARD.pdf)

## Problem
Order-based businesses need a weekly view of sales, customer loyalty, supplier activity and delivery reliability.

## Data
Olist Brazilian E-Commerce Public Dataset (Kaggle), about 99,000 orders, Jan 2017 to Aug 2018.
Source: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce


## Method
1. Loaded orders, customers, items and payments tables.
2. Joined them and assigned each order to a week.
3. Calculated four metrics by week.
4. Validated results (see below).
5. Built the dashboard in Looker Studio.

## Metric definitions
- **Fulfilled order value:** total payment value of delivered orders in the week.
- **Repeat buyer rate:** share of the week's buyers whose first order was in an earlier week.
- **Active sellers:** sellers with at least one delivered order in the week.
- **On-time delivery rate:** delivered orders arriving on or before the estimated date.

## Validation
- Order and delivered-order counts matched published totals for the dataset.
- Weekly totals matched the raw data.
- All percentages stayed between 0 and 100.

## Findings

- Across the 86 weeks analysed, the platform recorded about R$15.36 million in fulfilled order value.
- Of 98,962 orders placed in the window, 96,095 were delivered, a fulfilment rate of about 97%.
- Repeat purchases are rare in this dataset: the average weekly repeat buyer rate was about 2%, so most customers ordered once.
- On-time delivery averaged about 93% across the weeks analysed.
  
## Next steps
With real order data, I would add demand forecasting and buyer and supplier scoring.

## Tools
Python (pandas), Kaggle Notebooks, Looker Studio
