mini_capstone_orders.csv (Week 8 worked example)

- 358 rows. One row is one completed order at Sunrise Stores.
- Columns: order_id, order_date, weekday, is_weekend, channel, city,
  segment, n_items, revenue.
- Dates run from January to October 2026.
- is_weekend is 1 for Saturday and Sunday, 0 otherwise.
- Load with pd.read_csv("mini_capstone_orders.csv") from the same folder
  as the notebook.

This table is a teaching extract of completed orders from the Week 6
Sunrise Stores database. It is already aggregated to order grain, so you
should not join it back to line items unless you have a reason and you
check the counts.
