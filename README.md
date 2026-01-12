# Warehouse Inventory Optimization Model 🏭

## 📌 Project Overview
This project demonstrates a **Warehouse Management System (WMS)** logic to optimize inventory levels. It uses **ABC Analysis** to categorize stock and monitors **Re-order Levels** to prevent stockouts.

## 📊 Methodologies Applied
* **ABC Analysis:** Classified items into Class A (High Value), B (Moderate), and C (Low Value).
* **Inventory Tracking:** Real-time monitoring of Stock-in vs. Stock-out.
* **Safety Stock Logic:** Automated alerts when inventory dips below the threshold.

## 🛠️ Tools
* **Data Management:** Structured CSV/SQL database for 500+ SKUs.
* **Analysis:** Excel-based logic for calculating Inventory Turnover Ratio.

## ⚙️ Logic Workflow
```mermaid
graph TD;
    A[New Stock Entry] --> B{Calculate Value};
    B -- High Value (70%) --> C[Class A: Strict Control];
    B -- Medium Value (20%) --> D[Class B: Monthly Review];
    B -- Low Value (10%) --> E[Class C: Bulk Order];
    C --> F[Set Low Safety Stock];
    E --> G[Set High Safety Stock];
