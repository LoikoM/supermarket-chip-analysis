#  Chip Customer Segmentation Analysis

##  Project Overview

This project supports the **Category Manager for Chips** at a major supermarket chain in understanding the types of customers purchasing chips and their buying behaviour. The insights derived from this analysis will help inform the upcoming **category strategy** for the next six months, with a particular focus on **customer segmentation**, **spend behaviour**, and **product preferences**.

---

##  Data Sources

1. **Transaction Data** (`QVI_transaction_data.xlsx`) : purchase-level data such as product name, quantity, total spend, and customer ID.

2. **Customer Profile Data** (`QVI_purchase_behaviour.csv`) : customer segmentation information:
   - `LIFESTAGE`: Describes the customer's family situation and age group.
   - `PREMIUM_CUSTOMER`: Categorizes shoppers based on price sensitivity and quality preference.

These datasets were merged on the unique loyalty card number (`LYLTY_CARD_NBR`).

---

##  Data Cleaning & Preparation

The following preprocessing steps were applied:

- **Date Conversion**: Excel serial dates were converted to `datetime` format.
- **Filtering for Chips Only**: Products were filtered to include only those related to chips based on keywords (`chip`, `chips`, `chp`).
- **Outlier Removal**: A customer who purchased over 200 packs in a single transaction was removed.
- **Missing Data**: Any missing or malformed pack sizes were handled during feature engineering.

---

New features were derived to aid segmentation:

- **Pack Size**: Extracted from product names using regex (e.g., "175g" → 175).
- **Brand Name**: Standardized by extracting the first word from the product name and mapping inconsistencies to consistent brand labels (e.g., "Smith" → "Smiths", "RED" → "RRD").

---

##  Segment Analysis

We explored customer behavior by segmenting based on `LIFESTAGE` and `PREMIUM_CUSTOMER` status. Key metrics included:

| Metric | Description |
|--------|-------------|
| `total_sales` | Total dollar spend per segment |
| `avg_sales` | Average spend per transaction |
| `transaction_count` | Number of transactions |
| `total_units` | Total quantity of chip packs purchased |
| `unique_customers` | Number of unique shoppers in each segment |
| `avg_units_per_customer` | Total units divided by number of customers |

These metrics help identify **high-value segments**, **volume drivers**, and **potential areas for promotion or assortment changes**.

---

## Key Findings (To Be Expanded)

Initial analysis reveals:
- Segments with higher sales volume.
- Preferences in pack size by segment.
- Whether premium segments buy more expensive brands or larger pack sizes.

(These findings will be fully detailed in the final report to be shared.)

---

##  Next Steps

- Finalize segment insights
- Visualize trends in chip preferences by segment
- Generate actionable recommendations for product, pricing, and promotion strategies
- Compile presentation-ready visuals and summary tables

---

## Tech Stack

- **Python** (Pandas)
- **Jupyter Notebook**
- **Excel / CSV**
- **Tableau**

---
## Key Insights Summary

This project explores chip purchasing behaviour across different customer segments.  
The analysis identified key trends in total sales, customer preferences, and pack size popularity:

- **Mainstream customers** are the primary buyers, contributing to **38.78%** of total sales.
- **Young Singles/Couples** and **Retirees** are the top-performing groups within the mainstream segment.
- The **175g pack size** is the most popular across all segments.
- **Doritos** is the leading brand in sales, followed by **Smiths** and **Thins**.
- **Premium customers** tend to spend more per transaction, particularly **Older Singles/Couples**.

Full insights and strategic recommendations can be found in the [`INSIGHTS.md`](INSIGHTS.md) report.
---
## Contact

Project owner: *Mykyta Loiko*  



