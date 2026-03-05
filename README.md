# E-Commerce Database Schema Documentation

## Overview
This documentation provides a comprehensive guide to the e-commerce database schema used in the `E---Com-DB` project. The schema is designed to efficiently manage and store data relevant to an e-commerce platform, covering all aspects from product management to user transactions.

## Schema Structure
The schema consists of the following main entities:

1. **Users**  
   - `user_id` (Primary Key, INT)  
   - `username` (VARCHAR)  
   - `email` (VARCHAR)  
   - `password_hash` (VARCHAR)  
   - `created_at` (DATETIME)  

2. **Products**  
   - `product_id` (Primary Key, INT)  
   - `name` (VARCHAR)  
   - `description` (TEXT)  
   - `price` (DECIMAL)  
   - `stock_quantity` (INT)  
   - `created_at` (DATETIME)  

3. **Categories**  
   - `category_id` (Primary Key, INT)  
   - `category_name` (VARCHAR)  
   - `created_at` (DATETIME)  

4. **Orders**  
   - `order_id` (Primary Key, INT)  
   - `user_id` (Foreign Key, INT)  
   - `order_date` (DATETIME)  
   - `status` (VARCHAR)  

5. **Order_Items**  
   - `order_item_id` (Primary Key, INT)  
   - `order_id` (Foreign Key, INT)  
   - `product_id` (Foreign Key, INT)  
   - `quantity` (INT)  

## Relationships  
- **Users** can place multiple **Orders**.  
- **Orders** can have multiple **Order_Items**, each referring to a **Product**.  
- **Products** can belong to one or more **Categories**.  

## Data Flow
1. Users register and log in to the platform.  
2. Users can browse products, and products are categorized for easy navigation.  
3. Users place orders, and details are recorded in the **Orders** and **Order_Items** tables.

## Conclusion
The e-commerce database schema is designed for scalability and flexibility, allowing for future enhancements as the platform grows. Please refer to this document as a guide for understanding the underlying structure of the database.
