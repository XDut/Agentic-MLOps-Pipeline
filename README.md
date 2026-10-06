# Agentic MLOps Pipeline

An experimental **Agentic MLOps pipeline** that combines machine learning, experiment tracking, automated retraining, and LLM-based decision making.

## Features

- **XGBoost** for model training
- **Optuna** for hyperparameter tuning
- **MLflow** for experiment tracking and model logging
- **LangGraph** for workflow orchestration
- **Google Gemini** as the retraining decision agent
- Automated model retraining and version updates
- Workflow visualization using NetworkX

## Workflow

```text
Dataset
   ↓
Preprocessing
   ↓
XGBoost Training
   ↓
Optuna Tuning
   ↓
MLflow Tracking
   ↓
Model Monitoring
   ↓
Performance Degradation?
   ├── No → Done
   └── Yes
         ↓
    Gemini Agent
         ↓
    Retrain?
     ├── No → Done
     └── Yes
           ↓
        Retrain
           ↓
        MLflow
           ↓
        Deploy
```

## Tech Stack

`Python` `XGBoost` `Optuna` `MLflow` `LangGraph` `Gemini` `Scikit-learn` `Pandas`

## Run

Install dependencies:

```bash
pip install mlflow optuna xgboost pandas scikit-learn langchain-google-genai langgraph python-dotenv networkx matplotlib
```

Add your Gemini API key and place the dataset as:

```text
diabetes_prediction_dataset.csv
```

Then run:

```text
Agentic MLOps Pipeline.ipynb
```

## Current Scope

This project is a **proof-of-concept Agentic MLOps system**.

The current version demonstrates:

```text
Monitoring → Agent Decision → Retraining → Model Update
```

Future improvements can include:

- FastAPI model serving
- Docker
- MLflow Model Registry
- Evidently drift detection
- Prometheus/Grafana monitoring
- CI/CD
- Champion vs Challenger deployment

## Goal

The goal is to explore how **AI agents can participate in the ML lifecycle**, moving from traditional MLOps automation toward **self-managing ML systems**.

## Disclaimer

For educational and portfolio purposes only. The diabetes model is not intended for medical diagnosis.
