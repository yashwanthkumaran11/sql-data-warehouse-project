# SQL Data Warehouse Project

## 📌 Project Overview

This project demonstrates the development of an end-to-end SQL Data Warehouse using SQL Server.

The project focuses on transforming raw CRM and ERP source data into a structured, clean, and business-ready data warehouse using a Medallion Architecture.

The warehouse is organized into three layers:

- 🟤 Bronze Layer — Raw source data
- ⚪ Silver Layer — Cleaned and standardized data
- 🟡 Gold Layer — Business-ready data

---

## 🏗️ Data Warehouse Architecture

The project follows a Medallion Architecture with three layers.

### 🟤 Bronze Layer

- Raw, unprocessed source data
- Source-aligned tables
- Full-load processing
- DDL and load scripts
- Stored procedures
- Data validation and documentation

### ⚪ Silver Layer

- Cleaned and standardized data
- Data cleansing and normalization
- Derived columns
- Data enrichment
- Data quality checks
- Stored procedures and load scripts

### 🟡 Gold Layer

- Business-ready data
- Data integration and aggregations
- Business rules and logic
- Star-schema-based data model
- Dimension and fact tables
- Data catalog and documentation

---

## 🔄 Source Systems

The project works with two source systems:

### CRM

Customer Relationship Management data containing:

- Customer information
- Product information
- Sales transaction data

### ERP

Enterprise Resource Planning data containing:

- Customer information
- Customer location
- Product category information

The CRM and ERP data are integrated through the Bronze, Silver, and Gold layers.

---

## 🔄 Data Flow

The data flows through the warehouse as:

**CRM / ERP → Bronze Layer → Silver Layer → Gold Layer → Analytics & Reporting**

The Gold layer contains:

- `gold.fact_sales`
- `gold.dim_customers`
- `gold.dim_products`

---

## 🔗 Data Integration

CRM and ERP data are integrated to build a unified analytical data model.

The integration includes:

- Customer information
- Product information
- Product categories
- Customer location
- Sales transactions

This integration supports the creation of the Gold-layer fact and dimension tables.

---

## ⭐ Data Modeling

A Gold-layer Star Schema was designed for analytical use cases.

### Fact Table

`gold.fact_sales`

Contains sales-related measures and keys such as:

- `order_number`
- `product_key`
- `customer_key`
- `order_date`
- `shipping_date`
- `due_date`
- `sales_amount`
- `quantity`
- `price`

### Customer Dimension

`gold.dim_customers`

Contains customer-related attributes such as:

- `customer_key`
- `customer_id`
- `customer_number`
- `first_name`
- `last_name`
- `country`
- `marital_status`
- `gender`
- `birthdate`

### Product Dimension

`gold.dim_products`

Contains product-related attributes such as:

- `product_key`
- `product_id`
- `product_number`
- `product_name`
- `category_id`
- `category`
- `subcategory`
- `maintenance`
- `cost`
- `product_line`
- `start_date`

---

## 🔧 ETL Process

The project covers the ETL process — Extract, Transform and Load.

### Extract

- Data extraction from CRM and ERP source files
- Source data analysis
- Data ingestion into the Bronze layer

### Transform

- Data cleansing
- Data standardization
- Data normalization
- Derived columns
- Data enrichment
- Data integration
- Data aggregation
- Business rules and logic

### Load

- Full-load processing
- Truncate and insert
- Stored procedures
- Loading data across Bronze and Silver layers

---

## ✅ Data Validation

Validation was performed across the different layers to check:

- Data completeness
- Schema consistency
- Data correctness
- Data integration
- Data quality

---

## 📚 Documentation

The project includes documentation for:

- Data Architecture
- Data Flow
- Data Integration
- Data Layers
- Data Model
- ETL
- Data Catalog
- Naming Conventions
- Project Documentation

---

## 📁 Project Structure

```text
sql-data-warehouse-project/
│
├── datasets/
│
├── docs/
│   ├── data_architecture
│   ├── data_catalog
│   ├── data_flow
│   ├── data_integration
│   ├── data_layers
│   ├── data_model
│   ├── ETL
│   └── naming_conventions
│
├── scripts/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── tests/
│
├── README.md
└── LICENSE
