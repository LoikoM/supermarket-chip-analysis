# Strategic Customer Segmentation & Sales Performance Analysis

## Project Overview
This project provides an end-to-end analysis of the Australian Snack & Chips category. It combines **Python data engineering** with a **Tableau Executive Dashboard** to help Superstore Managers identify high-value customer segments and optimize retail strategies.

![Dashboard Preview](images/dashboard_main.jpg)

## Data Pipeline (Python)
The analysis started with a deep-dive into transaction data (2018-2019).
* **Data Cleaning:** Standardized brand names (e.g., 'RRD' to 'Red', 'Snbts' to 'Sunbites') and filtered for chip products only.
* **Outlier Detection:** Removed abnormal transactions (e.g., a single customer purchasing 200 packs) to ensure data integrity.
* **Feature Engineering:** Extracted `Pack Size` and `Brand` from product names using Regular Expressions.
* **Segmentation:** Grouped customers by Lifestage and Premium Status to calculate unit averages and sales share.

## Tableau Dashboard Highlights
The dashboard translates raw data into actionable insights:
* **Mix Delta Analysis:** A custom metric highlighting where sales share exceeds volume share.
* **Lifestage Correlations:** Correlating customer lifestages with price sensitivity (Budget vs. Premium).
* **Interactivity:** Integrated dynamic filters, MoM benchmarking, and a contextual info pop-up.

## Repository Structure
* `/notebooks`: Contains `code.ipynb` with the full Python cleaning and analysis process.
* `/outputs`: Cleaned datasets and PDF exports of the dashboard.
* `README.md`: This project summary.

## How to Use
1. Explore the [Python Notebook](notebooks/code.ipynb) to see the data transformation.
2. Visit the [Live Dashboard on Tableau Public](YOUR_TABLEAU_LINK) for the interactive experience.

---
**Author:** Mykyta Loiko | [LinkedIn](YOUR_LINKEDIN_LINK)

