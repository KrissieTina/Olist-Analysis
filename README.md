# Olist E-Commerce Power BI Dashboard

## Project Overview
This project provides a comprehensive, end-to-end business intelligence solution for Olist, a major Brazilian e-commerce marketplace. Built entirely in Power BI, the dashboard is designed to help executives, marketing teams, and logistics managers analyze revenue trends, track customer behavior, and pinpoint operational inefficiencies.

## Dashboard Pages

### 1. Executive Overview
This page acts as the financial anchor of the report, providing the C-Suite with immediate answers to the company's profitability and sales volume.

* **Key Metrics:** Total Revenue, Total Profit, Profit Margin %, YoY Revenue Growth.
* **Key Insights:** Includes a dynamic dual-line tracker for YoY performance and a drill-down matrix to view profitability from the Product Category down to the Subcategory level using conditional formatting.

<!-- PLACEHOLDER FOR PAGE 1 IMAGE -->
![Executive Overview Dashboard]([https://github.com/KrissieTina/Olist-Analysis/blob/main/Images/Overview.PNG]
*Caption: Executive Overview page showing revenue trends, product profitability, and year-over-year growth.*

---

### 2. Customer Analysis
This page pivots from financials to buyer behavior, answering *who* the customer is, *how* they pay, and *how happy* they are with their purchases.

* **Key Metrics:** Total Unique Customers, Average Order Value (AOV), Average Review Score.
* **Key Insights:** Highlights the dominance of Credit Cards vs. Boletos, visualizes shopping habits by day of the week, and maps out customer satisfaction (review scores) across different Brazilian states.

<!-- PLACEHOLDER FOR PAGE 2 IMAGE -->
![Customer Analysis Dashboard]([https://github.com/KrissieTina/Olist-Analysis/blob/main/Images/Customer%20Analysi.PNG]
*Caption: Customer Analysis page showing payment preferences, review scores by state, and order volume.*

## The Data Model
The backend of this project is built on a highly optimized **Star Schema**:
* **Custom Date Table:** A fully dynamic `Dim_Date` table built using DAX (`CALENDAR`, `MIN`, `MAX`) to enable robust Time Intelligence calculations (YTD, Previous Year).
* **Relationship Engineering:** Clean 1-to-Many relationships acting as the backbone, utilizing advanced bi-directional cross-filtering to accurately capture complex e-commerce behaviors (e.g., multi-payment orders).
* **Measure Hive:** All DAX calculations are centralized in a dedicated `_Measures` table for clean model architecture and measure branching.

<!-- PLACEHOLDER FOR DATA MODEL IMAGE -->
![Data Model Schema](insert-link-or-path-to-data-model-image.png)
*Caption: Star Schema data model featuring active/inactive relationships and the central fact tables.*

## Key DAX Calculations
* **Time Intelligence:** `TOTALYTD`, `SAMEPERIODLASTYEAR` for precise growth tracking.
* **Measure Branching:** Base measures (`Total Revenue`, `Total Cost`) layered into advanced analytics (`YoY Growth %`, `Average Order Value`).

## How to Use This Dashboard
1. Download the `.pbix` file from this repository.
2. Open the file in **Power BI Desktop**.
3. Use the interactive slicers (Year, Customer State, Order Status) located at the top/side of the pages to filter the entire report contextually.

