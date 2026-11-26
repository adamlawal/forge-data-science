Sunrise Stores data (Week 6)

sunrise_stores.db is the SQLite database used in both sessions and in the SQL Analytics Challenge.
The same tables are also saved as CSV files, if you want to peek with pd.read_csv.

Tables and grain
- customers.csv     one row per signed-up customer (80 rows)
- products.csv      one row per product on the shelf (31 rows)
- orders.csv        one row per basket / checkout (420 rows)
- order_items.csv   one row per line on an order (1,071 rows)
- payments.csv      one row per payment (379 rows). Cancelled orders have no payment.

Keys
- customers.customer_id  -> orders.customer_id
- products.product_id    -> order_items.product_id
- orders.order_id        -> order_items.order_id and payments.order_id

Useful values
- segment: New, Regular, Wholesale
- channel: Store, WhatsApp, Website
- status: Completed, Cancelled, Refunded
- payment method: Cash, Transfer, Card
- dates: signups from mid-2025 to mid-2026; orders from January to October 2026

Load in a notebook:

    import sqlite3
    import pandas as pd
    conn = sqlite3.connect("sunrise_stores.db")
    pd.read_sql("SELECT * FROM customers LIMIT 5;", conn)
