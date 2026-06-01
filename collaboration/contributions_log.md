# Contributions Log

Use this file to provide evidence for the collaboration rubric.

| Date | Student | Contribution | Files / Evidence | Next Step |
|---|---|---|---|---|
| 2026-05-21 | Student D | Set up collaboration repo structure and data folder. | `README.md`, `collaboration/`, `reports/student_sections/` | Team members add notebooks and update task board. |
| 2026-05-24 | Student B (Mukesh Murugesan, 25747763) | Completed all 5 regression notebooks: 2 EDA (person, sales_order_detail), Preparation (feature selection, cleaning, split, engineering, transformations), Baseline (DummyRegressor, R2=0.00, RMSE=$1,464), and Regression (Random Forest R2=0.8746, RMSE=$633, confirming hypothesis). | `notebooks/student_B_regression/` (5 notebooks) | Peer review of Student B notebooks; complete ethics + report section. |
| 2026-05-24 | Student D (Shameel Zeshan Khader Sheriff, 26030371) | Completed clustering stream for product portfolio segmentation. Finalised assigned EDA notebooks, preparation notebook, baseline explanation, K-Means/Mean Shift clustering comparison, final K-Means `k=5` model, cluster profiling, business recommendations, and ethics discussion for report. | `notebooks/student_D_clustering/` (5 EDA notebooks, Preparation, Baseline, Clustering), `reports/student_sections/`, `reports/final_report_assets/` | Completed; keep final artefacts aligned with submitted report and notebook PDFs. |

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
- Main datasets: `sales_territory.csv`, `special_offer.csv`, `special_offer_product.csv`, `product_cost_history.csv`, `product_list_price_history.csv`, plus supporting modelling tables `sales_order_detail.csv`, `product.csv`, `product_sub_category.csv`, and `product_category.csv`
- Modelling task: Product portfolio segmentation for margin-aware promotion decision support using unsupervised clustering
- Key contribution: Defined the clustering business use case, completed assigned EDA notebooks with table-grain, key, duplicate, missing-value, and join-coverage checks, and justified the final modelling grain of one row per sold product. Built the preparation pipeline that aggregates transactions, offer eligibility, actual promotion usage, and price/cost history to product level. Selected 13 scaled numeric clustering features across demand, revenue, realised price, gross margin, promotion eligibility, actual promotion usage, and historical price/cost movement. Explained why a supervised baseline is not applicable for clustering. Compared K-Means and Mean Shift using inertia, silhouette score, Davies-Bouldin index, cluster size balance, and business interpretability. Selected K-Means with `k=5` because it produced five actionable segments: promotion-risk revenue products, high-margin frequent sellers, low-activity review products, price-cost volatility products, and premium revenue products. Wrote the clustering report section with business impact, model limitations, ethics/privacy considerations, and recommendations for discount guardrails, cross-sell/bundles, demand review, cost monitoring, and price integrity.
- Files contributed: `36106_26AU_AT3_26030371_SD_1_eda_sales_territory.ipynb`, `36106_26AU_AT3_26030371_SD_2_eda_special_offer.ipynb`, `36106_26AU_AT3_26030371_SD_3_eda_special_offer_product.ipynb`, `36106_26AU_AT3_26030371_SD_4_eda_product_cost_history.ipynb`, `36106_26AU_AT3_26030371_SD_5_eda_product_list_price_history.ipynb`, `36106_26AU_AT3_26030371_SD_a_Preparation_updated.ipynb`, `36106_26AU_AT3_26030371_SD_b_Baseline.ipynb`, `36106_26AU_AT3_26030371_SD_c_clustering.ipynb`
- Peer review completed: Self-review, report consistency check, notebook PDF export check, and final artefact alignment completed
