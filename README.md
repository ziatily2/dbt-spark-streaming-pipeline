# Streaming Lakehouse with PySpark & DBT (Bronze / Silver / Gold)

## Overview
This project implements a production-style lakehouse architecture using Spark Structured Streaming, PySpark, and DBT.  
It focuses on incremental ingestion, modular transformations, and dimensional modeling using a real-world Uber-like dataset.

The project is designed to demonstrate interview-relevant skills such as streaming ingestion, reusable PySpark design, and DBT-based star schema modeling.

---

## Dataset
The dataset simulates an Uber-like platform and includes:
- Customers
- Trips
- Drivers
- Vehicles
- Locations
- Payments

It is specifically chosen to demonstrate **dimensional data modeling**, including fact and dimension tables.

---

## Architecture
The solution follows a Medallion Architecture:

### Bronze Layer (Ingestion)
- Spark Structured Streaming for incremental ingestion
- Data loaded **as-is** to preserve source of truth
- Uses checkpointing to track processed files
- Trigger configured as `once=true` to optimize compute usage
- Databricks Free Edition used as execution environment

### Silver Layer (Transformations)
- Modular PySpark transformations
- Python classes used for reusable and testable logic
- Cleaned, standardized, and enriched datasets

### Gold Layer (Analytics)
- Star schema built using **DBT**
- Fact and dimension tables
- Incremental DBT models with upserts
- Slowly Changing Dimensions (SCD)

---

## Tech Stack
- Apache Spark (Structured Streaming)
- PySpark
- Delta Lake
- DBT
- Python
- Databricks Free Edition

---

## Key DBT Concepts Applied
- DBT models & sources
- Jinja templating
- Incremental models
- Ephemeral materializations
- DBT CLI
- SCD handling
- Fact & dimension table design

---

## Key Features
- Incremental streaming ingestion
- Reusable PySpark architecture
- Bronze/Silver/Gold separation
- Star schema modeling
- Production-oriented DBT workflows

---

## Why This Project Matters
This project reflects real-world data engineering practices used in production systems.  
It is highly relevant for:
- Data Engineer interviews
- Lakehouse architecture discussions
- Streaming and dimensional modeling use cases

---

## What I Learned
- Designing streaming-first lakehouse pipelines
- Writing production-ready PySpark code
- Implementing DBT for analytics engineering
- Applying dimensional modeling in real datasets
