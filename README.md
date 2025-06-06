# 🚀 Azure Data Factory ETL Pipeline: CSV to Azure SQL

This project demonstrates how to build a scalable ETL pipeline using **Azure Data Factory (ADF)**. Unstructured CSV files stored in **Azure Blob Storage** are ingested, transformed, and loaded into a structured format within an **Azure SQL Database**.

> 🔄 Fully automated data integration pipeline with GitHub version control and scheduled execution.

---

## 📽️ Demo Video

Watch the full walkthrough:  
[![Watch the video](https://github.com/Piyush972004/Azure-Data-Factory-CSV-to-Azure-SQL-ETL-Pipeline/blob/19e664b963e8166bfa1467d5ae4593dfb0d0738f/Screenshot%202025-05-25%20143000.png)](https://github.com/Piyush972004/Azure-Data-Factory-CSV-to-Azure-SQL-ETL-Pipeline/blob/49f95b4c938c526a2bcd5f8e3eeca35bf260d80e/Azure%20data%20factory%20pipline.mp4)
_(or open `/media/demo.mp4` in this repository)_

## 🔧 Technologies Used

- Azure Data Factory
- Azure Blob Storage
- Azure SQL Database
- GitHub Integration with ADF

## 📁 Repository Structure

- `pipelines/`: Contains ADF pipeline JSON definitions.
- `datasets/`: Contains dataset definitions for source (CSV) and sink (SQL).
- `linkedServices/`: Connection info for storage and database.
- `adf_publish/`: Auto-generated ARM templates for deployment.
- `media/`: Contains demo video and screenshots.

## ✅ Features

- CSV file ingestion from Azure Blob Storage
- Data transformation and mapping (via Copy Activity)
- Automated loading into Azure SQL Database
- Scheduled execution using triggers
- Version control with GitHub


---
## 📸 AZURE DATA FACTORY

![Screenshot](assets/Screenshot%202025-05-25%20143000.png)


## 📸 AZURE BLOB STORAGE

![Screenshot](assets/Screenshot%202025-05-25%20143930.png)


## 📸 AZURE SQL DATABASE

![Screenshot](assets/Screenshot%202025-05-25%20143941.png)

---

## 🧑‍💻 Step-by-Step Setup

### 🔧 Prerequisites
- Azure subscription
- Azure Blob Storage with CSV files uploaded
- Azure SQL Database with a pre-created table
- Azure Data Factory instance
- GitHub account

---

### ⚙️ 1. Create Azure Resources
- Create a **Blob Storage account** and upload your `.csv` files
- Create an **Azure SQL Database** and define your destination table:
```sql
CREATE TABLE SalesData (
    OrderID INT,
    CustomerName VARCHAR(100),
    ProductName VARCHAR(100),
    Quantity INT,
    Price DECIMAL(10, 2),
    OrderDate DATE
);
```


---
### 🧩 2. Set Up Azure Data Factory
a. Create Linked Services
- Azure Blob Storage: Connect via account key or managed identity

- Azure SQL Database: Provide connection string and credentials

b. Create Datasets
- Source Dataset: Delimited text (CSV), point to blob container

- Sink Dataset: Azure SQL Table

c. Create Pipeline
- Use Copy Data activity to transfer data from source to sink

- Optionally define column mappings and transformations

d. Schedule Execution
- Add a trigger (time-based or event-based) for automation
---



### 🔄 3. Integrate with GitHub
In ADF Studio, go to Manage > Git Configuration

Choose:

- Repository type: GitHub

- Repository: Your GitHub repo

- Collaboration branch: main

- Publish branch: adf_publish

- Commit and push your ADF objects to GitHub
---



## 🗂️ Setup Instructions

1. Clone this repository.
2. Deploy ADF ARM templates (or import manually in ADF Studio).
3. Configure your storage and SQL credentials.
4. Upload your own CSV files to test.

## 🚀 Deployment

You can deploy this pipeline using ADF's GitHub integration or Azure Resource Manager (ARM) templates provided in the `adf_publish` folder.

## 📄 License

This project is licensed under the MIT License. Feel free to reuse or modify.

---

