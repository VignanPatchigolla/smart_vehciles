# 🚗 Smart Vehicles Data

## 📚 Project Overview
The **Smart Vehicles Data ** processes IoT data received daily in **AWS S3** in JSON format. This project validates incoming data, separates invalid records, and integrates the valid data into a **SQL Database** for further analysis by **Data Analysts (DA)** and **Data Scientists (DS)**.  

Invalid data is stored in a **rejected folder** within **Azure Data Lake Storage (ADLS)** for auditing, while valid data is sent to a **staging folder** in ADLS. This automated pipeline ensures seamless data validation and storage for downstream analytics and machine learning tasks.

---

## 🚀 Features
- **IoT Data Validation**: Identify and reject invalid JSON data (e.g., empty or malformed records).
- **Data Separation**: Store rejected data in ADLS and valid data in a staging area.
- **Automation**: Automatically trigger data pipelines upon new data arrival in AWS S3.
- **Integration**: Load validated data into a SQL Database for analytics and data science teams.
- **Technology Stack**:
  - **Data Ingestion**: AWS S3
  - **Orchestration**: Azure Data Factory (ADF)
  - **Data Validation**: Azure Functions
  - **Storage**: Azure Data Lake Storage (ADLS)
  - **Database**: Azure SQL Database

---

## 📂 Project Structure
```plaintext
smart-vehicles/
│
├── dataset/                 # Sample IoT JSON data
├── pipeline/                # Azure Data Factory pipeline configurations
├── linkedService/           # Linked Services created in project
├── trigger/                 # Triggers used in Pipeline
├── architecture/            # Architecture diagram
├── README.md                # Project documentation
