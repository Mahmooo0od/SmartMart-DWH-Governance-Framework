# SmartMart DWH Governance Framework

## 📌 Project Overview
This project demonstrates the implementation of **Data Governance** principles on an End-to-End Data Warehouse (SmartMart). It transitions a traditional ETL/BI stack into a governed, transparent, and trusted data ecosystem.

## 🏗️ Technical Stack
- **ETL:** SQL Server Integration Services (SSIS)
- **Data Warehouse:** SQL Server (Star Schema)
- **OLAP:** SQL Server Analysis Services (SSAS)
- **Reporting:** SQL Server Reporting Services (SSRS)
- **Dashboard:** Microsoft Power Bi Desktop

## ⚖️ Data Governance Pillars Applied

### 1. Business Glossary & Metadata Catalog
- Defined clear business definitions for technical entities (e.g., Defining "Active Customer" in `DimCustomer`).
- Categorized data into **Public, Internal, and Confidential** levels.

### 2. Automated Data Quality (DQ)
- Implemented a robust error-handling mechanism using `stg.RowErrors` to capture invalid records.
- Utilized `audit.ETL_Log` for full traceability of every ETL execution, ensuring data reliability.

### 3. Data Lineage
- Full mapping of data flow from Source Systems -> Staging -> DWH -> Semantic Layer -> Reports.
- Ensures clear visibility for impact analysis and troubleshooting.

## 📁 Repository Structure
- `/documentation`: Business Glossary and Lineage Maps.
- `/sql_scripts`: DWH Schema and DQ Rules.
- `/ssis_packages`: ETL logic with embedded DQ checks.
