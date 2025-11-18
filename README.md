# E-Commerce-Power-BI-Analytics-2020-2022-

🚀 Project Overview

This project analyzes e-commerce data from 2020–2022, covering Orders, Customers, Products, Categories, Subcategories, and Returns.
The goal is to build an end-to-end BI system that helps understand sales trends, customer behavior, product performance, profitability, and regional patterns.

🎯 Objectives

Integrate and clean multi-year sales data.

Build a star-schema data model using PK–FK relationships.

Create DAX measures for analytical insights.

Design multiple interactive dashboards in Power BI.

Generate actionable insights for business decision-making.

📂 Dataset Structure

The project uses the following tables:

Customers — customer details

Orders — transaction information

Sales (2020–2022) — merged sales dataset

Products — product descriptions & pricing

Categories & Subcategories — classification hierarchy

Returns — returned order records

Date Table — for DAX time intelligence

🛠 ETL Workflow
1️⃣ Extract

Imported all raw tables into Power BI

Merged multi-year sales files into one dataset

2️⃣ Transform

Cleaned missing values, duplicates

Standardized product/category mapping

Created calculated columns (Profit, Return Flag, etc.)

Formatted and validated all data types

3️⃣ Load

Loaded cleaned tables into the Power BI model

📐 Data Modeling

Designed a Star Schema Model consisting of:

Fact Table

Fact_Sales

Dimension Tables

Dim_Customer

Dim_Product

Dim_Category

Dim_Subcategory

Dim_Date

Relationships

CustomerID → Customers

ProductID → Products

CategoryID → Categories

SubCategoryID → Subcategories

OrderDate → Date Table

🧮 Key DAX Measures

Total Sales

Total Customers

Profit %

Return %

YOY Growth

Sales by Category/Subcategory

Average Order Value (AOV)

Returning Customer Rate

📊 Dashboards Included
📌 1. Index Dashboard

Navigation to all dashboards

Quick project overview

📊 2. Executive Dashboard

KPIs: Sales, Profit %, Return %, Customers

YOY trend analysis

Category revenue share

🗺 3. Map Dashboard

Region-wise sales

Return % by area

👥 4. Customer Dashboard

New vs Returning customers

Revenue by customer profile

Top 10 customers

📦 5. Product Dashboard

Best & least selling products

Profit %, Return %

Category & subcategory breakdown

🔍 Key Insights

Identified high-performing and low-performing regions

Found categories with highest sales & highest return rates

Detected product lines with best profitability

Discovered strong customer retention patterns

Understood seasonal demand cycles



Product Dashboard

Index Dashboard
