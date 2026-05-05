<h1 align="center">☁️ AWS Serverless Data Pipeline – Online Orders Processing</h1>

<h3 align="center">
Serverless Architecture | AWS Lambda | S3 | Glue | Athena | CloudWatch
</h3>

<p align="center"><em>"Building a scalable, cost-efficient serverless pipeline for processing and analyzing online order data."</em></p>

---

## ✨ Overview

This project demonstrates a **serverless data pipeline on AWS** that processes online order data in real time.

It uses AWS services to **ingest, clean, catalog, and analyze data** without managing servers, showcasing modern **cloud data engineering practices**.

---

## 🚀 Key Features

- ☁️ Fully serverless architecture  
- 📥 Automated data ingestion using S3 triggers  
- ⚙️ Data cleaning using AWS Lambda  
- 📊 Data cataloging with AWS Glue  
- 🔍 SQL-based querying using Amazon Athena  
- 📈 Monitoring using CloudWatch logs  

---

## 🧠 Tech Stack

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white)
![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white)
![Glue](https://img.shields.io/badge/Glue-FF9900?style=for-the-badge)
![Athena](https://img.shields.io/badge/Athena-232F3E?style=for-the-badge)
![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=for-the-badge)

---

## 📂 Architecture
- S3 (raw/) → Lambda → S3 (processed/)
↓
Glue
↓
Athena
↓
CloudWatch


---

## 🔍 Pipeline Workflow

1. Upload raw order data (`orders.csv`) to S3  
2. S3 event triggers AWS Lambda  
3. Lambda filters outdated `pending` and `cancelled` orders  
4. Cleaned data is stored in S3 (`processed/`)  
5. AWS Glue crawler catalogs the dataset  
6. Athena queries the cleaned data using SQL  
7. CloudWatch monitors execution logs  

---

## 📊 Dataset Overview

| Field | Description |
|------|------------|
| OrderID | Unique order identifier |
| Customer | Customer name |
| Amount | Order value |
| Status | Order status (confirmed, shipped, pending, cancelled) |
| OrderDate | Date of order |

---

## ⚙️ How to Run

### 1. Upload dataset
```bash
Upload `orders.csv` to S3 → `raw/` folder  
```
### 2. Trigger pipeline
```bash
S3 automatically triggers Lambda  
```

### 3. Run Glue crawler
```bash
Create table from processed data  
```

### 4. Query using Athena
```sql
SELECT *
FROM orders_processed
LIMIT 10;
```
---

### 📌 Project Highlights
- Built a serverless data pipeline using AWS
- Automated data processing using Lambda triggers
- Applied real-world ETL pipeline design
- Enabled SQL-based analytics with Athena
- Implemented monitoring using CloudWatch
