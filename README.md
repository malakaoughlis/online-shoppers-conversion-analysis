 Online Shoppers Conversion Analysis

This project analyses online shopping sessions to understand which browsing behaviours are associated with a purchase.

## Business Question

**Which session characteristics are associated with purchase conversion, and how can an e-commerce company improve its conversion rate?**

## Dataset

Source:  
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

The dataset contains 12,330 website sessions and uses `Revenue` as the purchase target.

## Project Structure

```text
data/raw/                 Original dataset
data/processed/           Cleaned and Power BI-ready datasets
notebooks/                Python cleaning and EDA notebooks
dashboard/                Power BI dashboard
```

## Tools

Python, Pandas, Matplotlib, Power BI and DAX.

## Main Findings

- Overall conversion rate: **15.47%**
- Purchase sessions view more product pages.
- Conversion falls when the exit rate increases.
- New visitors convert better than returning visitors.
- Weekend conversion is slightly higher.
- November has the highest monthly conversion rate.

## Recommendations

- Reduce early exits.
- Improve product-page navigation.
- Personalise the experience for returning visitors.
- Strengthen campaigns from September to November.
- Focus on the best-performing traffic sources.


Run the notebooks in this order:

1. `01_data_exploration_and_cleaning.ipynb`
2. `02_exploratory_data_analysis.ipynb`
