# Customer Segmentation using RFM Analysis + K-Means Clustering

## Overview
This project segments customers of a UK-based online retailer into distinct 
behavioral groups using RFM (Recency, Frequency, Monetary) analysis combined 
with K-Means clustering. The goal is to identify which customers drive the most 
revenue, which are at risk of churning, and what marketing actions are 
appropriate for each group.

## Key Finding
**Champions (30.6% of customers) generate 81.6% of total revenue** — 
making retention of this segment the single highest-priority business action.

## Dataset
- **Source:** [UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)
- **Also available on:** [Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)
- **Period:** December 2010 – December 2011
- **Raw size:** 541,909 transactions, 8 columns
- **After cleaning:** 386,019 rows, 4,325 unique customers

> Download the dataset from the links above and place `Online Retail.xlsx` 
> in the root directory before running the notebook.

## Project Steps
| Step | Description |
|------|-------------|
| 1 | Data Cleaning — remove cancellations, nulls, price outliers, duplicates |
| 2 | RFM Table — build Recency, Frequency, Monetary per customer |
| 3 | Clustering — log-transform, scale, elbow method, silhouette score, K-Means |
| 4 | Segment Profiling — label clusters in plain English |
| 5 | Visualizations — scatter plot and bar chart of segments |
| 6 | Business Framing — revenue analysis and actionable recommendations |

## Results

### Segment Profiles
| Segment | Customers | % of Customers | Avg Recency | Avg Frequency | Avg Monetary |
|---------|-----------|----------------|-------------|---------------|--------------|
| Champions | 1,325 | 30.6% | 29.8 days | 9.74 orders | £5,272.90 |
| Casual Customers | 2,015 | 46.6% | 54.6 days | 2.03 orders | £591.31 |
| Lapsed Customers | 985 | 22.8% | 254.5 days | 1.38 orders | £393.76 |

### Revenue Contribution
| Segment | Total Revenue | % of Revenue |
|---------|--------------|--------------|
| Champions | £6,986,589 | 81.6% |
| Casual Customers | £1,191,495 | 13.9% |
| Lapsed Customers | £387,852 | 4.5% |

## Business Recommendations
- **Champions:** VIP retention program — loyalty rewards, early product access,
  personalized outreach. Losing this segment would be catastrophic for revenue.
- **Casual Customers:** Increase purchase frequency via targeted promotions
  at the 45-60 day inactivity mark and product recommendations.
  Largest growth opportunity.
- **Lapsed Customers:** Single win-back email campaign. If no response in
  30 days, deprioritize — marketing spend is better directed at Casual Customers.

## Tech Stack
- **Python 3**
- **Pandas** — data manipulation
- **NumPy** — numerical operations
- **Scikit-learn** — K-Means clustering, StandardScaler, silhouette score
- **Matplotlib** — visualizations

## How to Run
1. Clone this repository
   ```
   git clone https://github.com/mishapatel2537/customer-segmentation-rfm.git
   ```
2. Install dependencies
   ```
   pip install -r requirements.txt
   ```
3. Download the dataset from UCI or Kaggle and place `Online Retail.xlsx`
   in the root folder
4. Open and run `Customer_Segmentation.ipynb` top to bottom

## Project Structure
```
customer-segmentation-rfm/
│
├── Customer_Segmentation.ipynb   # Main analysis notebook
├── README.md                     # Project documentation
├── requirements.txt              # Python dependencies
└── .gitignore                    # Excludes dataset file
```

## Acknowledgements
Dataset provided by Dr. Daqing Chen, London South Bank University,
via the UCI Machine Learning Repository.
