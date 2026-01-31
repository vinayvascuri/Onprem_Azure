# Onprem_Azure
OnPrem_Azure-Data-Migration-Project


Here is a professional, high-impact README.md file designed for your GitHub repository. It combines your technical steps with the evidence from your screenshots to showcase your competency to recruiters.

Hybrid Data Migration: On-Premise SQL Server to Azure Cloud
📌 Project Overview
Developed a secure, end-to-end data migration pipeline using Azure Data Factory (ADF) to replicate an enterprise-level cloud adoption workflow. The project focuses on moving relational data from a local SQL Server environment to Azure Blob Storage, utilizing a Self-Hosted Integration Runtime (SHIR) to bridge the gap between on-premise infrastructure and the cloud.

🏗 Architecture
Source: On-Premise Microsoft SQL Server (Database: employee).

Gateway: Self-Hosted Integration Runtime (onprem-azure-ir).

Orchestrator: Azure Data Factory Pipeline (onprem_azure_pl).

Sink: Azure Blob Storage (Container: target).

🛠 Technical Implementation
1. Data Source Configuration
Created a local SQL database and an Employee1 table using T-SQL.

Populated the table with structured records including EmployeeId, Name, Gender, Salary, Department, and Experience.

Verified data integrity locally before initiating the migration.

2. Hybrid Connectivity (The Bridge)
Configured a Self-Hosted Integration Runtime on the local host to establish a secure outbound connection to Azure.

Implemented Authentication Keys to register the node and authorize data transit without exposing the local database to the public internet.

3. ETL Pipeline Development
Established Linked Services (onprem_azure_ls2) using SQL Authentication to securely access the source database.

Configured a Copy Data activity within ADF to map relational SQL tables to cloud-native storage.

Handled data serialization, converting SQL records into a delimited .txt format (dbo.Employee1.txt) for cloud compatibility.

📊 Results & Validation
Successful Execution: The pipeline completed successfully with a total duration of 22 seconds.

Verification: Confirmed that all records were accurately ingested into Azure Blob Storage by reviewing the output file schema and record count.
