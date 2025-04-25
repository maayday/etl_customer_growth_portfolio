from db import get_connection
conn = get_connection()

import logging
from datetime import datetime
import pandas as pd
from db import get_connection

# Create timestamp for filenames/logs
today = datetime.now().strftime("%Y-%m-%d")

# Setup logging
log_path = f"../logs/customer_growth_{today}.log"
logging.basicConfig(
    filename=log_path,
    level=logging.INFO,
    format="%(asctime)s - %(levelname)s - %(message)s"
)

logging.info("🚀 ETL Job Started")

# Connect to DB
conn = get_connection()
cur = conn.cursor()
# Convert query results to DataFrame
query = """
SELECT 
    TO_CHAR(first_order_date, 'YYYY-MM') AS join_month,
    COUNT(*) AS new_customers
FROM (
    SELECT 
        customer_id,
        MIN(order_date) AS first_order_date
    FROM orders
    GROUP BY customer_id
) AS sub
GROUP BY join_month
ORDER BY join_month;
"""

cur.execute(query)
rows = cur.fetchall()

df = pd.DataFrame(rows, columns=["join_month", "new_customers"])
logging.info(f"📈 Loaded {len(df)} rows into DataFrame")

# Save to timestamped CSV
csv_path = f"../data/customer_growth_{today}.csv"
df.to_csv(csv_path, index=False)
logging.info(f"📦 Data exported to {csv_path}")

# 1. Imports and Logging Setup ✅
# 2. Connect to DB ✅
# 3. Execute Query and Fetch Results
# 4. Convert to DataFrame
# 5. Export CSV (you’re here now)
# 6. (Optional) Insert into PostgreSQL table
# 7. Close Connection and Log completion
