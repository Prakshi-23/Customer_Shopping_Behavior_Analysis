.
├── data/
│   └── shopping_behavior_updated.csv        # Raw dataset (3,900 records, 18 columns)
├── notebooks/
│   └── Customer_Behavior_Analysis.ipynb     # Jupyter Notebook containing Data Prep & Profiling
├── sql/
│   └── customer_behavior_queries.sql        # Complete MySQL script with schema & 10 analytical queries
├── docs/
│   └── Customer_Behavior_Analysis_Documentation.docx # Comprehensive Word Documentation
├── README.md                                 # Project README file
└── requirements.txt                          # Python dependencies list


---

## 📊 Dataset Schema & Features

| Column Name | Type | Description |
| :--- | :--- | :--- |
| `customer_id` | `INT` | Unique identifier per customer record |
| `age` | `INT` | Customer age in years (18 - 70) |
| `gender` | `VARCHAR` | Demographic gender (Male / Female) |
| `item_purchased` | `VARCHAR` | Purchased product title |
| `category` | `VARCHAR` | Product broad grouping (Clothing, Footwear, Outerwear, Accessories) |
| `purchase_amount_(usd)` | `INT` | Basket transaction amount ($20 - $100) |
| `location` | `VARCHAR` | US State where purchase occurred |
| `review_rating` | `FLOAT` | Customer feedback rating (2.5 - 5.0) |
| `subscription_status` | `VARCHAR` | Loyalty subscription indicator (`Yes` / `No`) |
| `shipping_type` | `VARCHAR` | Shipping class (Standard, Express, Free Shipping, Next Day Air, 2-Day Shipping, Store Pickup) |
| `discount_applied` | `VARCHAR` | Promotional discount flag (`Yes` / `No`) |
| `previous_purchases` | `INT` | Count of prior orders (1 - 50) |

---

## 🔍 Analytical SQL Queries Summary

The project answers key strategic business questions using MySQL:

1. **Gender Revenue Generation**: Quantifies gross monetary contribution across male and female shoppers.
2. **High-Value Discount Shoppers**: Isolates discount users who still exceed the platform average purchase amount.
3. **Top Rated Products**: Ranks items boasting highest average product review scores.
4. **Fulfillment Type Spend Comparison**: Compares average ticket size between Standard and Express delivery.
5. **Subscription Economics**: Analyzes spend disparity and total revenue contribution of active subscribers vs. non-subscribers.
6. **Promotion Penetration Rates**: Evaluates which items are most frequently bought with promotional discounts.
7. **Customer Lifecycle Segmentation**: Uses CTEs to segment customers into `New` (1), `Returning` (2–10), and `Loyal` (>10) buckets based on order history.
8. **Category Leadership (Window Functions)**: Utilizes `ROW_NUMBER()` windowing to extract top 3 selling items per product category.
9. **Repeat Buyer Subscription Conversion**: Measures subscription adoption among high-frequency shoppers (>5 prior purchases).
10. **Demographic Revenue Performance**: Evaluates revenue generation across engineered age cohorts.

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+**
- **MySQL Server 8.0+** or MySQL Workbench
- Required Python libraries: `pandas`, `numpy`, `ydata-profiling`

### Installation

1. **Clone the Repository**:
   ```bash
   git clone [https://github.com/your-username/customer-behavior-analysis.git](https://github.com/your-username/customer-behavior-analysis.git)
   cd customer-behavior-analysis
Set Up Python Environment:

Bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate
pip install -r requirements.txt
Database Setup & SQL Execution:

Open MySQL Workbench / CLI.

Run the script located at sql/customer_behavior_queries.sql to instantiate the database, create the shopping_behavior table, and execute queries.

🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

📜 License
This project is licensed under the MIT License.
"""

with open("README.md", "w") as f:
f.write(readme_content)

print("README.md written successfully.")


```text?code_stdout&code_event_index=2
README.md written successfully.

Your Word documentation file (.docx) and GitHub README.md file have been created.

Customer_Behavior_Analysis_Documentation
 DOCX 
Open

README
 MD 
Open

File Highlights
1. Word Documentation (Customer_Behavior_Analysis_Documentation.docx)
Styling & Layout: Deep Navy (#1F4E78) header accents, clean typography (Calibri / Consolas), custom-styled table padding, alternating backgrounds, and formatted code boxes.

Content:

Executive Summary: Overview of the dataset (3,900 customer records, 18 features).

Data Pipeline & Preprocessing: Data profiling, column standardization, missing-value verifications, and age quantile binning (pd.qcut).

Data Dictionary & Schema Table: Descriptions, types, and primary key definitions for MySQL deployment.

10 Analytical SQL Queries: Includes business intent descriptions and SQL code blocks covering customer segmentation, revenue drivers, promo rates, window functions (ROW_NUMBER()), and cohort analytics.

2. GitHub README (README.md)
Badges & Visual Headers: Includes status shields (Python, Pandas, MySQL, Jupyter, License).

Project Architecture: Clean repository structure diagram.

Schema Summary Table: Markdown table mapping dataset columns to descriptions.

Analytical Queries Overview: Concise explanations of all 10 analytical questions.

Setup & Installation Instructions: Commands for setting up a virtual environment, installing dependencies, and running the SQL script in MySQL Workbench.