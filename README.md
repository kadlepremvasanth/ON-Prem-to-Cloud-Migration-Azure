# ON-Prem to Cloud Migration – Azure Data Engineering Project

An end-to-end data engineering project that migrates on-premises and API data to Azure, transforms it using a Medallion Architecture, and deploys everything through a CI/CD pipeline with Git, GitHub, and Azure DevOps.

## What This Project Does

- Migrates data from on-prem SQL Server to Azure using Self-Hosted Integration Runtime
- Ingests data from REST APIs into Azure Data Lake Storage
- Loads data incrementally using watermark-based logic (no full reloads)
- Transforms raw data using PySpark Mapping Data Flows in Azure Data Factory
- Organizes data using a Medallion Architecture (Bronze → Silver → Gold) with Delta Lake
- Automates workflows and notifications using Azure Logic Apps
- Orchestrates pipelines using schedule, tumbling window, and event-based triggers
- Integrates with GitHub for version control (feature branch → pull request → merge)
- Deploys pipelines through Azure DevOps CI/CD

## Architecture

```
On-Prem SQL DB ──┐
                 ├──▶ Bronze (Raw) ──▶ Silver (Cleaned) ──▶ Gold (Delta Lake) ──▶ Azure SQL DB / Reporting
REST API ────────┘
```

- **Orchestration:** Azure Data Factory (pipelines + triggers)
- **Storage:** Azure Data Lake Storage Gen2
- **Transformation:** PySpark Mapping Data Flows
- **Automation:** Azure Logic Apps
- **CI/CD:** Git → GitHub → Azure DevOps

## Tech Stack

Azure Data Factory · PySpark · Azure Data Lake Storage Gen2 · Delta Lake · Azure SQL Database · Azure Logic Apps · Git · GitHub · Azure DevOps

## Repository Structure

```
ON-Prem-to-Cloud-Migration-Azure/
└── ADF/
    ├── pipeline/
    ├── dataset/
    ├── linkedService/
    ├── dataflow/
    └── trigger/
```
