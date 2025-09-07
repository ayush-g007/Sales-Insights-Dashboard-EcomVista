# Sales Insights for EcomVista

A complete project that centralizes fragmented ecommerce sales data, builds actionable KPIs with SQL, and visualizes insights in Tableau.

## What's Inside
- **data/**: Synthetic datasets (CSV) for regions, products, customers, calendar, and sales.
- **sql/**: Database schema, views, and KPI queries.
- **ecomvista.db**: Preloaded SQLite database with all tables and views.
- **tableau/**: Step-by-step guide and calculated fields for Tableau.
- **report/**: Business report template and user manual.

## Quickstart

### Option A: Use the SQLite DB (fastest)
1. Open SQL client and connect to `ecomvista.db` (SQLite).
2. Explore views (start with `v_sales_enriched`, `v_kpi_by_date`, `v_top_products`, `v_region_performance`).
3. Run queries from `sql/kpi_queries.sql`.

### Option B: Create your own DB
1. Create a new database in your preferred RDBMS.
2. Run `sql/schema.sql` to create tables.
3. Import CSVs from `data/` into their respective tables.
4. Run `sql/views.sql` to create analytical views.
5. Run KPI queries from `sql/kpi_queries.sql`.

### Build the Tableau Dashboard
1. Open Tableau Desktop.
2. Connect to **SQLite** and select `ecomvista.db` (or connect to the CSVs in `data/`).
3. Use the view **`v_sales_enriched`** as primary data source.
4. Recreate the following **KPI tiles** and **charts** (see `tableau/dashboard_instructions.md`):
   - KPI: Total Net Sales, Total Gross Profit, Profit Margin %, Orders, Units Sold
   - Charts: Sales Trend by Month, Top Products, Region Performance, Seasonality, Demographics

## Tech Stack
- **Data**: CSVs with synthetic but realistic ecommerce patterns
- **SQL**: SQLite (portable) + ANSI SQL (portable to Postgres/MySQL)
- **BI**: Tableau (instructions + calculated fields included)

## Notes
- Data covers **2023-01-01 to 2024-12-31** with seasonality and returns.
- Profit margin accounts for discounts and returns.
- Use this as a base to add forecasts, cohort analysis, RFM, or CLV features.
