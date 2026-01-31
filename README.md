# Zepto-Data-Analytics--SQL-PROJECT
## Zepto Data Analytics

- The project analyzes a real Zepto e-commerce inventory dataset with **3,732 rows and 9 columns**.
  - Each row represents a **unique SKU**, not just a product name
  - This explains **1,681 unique product names** across 3.7k SKUs

- Stock status split shows:
  - About **3,200 SKUs in stock**
  - About **453 SKUs out of stock**
  - Helps flag immediate replenishment priorities and missed-revenue risks

- Data cleaning includes:
  - Removing **zero-MRP** records
  - Converting prices from **paise to rupees**
  - Fixing encoding issues by saving the CSV as **UTF-8** before importing into **PostgreSQL**

- Business queries:
  - Estimate **category-level revenue** using  
    `discounted selling price × available quantity`
  - Identify **high-MRP, low-discount** items
  - Rank **top discounted products** (many ≥ 50% off)
  - Support promotion and pricing strategy decisions

- Additional analyses:
  - Segment products by **weight bands** (low / medium / bulk)
  - Compute **price per gram** for items ≥ 100 g to assess value for money
  - List **duplicate product names** mapped to multiple SKUs due to pack size or category variations
