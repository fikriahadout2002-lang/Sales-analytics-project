## 📌 Project Overview
An end-to-end data analytics project using a **Zepto E-Commerce dataset**. The project spans the entire analytics pipeline: cleaning and validating raw data in **Python (Pandas)**, executing targeted business and financial queries via **SQL (MySQL)**, and building an interactive **Power BI** dashboard for inventory management, risk analysis, and pricing strategies.

---

## 📁 Repository Structure
```text
Sales-analytics-project/
│
├── data/                      # Raw and cleaned datasets
│   ├── raw/                   # Raw Excel dataset
│   └── cleaned_ecommerce_data.csv
├── notebooks/                 # Python scripts for cleaning & validation
│   └── Ecommerce_analysis.ipynb
├── sql_queries/               #Database connection & queries
│   └── sql.ipynb
└── power_bi/                  # Power BI dashboard files & visual assets
    └── sales_analytics.pbix


## 🛠️ Tech Stack & Architecture
 * **Python (Pandas, NumPy, SQLAlchemy, dotenv):** Data cleaning, feature engineering, mathematical price validation, and database connection.
 * **SQL (MySQL):** Aggregations, financial KPI calculations, category performance, and stockout risk analysis.
 * **Power BI:** Interactive visualizations, KPI cards, category stock value distribution, and customer savings metrics.
## 🔄 Project Pipeline & Workflow
### 1. Data Cleaning & Feature Engineering (Python)
 * **Data Validation:** Verified zero missing values across 3,732 records and confirmed mathematical consistency between mrp, discountPercent, and discountedSellingPrice.
 * **Feature Creation:**
   * money_saved: Monetary savings per unit (mrp - discountedSellingPrice).
   * total_stock_value: Financial value of available stock (availableQuantity * discountedSellingPrice).
 * **SQL Optimization:** Converted outOfStock boolean flags to binary integers (1 for True, 0 for False).
### 2. SQL Analytics & Key Business Insights
The database queries focused on four key operational areas:
 * **Financial KPIs:** Aggregated overall metrics including total unique products (1,676), total items in stock (14,960), total inventory valuation (224.9M), and total consumer savings (24.3M).
 * **Category Performance:** Ranked product categories by total stock value and average discount rates (e.g., *Cooking Essentials* leading in inventory volume).
 * **Out-of-Stock & Risk Analysis:** Identified high-risk categories based on stockout ratios (e.g., *Biscuits* at 28.57% out of stock, *Dairy, Bread & Batter* at 21.71%).
 * **High-Value Product Identification:** Pinpointed flagship capital-heavy items (e.g., *Borges Extra Light Olive Oil*).
### 3. Interactive Power BI Dashboard
The dashboard consolidates all core metrics into a single high-impact executive view:
 * **KPI Cards:** Total Products (4K), Average Discount (7.34%), Total Stock Value (217.34M€), and Out of Stock Count (605).
 * **Category Distribution:** Horizontal bar chart highlighting top value categories (*Cooking Essentials*, *Munchies*, *Paan Corner*).
 * **Stock Risk Visualization:** Donut chart analyzing available stock vs. out-of-stock proportions (80.40% available vs. 19.60% out of stock).
 * **Product Insights:** Top 10 products ranked by total consumer savings.
