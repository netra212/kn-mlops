# 🧠 End-to-End Data Science Project

A modular and scalable Machine Learning project built with production-level standards, including complete workflows for data ingestion, validation, transformation, model training, and evaluation.

---

## 🚀 Project Overview

This project demonstrates an **end-to-end ML pipeline**, using best practices for configuration, code modularity, experiment tracking, and reproducibility. It leverages tools such as **MLflow**, **Dagshub**, and YAML configuration files to streamline every step of the pipeline.

---

## 📁 Project Structure


├── config
│ ├── config.yaml # Core configuration
│ ├── schema.yaml # Schema definitions for data validation
│ └── params.yaml # Model and training hyperparameters
│
├── src
│ ├── config # Configuration manager
│ │ └── configuration.py
│ ├── components # Individual pipeline components
│ │ ├── data_ingestion.py
│ │ ├── data_validation.py
│ │ ├── data_transformation.py
│ │ ├── model_trainer.py
│ │ └── model_evaluation.py
│ └── pipeline # Workflow orchestration
│ ├── training_pipeline.py
│ └── evaluation_pipeline.py
│
├── main.py # Entry point to trigger pipelines
└── requirements.txt # Python dependencies



---

## 🔁 Workflow Steps

### 1. **Data Ingestion**
- Reads raw data from a source (local/remote).
- Stores it in an organized directory structure.

### 2. **Data Validation**
- Ensures that incoming data meets expected formats and schema definitions (via `schema.yaml`).

### 3. **Data Transformation**
- Performs feature engineering and data preprocessing.
- Handles missing values, encoding, normalization, etc.

### 4. **Model Training**
- Trains ML models based on `params.yaml` hyperparameters.
- Saves models, metrics, and artifacts for reproducibility.

### 5. **Model Evaluation**
- Evaluates trained models using validation/test sets.
- Tracks metrics using:
  - 📌 **MLflow** for experiment tracking
  - 🌐 **Dagshub** for remote storage and collaboration (like S3)

---

## 🧩 Configuration Files

- `config.yaml`: Paths, directory structure, and general settings.
- `schema.yaml`: Column names, types, and constraints for validation.
- `params.yaml`: Hyperparameters for model training and evaluation.

---

## 🛠️ What's Updated

- ✅ `config.yaml` – Core configurations.
- ✅ `schema.yaml` – Data validation schema.
- ✅ `params.yaml` – Model hyperparameters.
- ✅ Entity classes – Data structures used across the pipeline.
- ✅ Configuration Manager – Centralized config loader in `src/config/`.
- ✅ Components – Modular logic for each pipeline step.
- ✅ Pipelines – Orchestrators calling each component.
- ✅ `main.py` – Single entry point for end-to-end execution.

---

## ▶️ Running the Pipeline

```bash
# Activate virtual environment
source venv/bin/activate  # or .venv/Scripts/activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the main pipeline
python main.py

--

** ## 🔍 Experiment Tracking**

Tool	Usage
MLflow	Logs model metrics, parameters, artifacts
Dagshub	Stores versioned data, models, experiment history

## 💡 Future Improvements
* Dockerize the pipeline.

* CI/CD with GitHub Actions.

* Real-time monitoring and alerting.

* Integration with cloud-based model serving.


