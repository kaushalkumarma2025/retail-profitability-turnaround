# Retail Profitability & Discount Strategy Analysis

## Executive Summary

This project analyzes profitability in the Sample Superstore retail dataset to identify products, discount levels, and regions associated with poor financial performance. The analysis focuses on the **Tables** and **Bookcases** subcategories, which together generated **$321,845.53 in sales but recorded a net loss of $21,198.04**.

The strongest area of concern is **Tables in the East region**, which recorded a loss of **$11,025.38**, a profit margin of **-28.17%**, and a loss-making record share of **97.50%**. Discount-level analysis also shows that profitability deteriorates at higher observed discount levels for both subcategories.

The project concludes with evidence-based recommendations to investigate discount practices, review persistently loss-making products, and establish ongoing profitability monitoring. These are proposed interventions, not implemented changes; the analysis does not claim that historical losses can be fully recovered.

## Business Problem

Retailers can generate strong sales while losing money on particular products, orders, or regions. The objective of this project is to identify where profitability is weakest, investigate the patterns associated with those losses, and prioritize potential management actions.

### Key Questions

- Which categories, subcategories, and regions have weak profitability?
- How does observed profitability vary across discount levels?
- Are losses concentrated in particular products or regions?
- Which areas should management investigate first?
- What monitoring practices could help detect unprofitable transactions?

## Dataset

The project uses the **Sample Superstore** dataset, containing **9,994 records** and 21 columns, including order dates, geographic information, product categories, sales, quantity, discount, and profit.

