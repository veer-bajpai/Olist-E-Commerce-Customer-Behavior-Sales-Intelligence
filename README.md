# 🛒 Olist E-Commerce — Customer Behavior & Sales Intelligence

> **End-to-end exploratory data analysis of Brazil's largest e-commerce marketplace dataset, covering 100k+ orders from 2016–2018. Includes RFM-based customer segmentation, revenue trend analysis, satisfaction scoring, and geo-demographic profiling.**

---

## 📌 Project Overview

This project analyses the publicly available [Olist Brazilian E-Commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) to surface actionable business intelligence across four key dimensions:

| Dimension | Questions Answered |
|---|---|
| 📈 Sales Trends | How did revenue grow over time? Where are the seasonal peaks? |
| 👥 Customer Segments | Who are the most valuable customers? Who is at risk of churning? |
| ⭐ Satisfaction | What do review scores reveal about product & delivery quality? |
| 🗺️ Geography | Which states drive the most orders? Where is untapped potential? |

---

## 🗂️ Repository Structure

```
olist-ecommerce-analysis/
│
├── data/
│   └── raw/                  # Raw CSVs from Kaggle (git-ignored)
│
├── notebooks/
│   └── Olist_E_Commerce_Customer_Behavior___Sales_Intelligence.ipynb
│
├── plots/                    # Generated chart images
│   ├── customer_segments.png
│   ├── monthly_revenue_trend.png
│   ├── review_score.png
│   ├── payment_type.png
│   ├── price_distribution.png
│   ├── customer_state.png
│   └── order_status.png
│
├── INSIGHTS.md               # Written summary of all key findings
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 📊 Key Charts & Findings

### Monthly Revenue Trend
Revenue grew from near-zero in late 2016 to a peak of **R$1.2 million** in November 2017, stabilising at **R$1.0–1.2M** through mid-2018. Clear Black Friday seasonality is visible every November.

### Customer Segments (RFM)
Five segments identified using Recency–Frequency–Monetary scoring:
- **Potential Loyalists** (~41k) — largest group, high conversion opportunity
- **Loyal Customers** (~34k) — steady repeat buyers
- **At Risk** (~13k) — need re-engagement
- **Champions** (~8k) — top-tier VIP customers
- **Lost Customers** (~3k) — minimal ROI to re-target

### Review Scores
Over **57,000 orders** received a perfect 5-star rating. The distribution follows a classic **J-curve** — polarised between delighted and unhappy customers with few neutral responses.

### Payment Types
**Credit card** accounts for ~75% of all transactions, reflecting Brazil's instalment-based credit culture. Boleto (~19%) serves the unbanked segment.

### Price Distribution
Heavily right-skewed — the majority of items sell for **under R$200**, with a long tail reaching R$7,000+. Olist is primarily a mass-market platform.

### Geographic Reach
São Paulo state alone accounts for **~41,500 orders**, more than 3× the next largest state (RJ). The Southeast region dominates overall demand.

### Order Fulfilment
A **~97% delivery success rate** indicates a reliable logistics network, with cancellations and unavailability together accounting for less than 1% of orders.

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/olist-ecommerce-analysis.git
cd olist-ecommerce-analysis
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate        # macOS / Linux
venv\Scripts\activate           # Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Download the dataset
The notebook auto-downloads the dataset via `kagglehub`. Make sure you have a valid Kaggle API key configured at `~/.kaggle/kaggle.json`.

```bash
# Or manually download from:
# https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
```

### 5. Run the notebook
```bash
jupyter notebook notebooks/Olist_E_Commerce_Customer_Behavior___Sales_Intelligence.ipynb
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.10+ | Core language |
| Pandas | Data wrangling & aggregation |
| NumPy | Numerical operations |
| Matplotlib | Base plotting |
| Seaborn | Statistical visualisations |
| KaggleHub | Automated dataset download |
| Jupyter Notebook | Interactive analysis environment |

---

## 📁 Dataset

**Source:** [Olist Brazilian E-Commerce Public Dataset — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

| File | Description |
|---|---|
| `olist_orders_dataset.csv` | Order lifecycle and timestamps |
| `olist_order_items_dataset.csv` | Item-level price and freight |
| `olist_order_payments_dataset.csv` | Payment method and value |
| `olist_order_reviews_dataset.csv` | Customer review scores |
| `olist_customers_dataset.csv` | Customer location data |
| `olist_sellers_dataset.csv` | Seller location data |
| `olist_products_dataset.csv` | Product categories and dimensions |
| `olist_geolocation_dataset.csv` | Lat/lon for zip codes |
| `product_category_name_translation.csv` | Portuguese → English category names |

> ⚠️ Raw CSV files are excluded from this repository via `.gitignore` due to their size. Download them directly from Kaggle.

---

## 💡 Insights Summary

See [`INSIGHTS.md`](./INSIGHTS.md) for a detailed written breakdown of all findings and actionable business recommendations.

---

## 📄 License

This project is licensed under the **MIT License**. The underlying dataset is made available by Olist under the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.

---

## 🙌 Acknowledgements

- [Olist](https://olist.com/) for making the dataset publicly available.
- The Kaggle community for enriching discussions around this dataset.
