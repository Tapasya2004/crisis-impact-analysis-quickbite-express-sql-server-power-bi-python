# QuickBite Data Dictionary

The source challenge package contains the following fact and dimension tables.

| Table | Key analytical fields |
|---|---|
| `fact_orders` | `order_id`, `customer_id`, `restaurant_id`, `delivery_partner_id`, `order_timestamp`, `subtotal_amount`, `discount_amount`, `delivery_fee`, `total_amount`, `is_cod`, `is_cancelled` |
| `fact_order_items` | `order_id`, `item_id`, `menu_item_id`, `restaurant_id`, `quantity`, `unit_price`, `item_discount`, `line_total` |
| `fact_ratings` | `order_id`, `customer_id`, `restaurant_id`, `rating`, `review_text`, `review_timestamp`, `sentiment_score` |
| `fact_delivery_performance` | `order_id`, `actual_delivery_time_mins`, `expected_delivery_time_mins`, `distance_km` |
| `dim_customer` | `customer_id`, `signup_date`, `city`, `acquisition_channel` |
| `dim_restaurant` | `restaurant_id`, `restaurant_name`, `city`, `cusini_type`, `partner_type`, `avg_prep_time`, `is_active` |
| `dim_delivery_partner` | `delivery_partner_id`, `partner_name`, `city`, `vehicle_type`, `employment`, `avg_rating`, `is_active` |
| `dim_menu_item` | `menu_item_id`, `restaurant_id`, `item_name`, `category`, `is_veg`, `price` |

## Analytical Outputs

The Power BI model also contains derived/calculated analytical structures such as:

- `calculated_customer`
- `calculated_restaurant`
- `high_value_customer`

The Python customer-intelligence workflow additionally produces a customer-level recommendation dataset containing segmentation, risk flags, recovery priority, priority band, and recommended action.
