# Amazon Sales Data Analysis

> *Analyzed Amazon product sales data to understand the impact of discounting strategies, category performance, and pricing on customer ratings and review engagement.*

**Type:** #EDA | **Tools:** #Python #pandas #matplotlib #seaborn | **Period:** `2024`

---

## Key Insights

**1. Discounts don't drive ratings** — Discount percentage has a weak/no correlation with product rating (r = -0.162). Customers don't rate products higher simply because they received a discount. Amazon should not rely on discounting as a proxy for quality signals.

**2. Category quality is uneven** — Office Products leads with the highest average rating, while Car & Motorbike and Musical Instruments fall below 4.0 stars. These underperforming categories need targeted quality and post-purchase service improvements.

**3. Discounts don't drive more reviews** — The correlation between discount percentage and review count is near zero (r = 0.003). Heavy discounting does not increase customer engagement or review volume.

**4. Price is not a quality signal** — Actual price has only a weak positive correlation with rating (r = 0.128). Budget products perform comparably to premium ones, suggesting price-based market segmentation is viable.

**5. Office Products is an underserved gem** — Despite having the highest average rating, Office Products has relatively low review volume. This category is likely undermarketed and has untapped growth potential.

---

## Overview

Amazon's marketplace spans hundreds of product categories with vastly different pricing, discount, and rating dynamics. This project analyzes the Amazon Sales Dataset (1,465 products after cleaning) to answer five business questions about the relationship between discounts, pricing, product ratings, and customer review volume. The analysis was conducted using Python (pandas, matplotlib, seaborn) following the Ask → Prepare → Process → Analyze → Share → Act framework. Key findings reveal that discounting strategies are largely disconnected from customer satisfaction and engagement, while category-level performance gaps point to concrete operational opportunities.

---

## Data Source

| Field | Details |
|-------|---------|
| **Source** | [Amazon Sales Dataset](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset) via Kaggle (`karkavelrajaj/amazon-sales-dataset`) |
| **Format** | CSV (`amazon.csv`) |
| **Raw Size** | 1,465 rows, 16 columns (after deduplication on `product_id`) |
| **Cleaned Size** | 1,351 rows, 9 columns |
| **Key fields** | `product_id`, `main_category`, `actual_price`, `discounted_price`, `discount_percentage`, `rating`, `rating_count` |

---

## Limitations

- The dataset is a snapshot — no time dimension available, so trends over time cannot be analyzed.
- Ratings and reviews are self-selected; they may not represent all buyers (response bias).
- Discount percentage is calculated from listed prices, which may not reflect actual promotional mechanics (e.g., coupon stacking, Prime deals).
- Category labels were hierarchical; only the top-level label was retained for analysis, which may lose sub-category nuance.
- Correlation results are observational — no causal claims can be made without controlled experiments.

---

## Files

| File | Description |
|------|-------------|
| [`main.ipynb`](main.ipynb) | Full analysis notebook covering all 6 phases (Ask → Act) |
| [`data/raw/amazon.csv`](data/raw/amazon.csv) | Original, unmodified source data |
| [`data/processed/amazon_clean.csv`](data/processed/amazon_clean.csv) | Cleaned dataset used for analysis |
| [`docs/presentation.md`](docs/presentation.md) | 15-minute stakeholder talk track |
| [`reports/REPORT_TEMPLATE.md`](reports/REPORT_TEMPLATE.md) | Full technical report |

---

*Author: **jack2000-dev** | Last updated: May 2026*
