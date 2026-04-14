
# Zepto Inventory Analysis using PostgreSQL

## Overview
This project analyzes a Zepto product dataset using **PostgreSQL**. The dataset was taken from **Kaggle**, imported into PostgreSQL, cleaned using SQL, and analyzed through business-focused queries.

The goal of this project was to explore product inventory, pricing, discounts, stock availability, and category-level patterns to generate useful business insights.

This project demonstrates practical SQL skills in:
- database creation
- data cleaning
- exploratory data analysis
- business insight generation
- writing analytical SQL queries

---

## Project Objective
The main objective of this project is to use SQL to answer business questions such as:
- which products offer the best discounts
- which expensive products are out of stock
- which categories generate the highest estimated revenue
- which categories offer the highest average discount
- how pricing changes with product weight
- how inventory is distributed across categories

---

## Dataset
- **Source:** Kaggle
- **Domain:** Grocery / quick commerce / retail inventory
- **Database Used:** PostgreSQL

The dataset contains product-level information such as:
- SKU ID
- Category
- Product name
- MRP
- Discount percentage
- Available quantity
- Discounted selling price
- Weight in grams
- Stock availability
- Quantity

---

## Tools Used
- **PostgreSQL** – database creation, cleaning, and analysis
- **SQL** – querying, transformations, and business insight generation
- **Kaggle** – dataset source

---

## Database Schema
The dataset was imported into a PostgreSQL table named `zepto`.

### Table structure:
- `sku_id`
- `category`
- `name`
- `mrp`
- `discountPercent`
- `availableQuantity`
- `discountedSellingPrice`
- `weightInGms`
- `outOfStock`
- `quantity`

---

## Data Cleaning
After importing the dataset into PostgreSQL, data cleaning was performed to improve analysis quality.

### Cleaning steps performed:
- checked total row count
- reviewed sample records
- identified null values across important columns
- checked duplicate product names
- identified products with zero MRP or zero selling price
- removed invalid rows where `mrp = 0`
- converted price values from **paise to rupees**

### Example cleaning actions:
- deleted products with invalid MRP
- updated `mrp` and `discountedSellingPrice` by dividing by 100

This helped make the dataset more accurate and analysis-ready.

---

## Exploratory Data Analysis
Initial SQL exploration was performed to understand the data before deeper analysis.

### Exploration included:
- total number of rows
- sample product records
- null value detection
- unique product categories
- products in stock vs out of stock
- product names appearing multiple times

These checks helped in understanding the structure and quality of the dataset.

---

## Business Insight Queries
The main focus of the project was writing SQL queries to generate meaningful business insights.

### Key business questions answered:

#### 1. Top 10 best-value products by discount percentage
Identified products offering the highest discounts.

#### 2. High-MRP products that are out of stock
Found premium-priced products currently unavailable in inventory.

#### 3. Estimated revenue by category
Calculated category-wise revenue using:
`discountedSellingPrice × availableQuantity`

#### 4. Products with high MRP but low discount
Filtered products where:
- MRP > ₹500
- discount < 10%

This helps identify premium products with limited promotional pricing.

#### 5. Top 5 categories with the highest average discount
Measured which categories are most aggressively discounted.

#### 6. Price per gram analysis
Calculated price efficiency for products above 100 grams to identify better-value products.

#### 7. Product weight segmentation
Grouped products into:
- Low
- Medium
- Bulk

based on weight ranges.

#### 8. Total inventory weight by category
Calculated total stock weight available in each category.

---

## Key Insights
This project helps reveal useful retail and inventory insights such as:
- discount-heavy products and categories
- premium items currently unavailable
- categories with strong revenue potential
- better-value products based on unit weight
- inventory load by category
- pricing and stock trends across the catalog

These insights can support pricing decisions, stock planning, and category management.

---

## SQL Concepts Used
This project uses a range of SQL concepts, including:
- `CREATE TABLE`
- `SELECT`
- `WHERE`
- `ORDER BY`
- `GROUP BY`
- `HAVING`
- `DISTINCT`
- `CASE`
- `SUM`
- `AVG`
- `ROUND`
- `DELETE`
- `UPDATE`

---

