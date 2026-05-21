# Shared Data Dictionary

This file records table purpose, keys, and known data quality notes.

| Dataset | Grain | Primary Key | Useful For | Notes |
|---|---|---|---|---|
| `customer.csv` | customer | `customer_id` | customer modelling, territory/store linkage | Contains duplicate rows in current extract; remove exact duplicates. |
| `person.csv` | person | `person_id` | customer demographics/name fields where relevant | Contains duplicate rows; use carefully for privacy. |
| `product.csv` | product | `product_id` | product attributes, costs, list price, sellable flag | Contains duplicate rows; filter sellable products if modelling products. |
| `product_category.csv` | product category | `product_category_id` | category labels | Four broad categories. |
| `product_sub_category.csv` | product subcategory | `product_subcategory_id` | subcategory labels | Join to category. |
| `product_cost_history.csv` | product cost over time | `product_id`, `start_date` | current cost, cost volatility, margin features | Missing `end_date` likely means current active record. |
| `product_list_price_history.csv` | product price over time | `product_id`, `start_date` | current price, price volatility | Missing `end_date` likely means current active record. |
| `sales_order_header.csv` | order | `sales_order_id` | customer orders, channel, dates, territory, totals | Territory join to `sales_territory.csv` may be incomplete. |
| `sales_order_detail.csv` | order line | `sales_order_detail_id` | product quantity, unit price, discount, line total | Core table for product/customer feature engineering. |
| `sales_territory.csv` | territory | `territory_id` | territory context | Only four territories in current extract. |
| `special_offer.csv` | offer | `special_offer_id` | discount features | Missing `max_quantity` can mean no maximum quantity. |
| `special_offer_product.csv` | offer-product relationship | `special_offer_id`, `product_id` | promotion exposure | Bridge table. |
| `store.csv` | store | `store_id` | store/customer context | Useful if modelling store or reseller behaviour. |
| `unit_measure.csv` | unit measure | `unit_measure_code` | product unit labels | Reference table. |

## Shared Cleaning Rules

- Remove exact duplicate rows before modelling.
- Parse dates with `pd.to_datetime`.
- Treat missing active-history `end_date` values as open/current records.
- Do not use names or identifiers as model features unless there is a justified non-identifying transformation.
- Keep IDs in output tables for traceability, but exclude them from model matrices.
- Document incomplete joins instead of silently ignoring them.

