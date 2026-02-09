# Supply-Chain-Analytics-BI
This project is an end-to-end Supply Chain Analytics solution built using a star schema data model and interactive dashboards. The dataset covers 2 years of operational data (2023–2024) and supports KPI tracking for procurement, inventory, shipments, deliveries, sales, and production.

The goal of this project is to analyze supply chain performance and support decision-making through reliable metrics such as order quantity, shipment quantity, delivered quantity, and inventory stock levels.

## Project Overview

This project includes:

- A supply chain star schema data model
- Fact tables for core operational processes
- Dimension tables for master data
- KPI calculations (DAX / SQL)
- Dashboards for supply chain insights

## Data Model (Star Schema)

### Fact Tables
- `fact_procurement` (Purchase Orders)
- `fact_inventory` (Daily Stock Levels)
- `fact_shipment` (Shipment Transactions)
- `fact_sales` (Sales Transactions)
- `fact_production` (Production Output)

### Dimension Tables
- `dim_date` (Daily values for 2023–2024)
- `dim_products`
- `dim_supplier`
- `dim_customer`
- `dim_facility`

## Key Metrics Example

### Inventory Stock Level
DAX:
Total_Delivered_Quantity =
CALCULATE(
    [Total_Sales_Quantity],
    fact_shipment[status] = "Delivered"
)

## Dashboard Insights

This dashboard helps answer key business questions such as:

- How much inventory is available across facilities?
- How many units are being ordered vs delivered?
- Which suppliers contribute the most to procurement volume?
- Which supplier has highest delays?
- Which products have the highest shipment and sales demand?
- Facility-level performance comparison for inventory and shipments
- Daily trends across 2023–2024
