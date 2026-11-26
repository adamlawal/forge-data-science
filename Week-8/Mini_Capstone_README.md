# Weekend orders at Sunrise Stores

Should Sunrise Stores add extra Saturday staff, on the assumption that
weekend orders bring in more money than weekday orders?

## Problem

The shop is considering extra Saturday staff. That decision would be easier
if weekend baskets were larger than weekday baskets. This short project
tests that assumption on completed orders. It cannot, on its own, decide
the hiring question, because we do not have staffing cost or footfall data.

## How to run this work

The walk-through lives in `Week8_Session1_Capstone_Studio.ipynb`, in the
same folder as `mini_capstone_orders.csv`. Open that folder, then run the
notebook from top to bottom.

Packages used: pandas, matplotlib.

## Data

- Source: completed orders from the Sunrise Stores teaching database
  (the same shop used in Week 6), aggregated to one row per completed order.
- Grain: one completed order.
- Time window and size: January to October 2026, 358 orders.
- Cleaning: the table arrives with no missing values. Cancelled and
  refunded baskets are already out of this file, which matters if someone
  wants to talk about attempted sales rather than kept sales.

## Findings

1. Weekend orders are 101 of 358 completed orders, or 28.2 percent, close
   to two days in seven. This is not a weekend surge in order count.
2. Mean completed-order revenue is about 37,198 on weekends and about
   48,240 on weekdays. The median gap points the same way (19,600 against
   26,100). Sunday is the softest day; Monday is the strongest.
3. Wholesale orders are a little more common on weekdays and have a higher
   weekday average, so they widen the gap. After removing wholesale,
   weekend orders are still smaller on average (about 14,771 against 17,185).

## Recommendation

Do not add Saturday staff on the belief that weekend baskets are larger.
They are not, in this window. If the shop still wants to change weekend
staffing, it needs a different reason, and it needs cost and footfall
data that this table does not have.

## Limitations and future work

This is one shop and ten months of completed orders only. We cannot see
staff hours, wages, or footfall, and we cannot see cancelled baskets in
this file. Segment mix is a confounder; a simple split is not a formal
test. Average revenue per order is not the same as profit.

A useful next step would be to bring in staffing hours and cost, look at
busy hours inside each day, and, if useful, test whether the
weekend-weekday difference still stands after a simple statistical check.
