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

