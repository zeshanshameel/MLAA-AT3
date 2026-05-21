# Student D - Clustering Report Section

## Business Understanding

Business use case:

Suggested HD option:

Segment customers by purchasing value, frequency, discount sensitivity, product mix, and channel behaviour so the retailer can design better loyalty, retention, promotion, and product recommendation strategies.

Alternative option:

Segment products by sales, pricing, cost, margin, promotion exposure, and demand behaviour.

Key objectives:

Stakeholders:

Hypothesis:

Customers or products can be meaningfully segmented into commercially actionable groups using behavioural, pricing, promotion, and transaction-derived features.

## Data Understanding

Describe only Student D assigned EDA datasets:

- `sales_territory.csv`
- `special_offer.csv`
- `special_offer_product.csv`
- `product_cost_history.csv`
- `product_list_price_history.csv`

Key findings:

Data quality notes:

- `product_cost_history.csv` has missing `end_date` values that likely represent current active cost records.
- `product_list_price_history.csv` has missing `end_date` values that likely represent current active price records.
- `sales_territory.csv` is small, so it is more useful as context or a joined feature than as the only clustering entity.
- Offer tables are useful for discount exposure and promotion intensity features.

## Data Preparation

Describe all tables actually used for the clustering model and why.

Possible customer segmentation tables:

- `customer.csv`: customer identifier and territory/store link.
- `sales_order_header.csv`: order dates, channel, customer, territory, and order total.
- `sales_order_detail.csv`: product-level purchase quantity, price, discount, and revenue.
- `product.csv`: product attributes, standard cost, list price, and product metadata.
- `product_category.csv`: category labels used to create category spend shares.
- `product_sub_category.csv`: subcategory labels for richer product mix features.
- `special_offer.csv`: discount type, discount percentage, and offer timing.
- `special_offer_product.csv`: product-offer relationship.
- `product_cost_history.csv`: cost and margin features.
- `product_list_price_history.csv`: price history and price volatility features.
- `sales_territory.csv`: territory context where join coverage is available.

Cleaning steps:

Feature engineering:

Recommended customer-level features:

- total spend
- order count
- average order value
- total quantity
- recency in days
- customer lifetime in days
- online order ratio
- discounted line ratio
- average discount percentage
- distinct product count
- distinct category count
- bike spend share
- component spend share
- clothing spend share
- accessory spend share
- estimated margin
- average margin percentage

Split or validation strategy:

## Modeling

Algorithms to compare:

- K-Means
- Agglomerative clustering
- Gaussian Mixture Model
- DBSCAN, if suitable

Parameter tuning:

Best model:

## Evaluation

Recommended metrics:

- Silhouette score
- Davies-Bouldin index
- Calinski-Harabasz score
- PCA visualisation
- Cluster profile table

Results:

Strong and weak cluster assignment analysis:

## Business Impact and Benefits

Benefits:

- targeted loyalty campaigns
- more efficient discounting
- retention strategy for low-recency customers
- premium product recommendations
- inventory planning by segment demand

Risks of poor segmentation:

- over-discounting profitable customers or products
- excluding low-value customers from useful offers
- misleading regional assumptions
- using segments as automatic pricing decisions instead of decision support

Final recommendation:

## Data Privacy and Ethical Concerns

Affected stakeholders:

Privacy concerns:

Fairness concerns:

Indigenous people risks:

Mitigations:

