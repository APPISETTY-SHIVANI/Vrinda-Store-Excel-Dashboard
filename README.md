# Vrinda Store – 2022 Annual Sales Dashboard (Excel)

An interactive Excel dashboard that analyses one year of online sales for Vrinda Store, an Indian women's and men's ethnic-wear brand selling across Amazon, Myntra, Flipkart and other marketplaces.

![Dashboard preview](dashboard.png)

## Business questions answered
1. How do monthly sales and order volumes trend through the year?
2. Who buys more – men or women – and in which age groups?
3. Which states drive the most revenue?
4. Which sales channels bring the most orders?
5. How many orders end up delivered vs. returned, cancelled or refunded?

## Key findings
| Metric | Result |
|---|---|
| Total sales | ₹21.18M across 31,047 order lines |
| Women vs. Men | Women contribute ~64% of sales (₹13.56M vs ₹7.61M) |
| Top state | Maharashtra (₹2.99M, ~14% of sales); top 5 states = ~53% |
| Top channel | Amazon (~35% of orders), then Myntra (~23%) and Flipkart (~22%) |
| Order outcomes | ~92% delivered; ~8% returned, cancelled or refunded |
| Age mix | Adults (30–49) ~50% of orders, Teenagers (18–29) ~30%, Seniors (50+) ~20% |
| Monthly trend | Sales peak in March (₹1.93M) and are lowest in November (₹1.62M) |

## What I did
- **Cleaned the data** (31,047 rows): standardised Gender (`M`/`W` → `Men`/`Women`), created an **Age Group** column (Teenager 18–29, Adult 30–49, Senior 50+), and extracted **Month** from the order date with `TEXT()`.
- Built **6 PivotTables** (sales vs. orders, gender, state, age × gender, channel, order status).
- Created **6 charts** (combo, pie, bar) and combined them into a single one-page **dashboard** with **slicers** (Month, Category) for interactive filtering.
- Added **4 KPI cards** (Total Sales, Total Orders, Delivery Rate, Avg Order Value) built with `GETPIVOTDATA`, `IFERROR` and `IF`, linked to the slicers so they update on filtering.

## Files
| File | Description |
|---|---|
| `Vrinda_Store_Data_Analysis.xlsx` | Full workbook: Dashboard, 6 pivot sheets, Raw data, Cleaned data |
| `images/dashboard.png` | Screenshot of the dashboard |

> Open the `.xlsx` in desktop Excel (2010+) for slicers to work. They do not work in Google Sheets or the GitHub preview.

## Tools used
Microsoft Excel – PivotTables, PivotCharts, Slicers, `TEXT()`, Find & Replace, data cleaning

## Limitations / next steps
- Order count is based on rows; 28,471 unique Order IDs exist across 31,047 rows (multi-item orders).
- Sales totals include returned, cancelled and refunded orders; a "net sales" view is a logical next step.
- The date column contains only 36 distinct dates (the 4th–6th of each month), so the monthly trend reflects those days rather than full-month activity.

## About me
Shivani | Aspiring Data Analyst | Excel · SQL · Power BI
