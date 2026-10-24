# Network Security: End-to-End MLOps Phishing Detection

An end-to-end ML system that classifies URLs/network data as phishing or legitimate.

## What it does
- Modular pipeline: data ingestion (MongoDB Atlas) → validation (KS-test drift detection across 31 features) → transformation (KNN imputation) → training (5 classifiers, GridSearchCV, 3-fold CV)
- Experiment tracking with MLflow + DagsHub; model artifacts versioned in S3
- FastAPI service with endpoints for training and batch prediction
- Dockerized, with CI/CD through GitHub Actions to Amazon ECR/EC2

## Tech stack
Python, Scikit-learn, FastAPI, MLflow, Docker, AWS (EC2, S3, ECR), MongoDB Atlas

## Run locally
1. `pip install -r requirements.txt`
2. Create a `.env` with your MongoDB connection string (see `.env.example`)
3. `python app.py`, then open `/docs` for the API

## Results
(Add your best model's F1 / Precision / Recall here)
