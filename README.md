# Nike Retail Analytics – Profitability Analysis

## Project Overview

This project investigates potential profit leakage in Nike retail sales by analysing product profitability, product lines, geographical regions, sales channels and discount levels.

The aim is to identify areas where profitability may be weaker and recommend strategies that could help improve retail performance.

**Course:** MSc Data Science  
**Project:** Nike Retail Profitability Analysis  
**Date:** 20 November 2026

## Team Members

- Hussnain
- Abubakar
- Mercy
- Mohammed

## Problem Statement

These Retail businesses need to understand not only how much revenue they generate but also how much profit they retain after costs.

This project analyses a Nike sales dataset to identify products, regions and sales channels that perform well or poorly in terms of estimated profitability. It also explores the relationship between discount levels and estimated profit.

This is an educational case study using the supplied dataset and assumed cost figures. It does not represent Nike's actual internal financial results.

## Research Questions

1. Which Nike products generate the highest and lowest estimated profits?
2. Which product lines contribute most to estimated profitability?
3. Which geographical regions perform best and worst?
4. How do online and retail sales channels compare?
5. How are different discount levels associated with estimated profit?

## Dataset

The project uses the following CSV file:

`Nike_Sales_With_Costs.csv`

The dataset contains **229 rows and 16 columns**, including:

- Order ID
- Gender category
- Product line
- Product name
- Size
- Units sold
- MRP
- Discount applied
- Revenue
- Order date
- Sales channel
- Region
- Profit
- Production cost
- Transportation cost
- Online shipment

### Data Preparation

The dataset was inspected and prepared using Python and Pandas.

The preparation included:

- Checking missing values.
- Checking duplicate records.
- Reviewing data types.
- Checking revenue, discounts and cost information.
- Standardising regional names.
- Selecting records with available MRP and positive revenue for financial analysis.

There were 457 missing cells and no duplicate rows in the original dataset.

The financial analysis used **110 records** with available MRP and positive revenue. The remaining 119 records were excluded because MRP was missing and revenue was zero.

## Methodology

The project uses exploratory data analysis (EDA) with Python.

### Tools and Libraries

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- GitHub

### Financial Assumptions

Because complete cost information was not available, the project uses the following assumptions for educational analysis:

| Cost | Assumption |
|---|---:|
| Production cost | 45% of MRP × units sold |
| Transportation cost | 3% of MRP × units sold |
| Online shipment | 80 per online order |
| Retail shipment | 0 |

These are project assumptions, not verified Nike operating costs. The currency of the dataset was not specified, so financial values are presented in dataset currency units.

### Estimated Profit Formula

```python
Estimated_Profit = (
    Revenue
    - Estimated_Production_Cost
    - Estimated_Transportation_Cost
    - Online_Shipment
)
```

Revenue was treated as already reflecting discounts, so discounts were not subtracted a second time.

## Key Findings

The following results are based on the 110 records included in the financial analysis.

### Overall Financial Results

| Measure | Result |
|---|---:|
| Total revenue | 801,333.16 |
| Estimated production costs | 697,334.94 |
| Estimated transportation costs | 46,489.00 |
| Estimated online shipment costs | 4,240.00 |
| Total estimated profit | 53,269.22 |
| Estimated profit margin | 6.65% |
| Profitable records | 64 |
| Loss-making records | 46 |

### Product Analysis

- **SuperRep Go** generated the highest total estimated profit of 16,353.54.
- **React Infinity** recorded the largest estimated loss of -16,199.19.
- Other products with estimated losses included Air Jordan, Phantom GT and Kyrie Flytrap.

### Product Line Analysis

- Training generated the highest estimated profit at 30,924.83.
- Lifestyle generated 13,157.94.
- Soccer was the only loss-making product line, with an estimated loss of -1,207.56.

### Regional Analysis

- Kolkata recorded the highest estimated profit at 27,644.29.
- Pune followed with 21,676.67.
- Bengaluru recorded the largest estimated loss at -16,506.09.

### Sales Channel Analysis

| Sales Channel | Revenue | Estimated Profit |
|---|---:|---:|
| Retail | 386,968.67 | 47,608.26 |
| Online | 414,364.49 | 5,660.96 |

Online sales generated more revenue, but retail sales generated substantially higher estimated profit in this dataset.

### Discount Analysis

The analysis grouped discounts into four categories:

- Low: 0–25%
- Medium: above 25–50%
- High: above 50–75%
- Very High: above 75–100%

Average estimated profit decreased as the discount category increased. This indicates an association between higher discounts and lower estimated profit, but it does not prove that discounts alone caused lower profitability.

## Recommendations

Based on the analysis, the project recommends:

1. Review the pricing and cost structure of products with negative estimated profits.
2. Investigate why Bengaluru has a negative estimated profit in the analysed records.
3. Review online fulfilment and shipment costs.
4. Monitor high discount levels and assess their effect on profitability.
5. Consider expanding successful product lines such as Training.
6. Improve data quality by ensuring important fields such as MRP, costs and order dates are complete.

## Project Limitations

- The dataset contains only 229 records.
- Only 110 records were suitable for the financial analysis.
- Cost figures are based on assumptions rather than verified Nike financial data.
- Missing MRP and zero-revenue records were excluded from the financial analysis.
- The dataset currency was not specified.
- The findings show patterns and associations, not proof of cause and effect.
- The results should not be generalised to Nike's actual global business.

## Repository Structure

The GitHub repository contains the following project files:

```text
Nike-Retail-Analytics/
│
├── Nike_Retail_Profit_Analysis.ipynb
│
├── Nike_Sales_With_Costs.csv
│
├── Nike_Retail_Profitability_Technical_Report.docx
│
├── Nike_Retail_Analytics_Investigation_Blueprint.docx
│
├── Nike_Retail_Profitability_Analysis_with_Agile (2).pptx
│
└── README.md
```

## How to Run the Project

1. Download or clone this GitHub repository.
2. Make sure Python is installed.
3. Install the required libraries:

```bash
pip install pandas numpy matplotlib jupyter
```

4. Open the project folder in VS Code.
5. Open `Nike_Retail_Profit_Analysis.ipynb`.
6. Make sure the CSV file is in the same folder as the notebook.
7. Run the notebook cells from top to bottom.

## Project Presentation

The PowerPoint presentation is included in this repository:

`Nike_Retail_Profitability_Analysis_with_Agile (2).pptx`

It presents the project background, Agile approach, analysis, key findings and recommendations.

## Conclusion

This project demonstrates how data analysis can help investigate retail profitability and identify possible areas of profit leakage.

The findings highlight differences between products, product lines, regions, sales channels and discount categories. Although the analysis uses estimated costs and a limited dataset, it provides a useful example of how data-driven insights can support business decisions.

---

**Project completed as part of the MSc Data Science programme.**

**Team:** Hussnain, Abubakar, Mercy and Mohammed
