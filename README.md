# 🚀 Network Security System – End-to-End ML + MLOps Pipeline

An end-to-end **Machine Learning + MLOps system** for detecting network intrusions and anomalies using a fully automated pipeline covering **ingestion → preprocessing → model training → registry → deployment → monitoring**.

This project demonstrates how to build production-grade ML workflows using **MLflow, FastAPI, Docker, and AWS**.

---

## 📌 Features

### ✅ Automated Data Ingestion  
- Scheduled ingestion from cloud/local sources  
- Schema validation + versioning  
- Stores raw & processed datasets

### ✅ Preprocessing & Feature Engineering  
- Cleaning + transformation  
- Session-level metrics  
- Encoding + scaling pipeline  
- Artifact generation for training

### ✅ ML Training with MLflow  
- Models: RandomForest, XGBoost, LightGBM, Neural Networks  
- MLflow logs: metrics, params, confusion matrix, artifacts  
- Automatic best-model selection

### ✅ Model Registry & Promotion  
- MLflow Model Registry  
- Auto-promotion from *Staging → Production*

### ✅ FastAPI Deployment  
- Real-time prediction endpoint  
- Loads production model directly from registry  
- Fully containerized using Docker  
- Ready for AWS EC2/ECS deployment

### ✅ CI/CD Automation  
- GitHub Actions pipeline  
- Code checks, tests, Docker build & deploy  
- Automatic API redeployment

### ✅ Monitoring & Drift Detection  
- Input/output drift tracking  
- Latency monitoring  
- Grafana/Prometheus integration

---

## 🧠 Architecture

           ┌────────────────────────┐
           │     Data Ingestion      │
           └────────────┬───────────┘
                        │
           ┌────────────▼───────────┐
           │   Preprocessing & FE    │
           └────────────┬───────────┘
                        │
           ┌────────────▼───────────┐
           │     Model Training      │
           │     (MLflow)            │
           └────────────┬───────────┘
                        │
           ┌────────────▼───────────┐
           │    Model Registry       │
           └────────────┬───────────┘
                        │
           ┌────────────▼───────────┐
           │ FastAPI Deployment API  │
           └────────────┬───────────┘
                        │
           ┌────────────▼───────────┐
           │ Monitoring + Drift      │
           └─────────────────────────┘
