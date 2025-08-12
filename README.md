# E-commerce-Sales-Analysis-Kaggle-
E-commerce Sales Analysis (Kaggle Dataset) – Data cleaning, exploratory analysis, cohort retention, and RFM segmentation of 392k+ transactions from an online retail store (2010–2011). Includes top product &amp; country insights, customer segmentation, and a summary dashboard.
# E-commerce Sales Analysis (Kaggle)

## Dataset
- Source: Kaggle Online Retail (2010-12 to 2011-12)
- Clean rows: 392,691 (after removing cancellations/negatives/outlier)
- Files: `ecommerce_clean.csv`, `RFM_Analysis_Results.csv`, `ecommerce_summary_dashboard.png`

## Key KPIs
- Total Revenue: £8.72M (outlier removed)
- Orders: 18,532 | Unique Customers: 4,338 | AOV: £479.56
- Top Country: United Kingdom (~82% of revenue)
- Top Products: REGENCY CAKESTAND 3 TIER, RABBIT NIGHT LIGHT

## Methods
- Cleaning: drop NA `CustomerID`/`Description`, filter `Quantity>0`, `UnitPrice>0`
- Features: `TotalPrice = Quantity*UnitPrice`, `YearMonth`
- Outlier handling: removed invoice 581483 (~1.90% total)
- RFM: Recency, Frequency, Monetary + quintile scores → 5 segments
- Cohort retention: monthly cohorts with heatmap

## Insights
- Sales peak: Nov 2011; UK dominates revenue
- VIP & Loyal segments generate most revenue (see dashboard)
- Price spikes for REGENCY CAKESTAND 3 TIER around Oct 2011
- Product mix: top items are gifting/home décor; seasonal uplift visible

## Files
- `ecommerce_clean.csv` — cleaned transactions
- `RFM_Analysis_Results.csv` — customer RFM with segment
- `ecommerce_summary_dashboard.png` — summary visuals

## How to Reproduce
1. `pip install pandas matplotlib seaborn`
2. Run notebooks/scripts in order: cleaning → EDA → RFM → Cohort → dashboard.

## Next Work
- Market basket analysis (association rules)
- Forecasting monthly sales (ARIMA/Prophet)
