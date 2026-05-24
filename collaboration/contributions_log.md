# Contributions Log

Use this file to provide evidence for the collaboration rubric.

| Date | Student | Contribution | Files / Evidence | Next Step |
|---|---|---|---|---|
| 2026-05-21 | Student D | Set up collaboration repo structure and data folder. | `README.md`, `collaboration/`, `reports/student_sections/` | Team members add notebooks and update task board. |
| 2026-05-24 | Student B (Mukesh Murugesan, 25747763) | Completed all 5 regression notebooks: 2 EDA (person, sales_order_detail), Preparation (feature selection, cleaning, split, engineering, transformations), Baseline (DummyRegressor, R2=0.00, RMSE=$1,464), and Regression (Random Forest R2=0.8746, RMSE=$633, confirming hypothesis). | `notebooks/student_B_regression/` (5 notebooks) | Peer review of Student B notebooks; complete ethics + report section. |

## Individual Contribution Summary Template

### Student A

- Assigned role:
- Main datasets:
- Modelling task:
- Key contribution:
- Files contributed:
- Peer review completed:

### Student B — Mukesh Murugesan (25747763)

- Assigned role: Regression
- Main datasets (EDA): `person.csv`, `sales_order_detail.csv`
- Modelling task: Predict `line_total` (revenue per order line item) using Random Forest Regression
- Key contribution: Built complete regression pipeline — 6-table join, leakage-prevention feature selection (10 features), data cleaning, 70/15/15 split, 4 engineered features (has_discount, order_year, order_month, price_vs_list), log1p target transform, label encoding, StandardScaler. Compared Linear Regression vs Random Forest vs Gradient Boosting. Final model: Random Forest (n_estimators=50, max_depth=20), R2=0.8746, RMSE=$633, MAE=$262 on validation set — significantly beating baseline (R2=0.00, RMSE=$1,464). Hypothesis confirmed.
- Files contributed: `36106_26AU_AT3_25747763_SB_1_eda_person.ipynb`, `36106_26AU_AT3_25747763_SB_2_eda_sales_order_detail.ipynb`, `36106_26AU_AT3_25747763_SB_a_Preparation_updated.ipynb`, `36106_26AU_AT3_25747763_SB_b_Baseline.ipynb`, `36106_26AU_AT3_25747763_SB_c_regression.ipynb`
- Peer review completed: Pending

### Student C

- Assigned role:
- Main datasets:
- Modelling task:
- Key contribution:
- Files contributed:
- Peer review completed:

### Student D

- Assigned role: Clustering
- Main datasets:
- Modelling task:
- Key contribution:
- Files contributed:
- Peer review completed:

