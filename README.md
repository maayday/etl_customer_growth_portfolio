# 📈 ETL Pipeline: Monthly Customer Growth (Northwind Dataset)

This project demonstrates a full ETL pipeline built with Python and PostgreSQL.  
It extracts customer order data from a PostgreSQL database, transforms it into monthly customer growth metrics, and loads it into a summary table and timestamped CSV for further analysis or reporting.

---

## 🔧 Tech Stack

- **Python**: Data extraction, transformation, loading
- **PostgreSQL**: Data storage and querying
- **Pandas**: Data manipulation
- **Matplotlib**: Visualization
- **Logging**: Process tracking
- **Virtualenv**: Environment isolation

---

## 💡 Features

- 🗂️ Modular PostgreSQL connection via `db.py`
- 📦 Exports data to date-stamped CSVs
- 🧾 Logs all ETL steps with timestamps
- 🛠 Creates `monthly_customer_growth` table if missing
- 📈 Visualizes customer growth trends using Jupyter + Matplotlib

---

## 📁 Project Structure

etl_customer_growth_portfolio/ ├── data/ # Output CSVs ├── logs/ # ETL logs ├── scripts/ # Core ETL scripts │ ├── db.py │ └── etl_customer_growth.py ├── notebooks/ # Jupyter notebooks for visualization │ └── visualize_customer_growth.ipynb ├── .gitignore ├── requirements.txt └── README.md


---

## 🚀 How to Run

### 1. Clone the Repo
```bash
git clone https://github.com/YOUR_USERNAME/etl_customer_growth_portfolio.git
cd etl_customer_growth_portfolio

2. Set Up Virtual Environment

python3 -m venv env
source env/bin/activate
pip install -r requirements.txt

3. Run the ETL Script
python scripts/etl_customer_growth.py


Output will be saved in:
data/customer_growth_<YYYY-MM-DD>.csv

logs/customer_growth_<YYYY-MM-DD>.log

PostgreSQL table: monthly_customer_growth


📊 Preview

Monthly customer growth trend plotted from ETL output.

🧠 Inspired by
Northwind PostgreSQL Dataset

Real-world data engineering workflows

📬 Contact
Mehdi Hindi – mehdi.hindi@gmail.com
GitHub: @maayday

✅ To Do
 Add revenue pipeline alongside customer growth

 Schedule ETL runs with cron

 Upload visualizations to a dashboard


---

### ✅ Next Steps

1. Save this as a file in your project:

```bash
cd etl_customer_growth_portfolio
touch README.md
