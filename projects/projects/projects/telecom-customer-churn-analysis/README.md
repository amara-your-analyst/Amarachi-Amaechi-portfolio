# Telco Customer Churn Analysis

## Project purpose

A telecom company is losing about 1 in 4 of its customers. This project answers the questions a business would ask next:

1. How many customers are leaving, and how much revenue does that cost?
2. Which customers are most likely to leave, and why might that be?
3. Can we spot at-risk customers before they go?
4. What should the business do about it?

The aim was not only to run the numbers but to turn them into something a non-technical manager can read and act on, so the project ends with a one-page dashboard and a plain-language report.

![visualizations](telco_churn_summary.png)

## Key findings

- **26.5% of customers have left** (1,869 of 7,043), taking about $139,000 of monthly revenue with them. That is 31% of the total, more than their share of the customer count, because customers who leave pay more on average ($74 a month against $61).
- **Contract type is the biggest factor.** Month-to-month customers leave at 43%, compared with 11% on one-year contracts and 3% on two-year contracts.
- **The first year is the danger period.** 47% of customers in their first 12 months leave, falling to 10% after four years. More than half of all departures happen in the first year.
- **Fiber optic and electronic check stand out.** Fiber customers leave at 42% (DSL: 19%). Electronic check payers leave at 45% (automatic card or bank payers: about 16%).
- **One high-risk group drives much of the loss.** Customers on month-to-month plans with fiber internet who pay by electronic check make up 19% of the base, leave at 60%, and account for 42% of all departures.
- **Customers with tech support or online security leave far less often** (about 15%, against about 42% without).

## Recommendations

Move month-to-month customers onto longer contracts, support customers through their first year, investigate why fiber customers leave, encourage automatic payment, and use the model's risk scores to decide who to contact first. Changes should be tested on a small group before a full rollout. The full reasoning, with caveats, is in the business report.

## What is in this folder

| File | What it is |
|---|---|
| `Telco_Churn_Analysis.ipynb` | The full analysis in Python: cleaning, exploration, revenue impact, models and dashboard |
| `telco_churn_summary.png` | One-page dashboard for management |
| `Telecom-Customer-Churn_Report.pdf` | Plain-language report with findings and advice for a non-technical audience |
| `Telco Customer Churn.xlsx` | The dataset |

## Approach

1. **Cleaned the data.** Checked for duplicates and missing values. Found that 11 brand-new customers had a blank total-charges value instead of a number (they had not been billed yet), set those to 0, and converted the column to numeric. Recoded the senior-citizen flag to Yes/No for consistency.
2. **Explored churn patterns.** Compared churn rates across contract type, tenure, internet service, payment method and add-on services.
3. **Measured the revenue impact.** Worked out how much monthly revenue the departed customers represented and where it came from.
4. **Built prediction models.** A logistic regression (ROC AUC 0.84) and a random forest (ROC AUC 0.83), trained on 80% of the data and tested on the remaining 20%. The logistic regression identifies about 78% of customers who go on to leave, with about 51% precision, so it works best for ranking who to contact first rather than as a firm prediction.
5. **Communicated the results.** Built a one-page dashboard and a written report in plain language for business readers.

**Tools:** Python, pandas, matplotlib, scikit-learn, Google Colab.

## Limitations

This is a single snapshot with no reasons for leaving, so the findings show who leaves, not why. The patterns are associations, not proof of cause. The models use default settings and have not been fine-tuned.

## Running it yourself

1. Download this folder.
2. Open `Telco_Churn_Notebook.ipynb` in Google Colab or Jupyter.
3. Upload `telco-Customer-Churn.xlsx` when prompted, or place it in the same folder.
4. Run the cells in order.

## Data source

The Telco Customer Churn dataset is a widely used public sample dataset, originally published by IBM.

## About me

Amarachi Amaechi | Data analyst, Business Intelligence Consultant and Researcher | [LinkedIn](https://www.linkedin.com/in/amarachiamaechi) | marydolaris@gmail.com