Dataset source: [Sample Superstore Dataset on Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

Check the dataset's license and redistribution terms before committing the raw CSV to a public repository. If redistribution is not permitted, document the download instructions and keep the data file out of the repository.

## Methodology

The analysis follows a structured workflow:

1. **Data quality and baseline assessment** — inspect the dataset, validate dates and records, and establish overall sales and profitability metrics.
2. **Exploratory profitability analysis** — compare performance across regions, segments, categories, and subcategories.
3. **Discount analysis** — examine how aggregate profit, profit margin, and the share of loss-making records vary across observed discount levels.
4. **Root-cause investigation** — analyze discount patterns for Tables and Bookcases, inspect large loss-making records, and identify products with low aggregate profitability.
5. **Regional and product prioritization** — compare the two subcategories across regions and rank areas requiring further investigation.
6. **Validation and consolidation** — reconcile regional and aggregate profit totals and consolidate the findings.
7. **Business recommendations** — translate the findings into proposed actions, implementation considerations, and monitoring metrics.

The analysis is descriptive. It identifies patterns and associations in historical data rather than proving that a particular factor caused the observed losses.

## Key Findings

### Overall performance of Tables and Bookcases

| Metric | Result |
|---|---:|
| Records in full dataset | 9,994 |
| Records in Tables and Bookcases | 547 |
| Combined sales | $321,845.53 |
| Combined net profit | -$21,198.04 |
| Combined profit margin | -6.59% |
| Loss-making records | 312 |
| Share of loss-making records | 57.04% |

### Subcategory performance

| Subcategory | Sales | Net Profit | Profit Margin | Loss-Making Records | Loss-Making Record Share |
|---|---:|---:|---:|---:|---:|
| Tables | $206,965.53 | -$17,725.48 | -8.56% | 203 of 319 | 63.64% |
| Bookcases | $114,880.00 | -$3,472.56 | -3.02% | 109 of 228 | 47.81% |

Tables are the primary profitability concern, with a larger net loss and a more negative margin than Bookcases.

### Regional findings

| Subcategory and Region | Sales | Net Profit | Profit Margin | Loss-Making Record Share |
|---|---:|---:|---:|---:|
| Tables — East | $39,139.81 | -$11,025.38 | -28.17% | 97.50% |
| Tables — South | $43,916.19 | -$4,623.06 | -10.53% | 52.94% |
| Tables — Central | $39,154.97 | -$3,559.65 | -9.09% | 68.06% |
| Tables — West | $84,754.56 | $1,482.61 | 1.75% | 42.24% |
| Bookcases — Central | $24,157.18 | -$1,997.90 | -8.27% | 72.00% |
| Bookcases — West | $36,004.12 | -$1,646.51 | -4.57% | 40.00% |
| Bookcases — East | $43,819.33 | -$1,167.63 | -2.66% | 47.14% |
| Bookcases — South | $10,899.36 | $1,339.49 | 12.29% | 28.57% |

Tables in the East are the most severe regional problem identified. Bookcases in Central are a secondary priority. Tables in the West and Bookcases in the South are profitable in aggregate and provide useful comparison cases for further investigation.

### Discount-level findings

- Tables recorded a small aggregate loss at the observed 20% discount level and increasingly negative margins at higher observed discount levels.
- Bookcases were close to break-even at 20% discount and recorded a negative aggregate margin at 30%.
- Every observed Table record at discounts of 40% or more was loss-making.
- Every observed Bookcases record at discount levels of 32%, 50%, and 70% was loss-making.

These are observed patterns, not recommended discount caps. Different products and orders may have different underlying economics, and the data does not establish that discounts alone caused the losses.

### Product-level findings

Among the five products with the largest negative total profits, the products were:

- Chromcraft Bull-Nose Wood Oval Conference Table: -$2,876.12
- Bush Advantage Collection Racetrack Conference Table: -$1,934.40
- Balt Solid Wood Round Tables: -$1,201.06
- BoxOffice By Design Rectangular and Half-Moon Table: -$1,148.44
- Riverside Furniture Oval Coffee Table: -$1,147.40

Together, these five products accounted for approximately **29.1% of the negative profit summed across all loss-making products** in Tables and Bookcases. This is not the same as 29.1% of the subcategories' net loss.

## Business Recommendations

### 1. Review discounting practices for Tables in the East

Investigate high-discount Table transactions in the East region, where the observed net loss was $11,025.38 and the profit margin was -28.17%. Review product-level margins and consider a margin-based discount approval process that flags orders expected to generate negative profit.

### 2. Investigate persistently loss-making products

Review selling prices, discount levels, acquisition costs, order quantities, and transaction characteristics for the worst-performing products. Consider product-specific pricing changes, supplier-cost discussions, or assortment changes only where further evidence supports them.

### 3. Investigate Bookcases in the Central region

Compare Central with the profitable South region to examine differences in discount levels, product mix, costs, and order characteristics. Use the findings to inform region-specific actions rather than assuming a uniform policy will work everywhere.

### 4. Establish ongoing profitability monitoring

Track net profit, profit margin, loss-making transaction share, average discount, and profitability by product and region. Flag transactions with negative expected margins for review and measure the outcomes of any pricing intervention.

### Measuring outcomes

Any intervention should be evaluated using net profit, profit margin, sales volume, and order conversion. A reduction in discounts may improve margin per order but could also reduce demand. The historical loss figures should not be treated as recoverable savings.

## Limitations

- **Descriptive analysis:** The findings show associations and historical patterns; they do not establish causation.
- **Demand response is unknown:** The dataset does not reveal how sales volume would change under different discount policies.
- **Cost information may be incomplete:** Additional cost and product-economics information may be needed to explain differences in profitability.
- **Regional comparisons may reflect product mix:** Regional performance can differ for reasons other than discounting.
- **No realized impact is claimed:** Recommendations are proposed actions; no pricing intervention was implemented or evaluated in this project.
- **Historical losses are not recoverable savings:** Any potential benefit must be estimated and validated separately.

## Repository Structure

The repository currently uses these notebook names:

```text
Retail Profitability Turnaround/
├── readme.md
├── data/
├── notebook/
│   ├── 01_Data_Quality_and_Baseline.ipynb
│   ├── 02_Exploratory_Profitability_Analysis.ipynb
│   ├── 03_Root-Cause Analysis of Profitability Gaps.ipynb
│   ├── 04_Product_Region_Profitability.ipynb
│   ├── 05_Discount_Product_Analysis.ipynb
│   ├── 06_Business_Opportunity_Prioritization.ipynb
│   ├── 07_Validation_and_Consolidation.ipynb
│   └── 08_Business_Recommendations.ipynb
└── requirements.txt
```

Avoid uploading the raw dataset if its license does not permit redistribution.

## Tools

- Python
- pandas
- NumPy
- Jupyter Notebook

Add Matplotlib or Plotly only if they are used in the notebooks.

## Conclusion

This project identifies a profitability problem in Tables and Bookcases, with Tables in the East region representing the highest-priority area for further investigation. The analysis combines aggregate profitability metrics, discount-level comparisons, product-level loss analysis, regional comparisons, and reconciliation checks to create a traceable evidence base for proposed business actions.

