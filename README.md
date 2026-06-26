# Olist Business Health Tracker

An end-to-end business diagnostics and operational analytics project built on the Olist Brazilian E-Commerce dataset. The project combines Python, MySQL, and Streamlit to identify operational inefficiencies that negatively impact profitability and customer experience.

---

## Project Overview

**Project Type:** End-to-End Business Analytics Project

**Technology Stack**

* Python
* Pandas & NumPy
* MySQL
* Streamlit
* Plotly

**Dataset**

Brazilian E-Commerce Public Dataset (Olist)

* ~100,000 Orders
* 9 Relational Tables
* Marketplace containing customers, sellers, products, logistics, reviews, and payments

---

## Business Problem

Revenue growth alone does not guarantee business growth.

Large e-commerce platforms often experience declining profit margins despite increasing sales due to hidden operational inefficiencies such as delayed deliveries, cancelled orders, poor seller performance, and excessive logistics costs.

The objective of this project is to identify these hidden operational issues, quantify their financial impact, and provide data-driven recommendations to improve profitability.

---

## Project Objectives

* Analyze the operational health of the marketplace
* Identify major sources of revenue leakage
* Measure seller operational risk
* Evaluate delivery performance across regions
* Monitor product category performance
* Quantify financial impact of operational failures
* Provide actionable business recommendations

---

## Dataset

Source:
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

The dataset consists of nine relational tables containing:

* Orders
* Order Items
* Payments
* Reviews
* Customers
* Sellers
* Products
* Geolocation
* Product Category Translation

The relational nature of the dataset enables realistic SQL joins and business analytics similar to production environments.

---

## Technology Stack

### Python

Used for:

* Data Cleaning
* Missing Value Handling
* Feature Engineering
* Data Validation
* Master Table Creation
* Exploratory Data Analysis

### MySQL

Used for:

* Data Storage
* SQL Joins
* KPI Calculations
* Business Queries
* SQL Views
* Window Functions
* Performance Optimization using Indexes

### Streamlit

Used to build an interactive business dashboard for executives and business stakeholders.

---

## Project Workflow

```text
Raw Kaggle Dataset
        │
        ▼
Python
• Data Cleaning
• Feature Engineering
• Validation
        │
        ▼
Master Dataset
        │
        ▼
MySQL
• Business Queries
• KPI Views
• Seller Risk Analysis
• Revenue Leakage Analysis
        │
        ▼
Streamlit Dashboard
```

---

## Feature Engineering

Several business-focused features were created before loading data into MySQL.

| Feature               | Purpose                           |
| --------------------- | --------------------------------- |
| is_late_delivery      | Delivery performance indicator    |
| delivery_delay_days   | Measures delivery delay severity  |
| actual_delivery_days  | End-to-end fulfillment time       |
| order_ym              | Monthly trend analysis            |
| total_item_value      | True item value including freight |
| freight_ratio         | Margin pressure indicator         |
| is_bad_review         | Customer dissatisfaction flag     |
| high_installment_flag | Financial stress indicator        |

---

## SQL Views

Reusable SQL views were created for dashboard generation.

* Monthly Revenue Performance
* Seller Performance Scorecard
* Delivery Intelligence
* Category Health
* Revenue Leakage Summary

---

## Dashboard Modules

### 1. Business Overview

Provides a high-level snapshot of marketplace performance through revenue, orders, customer ratings, delivery performance, and monthly trends.

---

### 2. Seller Risk Analysis

Evaluates every seller using a custom operational risk score derived from late delivery rate and bad review rate.

Highlights:

* High-risk sellers
* Revenue handled by risky sellers
* Regional seller risk distribution
* Seller ranking using SQL Window Functions

---

### 3. Delivery Intelligence

Analyzes logistics performance and its impact on customer satisfaction.

Highlights:

* Late vs On-Time deliveries
* Review score comparison
* State-wise delivery performance
* Revenue at risk due to delivery delays

---

### 4. Category Performance

Identifies product categories affecting profitability through high freight costs and poor customer satisfaction.

Highlights:

* High complaint categories
* Freight cost analysis
* Category profitability
* Customer experience metrics

---

### 5. Revenue Leakage Summary

Consolidates major operational losses into a single executive view.

Revenue leakage sources include:

* High Freight Cost
* Cancelled Orders
* Delivery Delay Impact

---

## Key Business Insights

* Operational issues remained hidden despite increasing revenue.
* High-risk sellers handled a significant portion of marketplace revenue.
* Late deliveries were strongly associated with poor customer ratings.
* High freight costs significantly reduced product margins.
* A small number of categories generated disproportionate customer complaints.

---

## Business Recommendations

* Introduce automated seller governance for high-risk vendors.
* Optimize logistics partnerships in high-delay regions.
* Reduce freight margin drain through pricing and fulfillment optimization.
* Implement proactive customer support for delayed orders.
* Monitor operational KPIs continuously using the dashboard.



---

## Skills Demonstrated

* Data Cleaning
* Feature Engineering
* Exploratory Data Analysis
* SQL Joins
* Window Functions
* View Creation
* Indexing
* Business KPI Design
* Dashboard Development
* Business Storytelling
* Operational Analytics

---

## Future Improvements

* Integrate Generative AI for natural language business insights.
* Build an AI assistant capable of answering business questions using SQL.
* Deploy on Streamlit Cloud with cloud-hosted database.
* Add predictive models for seller risk and customer churn.

##
