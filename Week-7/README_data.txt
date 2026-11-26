GreenLine Courier and used phones data (Week 7)

greenline_deliveries.csv
- 400 deliveries. One row is one drop.
- Features you may use when modelling: distance_km, package_kg, is_weekend,
  rain_mm, depart_hour, area, rider_experience_months.
- Targets: delivery_minutes (how long the drop took) and arrived_late (1 = late, 0 = on time).
- package_kg has 8 missing values. In class we filled them with the median (8.75).
- Do not use delivery_minutes as a feature when predicting arrived_late. That would leak the answer.
- About 25 percent of drops are late, so a model that always predicts "on time" is right
  about 75 percent of the time and never catches a late drop.

used_phones.csv (optional project dataset)
- 280 sold phones. One row is one handset.
- Columns: phone_id, brand, storage_gb, age_months, battery_health, condition,
  listed_price, sold_price, days_to_sell.
- Natural project questions: predict sold_price (regression) or days_to_sell (regression).
  You could also build a class, for example "sold in under 7 days", if you define it clearly
  and you do not use a column that already contains that answer.

Load either file with pd.read_csv in the same folder as your notebook.
