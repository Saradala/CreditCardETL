# Credit Card Fraud Detection Data Warehouse

A SQL Server data warehouse built for the IT3021 Data Warehousing and Business Intelligence module.

## Overview
Star schema dimensional model built on a 700,000-record credit card transaction dataset (2019).
Designed for fraud pattern analysis and OLAP reporting.

## Schema
- **FactTransaction** — one row per transaction (Amount, IsFraud, ProcessingTime)
- **DimDate** — calendar dimension with Year → Quarter → Month hierarchy
- **DimCardholder** — SCD Type 2 cardholder dimension
- **DimMerchant** — merchant and location data
- **DimCategory** — category with CategoryGroup hierarchy

## Stack
- SQL Server (data warehouse)
- SSIS (ETL — two packages: initial load + accumulating fact update)
- Visual Studio (SSDT)

## Data Source
Kaggle Credit Card Fraud Detection dataset (~700k transactions, 2019)
