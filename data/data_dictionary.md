# Data Documentation

## Data Overview

The QuickBite Express analysis uses approximately 149K orders
covering January–September 2025.

The data was stored and processed in SQL Server and organized into
three analytical layers:

Raw Data → Cleaned Data → Analytical Tables

## Raw Data

Raw source tables used the `fact_*` and `dim_*` naming convention.

| Table | Records |
|---|---:|
| fact_order | 149,166 |
| fact_order_items | 342,994 |
| fact_delivery_performance | 149,166 |
| fact_ratings | 68,842 |
| dim_customer | 107,776 |
| dim_menu_item | 342,671 |
| dim_restaurant | 19,995 |
| dim_delivery_partner_ | 15,000 |

## Cleaned Data

The cleaned layer contains tables without the `fact_` / `dim_`
prefix.

| Table | Records |
|---|---:|
| orders | 149,166 |
| order_items | 342,994 |
| delivery_performance | 149,166 |
| ratings | 68,825 |
| customer | 107,776 |
| menu_item | 342,671 |
| restaurant | 19,995 |
| delivery_partner | 15,000 |

## Analytical Tables

| Table | Records | Purpose |
|---|---:|---|
| calculated_customer | 107,776 | Customer-level pre/post-crisis metrics |
| calculated_restaurant | 19,995 | Restaurant-level crisis impact |
| high_value_customer | 5,259 | High-value customer identification |
| customer_reccommendations | 94,357 | Recovery priority and recommendation engine |

## Transformation Workflow

Raw SQL Server tables
→ cleaning and validation
→ cleaned analytical tables
→ customer/restaurant aggregations
→ customer segmentation and recovery scoring
→ Power BI business reporting

## Data Preparation

The analysis included:

- Data validation
- Duplicate/consistency checks
- Pre-crisis vs crisis classification
- Customer-level aggregation
- Restaurant-level aggregation
- Revenue calculations
- Order and cancellation analysis
- Delivery-performance analysis
- Customer rating analysis
- Loyal/high-value customer identification

## Data Availability

The original datasets are not included in this repository because the
project data is stored in SQL Server and the full dataset is too large
for a lightweight portfolio repository.

The repository therefore documents the data architecture, schema,
transformation process, and analytical outputs rather than distributing
the complete source data.
