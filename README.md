# Food Delivery Application Database Design

## Overview
This database design supports a simple food delivery application. It includes tables for customers, stores, food items, transactions, and order items.

## Tables

### `customers`
- Stores customer details.
- Fields: `id`, `name`, `email`, `address`.

### `stores`
- Represents restaurants or stores in the system.
- Fields: `id`, `name`, `address`.

### `food_items`
- Lists food and beverage items available for order.
- Fields: `id`, `name`, `description`, `price`, `size`, `category`, `store_id`.

### `transactions`
- Records each order transaction.
- Fields: `id`, `customer_id`, `order_time`.

### `order_items`
- Maps multiple food items to a single transaction.
- Fields: `transaction_id`, `food_item_id`, `quantity`.

## SQL Files
- `schema.sql`: Contains SQL commands to create the database and tables.
- `seeding.sql`: Includes mock data to populate the tables for initial setup.

## Design Considerations
- The `transactions` table is designed to support multiple food items per order through the `order_items` table.
- The `food_items` table includes details like `description`, `size`, and `category` for a comprehensive listing.

