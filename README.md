# 🛍️ Customer Shopping Behavior Analysis

A full-stack data analytics project that uncovers insights into customer spending patterns, product preferences, and subscription behavior from 3,900 retail transactions — using Python, PostgreSQL, and Power BI.

---

## 📌 Project Overview

This project analyzes transactional retail data to help businesses make smarter, data-driven decisions. The analysis spans the complete data pipeline: from raw data cleaning and feature engineering to SQL-based business queries and an interactive Power BI dashboard.

---

## 📂 Dataset Summary

| Property | Detail |
|---|---|
| Total Records | 3,900 transactions |
| Features | 18 columns |
| Missing Data | 37 values in `review_rating` (imputed) |

**Key Features:**
- **Demographics** — Age, Gender, Location, Subscription Status
- **Purchase Details** — Item, Category, Amount, Season, Size, Color
- **Behavior** — Discount Applied, Previous Purchases, Frequency, Review Rating, Shipping Type

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python (Pandas) | Data cleaning & feature engineering |
| PostgreSQL | Business query analysis |
| Power BI | Interactive dashboard |

---

## 🐍 Data Preparation (Python)

- Loaded dataset using `pandas`
- Handled missing values in `review_rating` using **median imputation per product category**
- Renamed all columns to `snake_case` for consistency
- Feature engineering:
  - `age_group` — binned customer ages into groups
  - `purchase_frequency_days` — derived from purchase frequency data
- Dropped redundant column `promo_code_used` (duplicate of `discount_applied`)
- Exported cleaned data to **PostgreSQL** for SQL analysis

---

## 🗄️ SQL Business Analysis (PostgreSQL)

Ten structured queries were written to answer real business questions:

| # | Query | Insight |
|---|---|---|
| 1 | Revenue by Gender | Compared total spend across male vs. female customers |
| 2 | High-Spending Discount Users | Customers using discounts but spending above average |
| 3 | Top 5 Products by Rating | Highest average review-rated products |
| 4 | Shipping Type Comparison | Avg spend — Standard vs. Express shipping |
| 5 | Subscribers vs. Non-Subscribers | Spend and revenue comparison by subscription status |
| 6 | Discount-Dependent Products | Top 5 products with highest % of discounted purchases |
| 7 | Customer Segmentation | Classified into New, Returning, and Loyal segments |
| 8 | Top 3 Products per Category | Most purchased items within each category |
| 9 | Repeat Buyers & Subscriptions | Do customers with 5+ purchases subscribe more? |
| 10 | Revenue by Age Group | Total revenue contribution per age segment |

---

## 📊 Power BI Dashboard

An interactive dashboard was built to visualize all key findings, including:
- Revenue breakdowns by gender, age group, and category
- Customer segmentation distribution
- Subscription behavior patterns
- Discount usage trends

---

## 💡 Business Recommendations

1. **Boost Subscriptions** — Promote exclusive subscriber-only benefits to drive sign-ups
2. **Customer Loyalty Programs** — Reward repeat buyers to move them into the "Loyal" segment
3. **Review Discount Policy** — Reduce dependency on discounts for margin-sensitive products
4. **Product Positioning** — Feature top-rated and best-selling items in marketing campaigns
5. **Targeted Marketing** — Focus ad spend on high-revenue age groups and Express shipping users

---

## 📁 Project Structure

```
customer-shopping-behavior-analysis/
│
├── data/
│   └── shopping_behavior.csv          # Raw dataset
│
├── notebooks/
│   └── eda_cleaning.ipynb             # Python EDA & cleaning notebook
│
├── sql/
│   └── business_queries.sql           # All 10 PostgreSQL queries
│
├── dashboard/
│   └── shopping_dashboard.pbix        # Power BI dashboard file
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- PostgreSQL
- Power BI Desktop

### Setup

```bash
# Clone the repository
git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
cd customer-shopping-behavior-analysis

# Install Python dependencies
pip install pandas sqlalchemy psycopg2

# Run the cleaning notebook
jupyter notebook notebooks/eda_cleaning.ipynb
```

Then connect to your PostgreSQL instance and run the queries in `sql/business_queries.sql`.

---

## 📬 Contact

Feel free to connect or reach out for collaboration!

- **LinkedIn:** [your-linkedin-url]
- **Email:** your-email@example.com

---

⭐ *If you found this project useful, give it a star!*
