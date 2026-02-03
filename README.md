# Workflow XML Data Pipeline (Databricks + AWS + Tableau)

## Overview
This project implements an end-to-end data pipeline that ingests XML workflow files,
normalizes them into relational tables, aggregates metrics, and visualizes results
using Tableau.

## Architecture
XML → Databricks (Bronze) → Silver (Normalized Tables) → Gold (Aggregations)
→ AWS RDS (PostgreSQL) → Tableau Dashboard

## Tech Stack
- Databricks (PySpark, SQL)
- AWS RDS (PostgreSQL)
- Tableau Desktop
- GitHub

## Data Model
Silver tables:
- workflow
- wfdoc
- wfsupersededdoc
- wfroles
- wftaskresults

Gold tables:
- workflow_summary

## Key Metrics
- Workflows over time
- Documents per workflow
- Approval workload by role
- Task duration per workflow

## Tableau Dashboard
Link: <TABLEAU PUBLIC URL HERE>

## Notes
- Secrets managed via Databricks secrets / environment variables
- Incremental MERGE logic used in Silver layer
