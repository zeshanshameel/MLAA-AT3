# Data Folder

Assignment CSV files should live in this folder because the official notebooks use:

`36106/assignment/AT3/data`

## Included Tables

- `customer.csv`
- `person.csv`
- `product.csv`
- `product_category.csv`
- `product_cost_history.csv`
- `product_list_price_history.csv`
- `product_sub_category.csv`
- `sales_order_detail.csv`
- `sales_order_header.csv`
- `sales_territory.csv`
- `special_offer.csv`
- `special_offer_product.csv`
- `store.csv`
- `unit_measure.csv`

## Notes For Modelling

- Some tables contain exact duplicate rows. Handle duplicates in preparation notebooks and explain the decision.
- Some joins are incomplete, especially territory coverage between `sales_order_header.csv` and `sales_territory.csv`.
- Missing `end_date` values in history tables usually indicate the current active record.

