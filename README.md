# E-Commerce-Power-BI-Analytics-2020-2022

# 📊 E-Commerce Business Intelligence Dashboard System (2020–2022)

## 📌 **Project Overview**

This project is an end-to-end **Business Intelligence solution** built using **Power BI**. It analyzes multi-year e-commerce data (2020–2022) covering customers, orders, products, categories, subcategories, and returns. The goal is to deliver actionable insights into sales performance, customer behavior, product profitability, and geographic trends.

---

## 🎯 **Objectives**

* Integrate and clean multi-year sales datasets.
* Create a robust star-schema data model using PK–FK relationships.
* Build DAX measures for advanced calculations.
* Develop interactive dashboards for business insights.
* Enable real-time decision-making through visual analytics.

---

## 📂 **Dataset Details**

The project uses the following tables:

* **Customers** – Customer information & demographics
* **Orders** – Order-level transaction data
* **Sales (2020–2022)** – Multi-year sales merged into one dataset
* **Products** – Product details and pricing
* **Categories & Subcategories** – Product classification
* **Returns** – Returned orders with return quantity
* **Date Table** (Created for DAX time intelligence)

---

## 🔄 **ETL Workflow**

### **1. Extract**

* Imported raw tables into Power BI.
* Combined yearly sales files into a single dataset.

### **2. Transform**

* Removed duplicates & missing values
* Standardized product/category mapping
* Created calculated columns for Profit, Return Flag, etc.
* Ensured consistent data types and formatting

### **3. Load**

* Loaded all cleaned tables into Power BI model view

---

## 🧩 **Data Modeling**

Below is the actual data model extracted from the Power BI Model View:

### **Tables Included in the Model**

* **SALES 2020–2022 (Fact Table)**
  Contains: CustomerKey, OrderDate, OrderNumber, OrderQuantity, ProductKey, QuantityType, Retail Price

* **Customer Lookup 2 (Dimension)**
  Contains: AnnualIncome, BirthDate, BirthYear, Child, Customer Priority, CustomerCity, EducationCategory, EmailAddress

* **Calendar Lookup (Dimension)**
  Contains: Date

* **Product Lookup (Dimension)**
  Contains: ModelName, PriceRanges, ProductColor, ProductDescription, ProductKey, ProductLine, ProductName, ProductSize

* **Product Categories Lookup (Dimension)**
  Contains: CategoryName, ProductCategoryKey

* **Product Subcategories Lookup (Dimension)**
  Contains: ProductCategoryKey, ProductSubcategoryKey, SubcategoryName

* **Returns Data (Fact Table)**
  Contains: ProductKey, ReturnDate, ReturnQuantity, TerritoryKey

* **Territory Lookup (Dimension)**
  Contains: Continent, Country, Region, SalesTerritoryKey

* **Customer Matric Selection (Helper Table)**
  Used for dynamic metrics and slicer-based analysis.

* **Measure Table**
  Contains all core DAX measures.

### **Relationship Structure (PK–FK)**

* SALES 2020–2022[CustomerKey] → Customer Lookup 2[CustomerKey]
* SALES 2020–2022[ProductKey] → Product Lookup[ProductKey]
* Product Lookup[ProductCategoryKey] → Product Categories Lookup[ProductCategoryKey]
* Product Lookup[ProductSubcategoryKey] → Product Subcategories Lookup[ProductSubcategoryKey]
* SALES 2020–2022[OrderDate] → Calendar Lookup[Date]
* Returns Data[ProductKey] → Product Lookup[ProductKey]
* Returns Data[TerritoryKey] → Territory Lookup[TerritoryKey]

This model supports a clean star-schema structure and improves reporting performance.

---**
A star schema model was designed:

* **Fact Table:** Fact_Sales
* **Dimension Tables:** Customers, Products, Categories, Subcategories, Date

### **Relationships (PK–FK)**

* CustomerID → Dim_Customer
* ProductID → Dim_Product
* CategoryID → Dim_Category
* SubCategoryID → Dim_Subcategory
* OrderDate → Date Table

This ensures efficient DAX performance and cleaner reporting.

---

## 📐 **Key DAX Measures**

Some of the major measures used:

* **Total Sales**
* **Total Customers**
* **Profit %**
* **Return %**
* **Year-over-Year Growth**
* **Sales by Category/Subcategory**
* **Average Order Value (AOV)**

---

## 📊 **Dashboards Included**

### **1. Index Dashboard**

* Navigation panel to access all dashboards
* Quick project overview

### **2. Executive Dashboard**

* KPIs: Total Sales, Profit %, Return %, Total Customers
* Sales trend visuals
* Category-level performance comparison

### **3. Map Dashboard**

* State/region-wise sales & return distribution
* High-performing vs low-performing regions

### **4. Customer Dashboard**

* New vs returning customers
* Customer segmentation
* Top customers by revenue

### **5. Product Dashboard**

* Best & least performing products
* Profit %, Return %, and revenue contribution
* Category & subcategory breakdown

---

## 🔍 **Key Insights Generated**

* Identified top-performing regions & sales hotspots
* Found high-return product categories
* Determined most profitable product lines
* Recognized customer buying patterns & retention rates
* Understood category-wise contribution to overall revenue

---

## 🛠 **Tech Stack Used**

* **Power BI** – Data model, DAX, dashboards
* **Excel** – Initial preprocessing
* **Power Query** – ETL operations

---


