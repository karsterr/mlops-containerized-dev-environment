# MLOps Containerized Development Environment (Docker Compose)

## 🚀 Project Overview
This project creates a fully reproducible, isolated, and standardized development environment using **Docker Compose**. It bundles all necessary MLOps components—a Jupyter/VS Code server, an MLflow Tracking Server, and a PostgreSQL database—into a single, portable configuration. This ensures that any data scientist or engineer can start a new project with all necessary dependencies instantly, promoting collaboration and eliminating "works on my machine" issues.

This demonstrates fundamental DevOps, MLOps, and Linux containerization skills.

## ⚙️ Key Technologies
* **Linux (Docker):** Core operating system for containers.
* **Docker Compose:** Orchestration and service definition.
* **MLflow:** Experiment tracking service.
* **PostgreSQL:** Centralized database for MLflow artifacts/metadata and feature storage.
* **Jupyter/VS Code Server:** Primary development environment.

## 📋 Project Scope and Deliverables
1.  **Service Definition:** Creating a `docker-compose.yml` file defining four interconnected services: `mlflow-server`, `postgres-db`, `jupyter-lab`, and a `dvc-cache` volume (optional).
2.  **Networking:** Ensuring all services can communicate seamlessly (e.g., Jupyter can connect to MLflow, and MLflow can connect to Postgres).
3.  **Persistence:** Configuring **Docker Volumes** to ensure that all MLflow run data and database contents persist even if the containers are stopped.
4.  **Test Script:** Including a simple `train_example.py` script that successfully logs a run to the containerized MLflow server, using the containerized PostgreSQL backend.

## 📊 Results and Benchmarks
The environment can be started with a single command (`docker-compose up`) and provides a fully functional MLOps environment in under **[TIME] seconds**.

## 🏃 Getting Started
1.  Ensure Docker and Docker Compose are installed on your Linux system.
2.  Start the environment: `docker-compose up -d`
3.  Access JupyterLab: `http://localhost:8888`
4.  Access MLflow UI: `http://localhost:5000`
