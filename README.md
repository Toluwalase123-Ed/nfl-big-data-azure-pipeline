# NFL Big Data Analytics Pipeline on Microsoft Azure

This project demonstrates a scalable, cloud-native big data architecture built on **Microsoft Azure**, designed to ingest, process, and analyze NFL player tracking data from the **NFL Big Data Bowl 2023**. The solution uses Python and Azure-native services to derive actionable football insights while operating within the limitations of an Azure for Students subscription.

## 📊 Project Overview

- **Dataset**: [NFL Big Data Bowl 2023](https://www.kaggle.com/competitions/nfl-big-data-bowl-2023/data) (Player tracking, plays, games, scouting)
- **Cloud Platform**: Microsoft Azure
- **Goal**: Create an end-to-end analytics pipeline from data ingestion to predictive modeling

## 🧱 Architecture Components

| Layer        | Tools & Services                            |
|--------------|---------------------------------------------|
| Storage      | Azure Blob Storage (ADLS Gen2)              |
| Ingestion    | Python (Jupyter Notebook), azure-storage-blob |
| Processing   | Azure Synapse Analytics, Pandas, PySpark    |
| Orchestration| Azure Data Factory, Azure Functions         |
| Modeling     | scikit-learn (Logistic Regression)          |
| Visualization| Power BI, Jupyter (matplotlib/seaborn)      |

## ⚙️ Workflow

1. **Ingest NFL CSV data** from Kaggle into Azure Blob Storage
2. **Preprocess and clean** the dataset using Pandas in Jupyter Notebooks
3. **Convert to Parquet** for optimized querying
4. **Analyze play-level data** using Azure Synapse SQL and notebooks
5. **Build a ML model** to predict pass-play probability
6. **Visualize insights** for coaching and scouting decisions

## 🧠 Key Insights

- Created a logistic regression model to predict passing plays with **ROC-AUC ~0.81**
- Identified team-specific offensive tendencies using model coefficients
- Reduced storage and query costs with Parquet + partitioning

## 💰 Cost Optimization

- Used Azure for Students credit ($100/month)
- Serverless SQL for ad-hoc querying (Synapse)
- Blob storage lifecycle rules to reduce long-term storage costs
- Auto-pausing notebooks to avoid idle compute billing

## 🔒 Security & Compliance

- TLS 1.2 enforced for all data in transit
- AES-256 encryption at rest
- Role-based access via Azure AD
- GDPR & CCPA considerations for player tracking data

## 📈 Performance Monitoring

- Real-time KPIs tracked using Azure Monitor & Log Analytics
- Auto-shutdown rules and alerts for efficient resource use

## 📂 Project Structure

nfl-big-data-azure-pipeline/
│
├── notebooks/ # Jupyter notebooks for ingestion, processing, and modeling
├── scripts/ # Python helper scripts
├── data/ # Sample dataset (if included)
├── visualizations/ # Graphs, charts, Power BI dashboards
├── report/ # Full project report (TOLU.docx or PDF)
└── README.md # Project overview and instructions


## 📌 Requirements

- Azure subscription (Azure for Students)
- Python 3.9+
- Jupyter Notebook
- Required packages: `pandas`, `azure-storage-blob`, `scikit-learn`, `pyarrow`

## 🧪 Run Locally

Clone the repo and run the notebook:

```bash
git clone https://github.com/yourusername/nfl-big-data-azure-pipeline.git
cd nfl-big-data-azure-pipeline
jupyter notebook

Contact
Toluwalase Paul Edgal
📧 laseedgal@gmail.com
📍 London, UK
