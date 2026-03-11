# instacart-data-mining-snacks

# Instacart Data Mining – Snacks Department (COMP 541)

## Overview
This repository contains our semester-long **COMP 541 Data Mining** group project using the **Instacart Market Basket Analysis** dataset.  
We were assigned the **Snacks department**, and our goal is to discover interesting insights about snack products and customer ordering behavior using:
- basic statistics + visualizations
- (later) **frequent pattern mining / association rules** (Apriori or FP-Growth)

**Department Focus:** Snacks

---

## Dataset
We use the Instacart dataset tables:
- `departments.csv` — department IDs and names
- `aisles.csv` — aisle IDs and names
- `products.csv` — product names with aisle/department IDs
- `orders.csv` — order timing info (day of week, hour of day, etc.)
- `order_products__train.csv` — which products were included in each order

> Note: For our analysis we use `order_products__train.csv` as the order-product mapping table for this project work.

---

## Project Goal
We act as data analysts at Instacart. Our job is to mine and uncover **interesting insights** related to the Snacks department, including:
- product distribution across aisles
- product popularity
- when snacks are purchased (time patterns)
- (later) association rules that reveal meaningful product combinations, ideally including **cross-department** insights

---

## Progress Report (Current Status)
We have completed the following analyses so far:

### 1) Dataset Loading & Preview
- Mounted Google Drive in Colab
- Loaded all required CSV files into pandas DataFrames
- Previewed each dataset with `.head()` to verify correct loading

### 2) Snacks Department Size
- Confirmed the Snacks department is represented by `department_id = 19`
- Counted the number of snack products in `products.csv`  
  **Result:** 6,264 snack products

### 3) Snack Products by Aisle
- Merged snack products with aisle names
- Counted snack products per aisle
- Created a bar chart for the top aisles

**Example top aisles (by number of snack products):**
- candy chocolate
- chips pretzels
- cookies cakes
- energy granola bars
- crackers

### 4) Commonly Bought Snack Products (Early Popularity Check)
- Merged `order_products__train.csv` with snack products
- Found the most frequently appearing snack products in orders (Top 10) with counts  
  Example products include:
- Lightly Salted Baked Snap Pea Crisps
- Pretzel Crisps Original Deli Style Pretzel Crackers
- Sea Salt Pita Chips
- Original Veggie Straws
- Organic Tortilla Chips

---

## Next Steps (Planned Work)
### A) Additional Statistical Analyses + Visualizations
We plan to analyze:
- **Snack purchasing by hour of day**
- **Snack purchasing by day of week**
- Additional charts to compare snack order timing vs overall orders

### B) Frequent Pattern Mining / Association Rules (Later Phase)
We will perform market basket analysis using:
- **Apriori** or **FP-Growth**
- Generate association rules with support and confidence values
- Select reasonable thresholds and explain the choice

We aim to go beyond basic “within-snacks” rules by exploring:
- **cross-department** combinations (e.g., snacks + beverages)
- multi-level patterns (department → aisle → product)
- rare but meaningful patterns

---