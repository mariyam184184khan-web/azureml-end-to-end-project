# End-to-End Machine Learning Project using Azure ML Studio – Diabetes Prediction

## Project Overview
This project implements a complete **end-to-end machine learning workflow using Azure Machine Learning Studio**.  
It covers the entire ML lifecycle including **workspace creation, dataset management, automated model training using AutoML, pipeline orchestration using Designer, compute cluster configuration, and deployment to a real-time online endpoint**.

The solution predicts diabetes outcomes using the **Pima Indians Diabetes Dataset** and demonstrates enterprise-ready ML practices using Azure-native tools.

---

## Problem Statement
To design, train, and deploy a scalable machine learning solution that predicts whether a patient is diabetic based on clinical attributes, using Azure ML Studio and best practices for cloud-based machine learning workflows.

---

## Dataset
- **Dataset Name:** Pima Indians Diabetes Dataset  
- **Data Type:** Structured tabular data  
- **Machine Learning Task:** Binary Classification  
- **Target Variable:** Diabetes Outcome  

The dataset was registered within the Azure ML Workspace and used consistently across AutoML experiments and Designer pipelines to ensure reproducibility and traceability.

---

## Azure Machine Learning Workspace
- **Workspace Name:** `ms-azureml-ds-workspace`

An Azure ML Workspace was created as the central environment for:
- Managing datasets and model assets
- Running AutoML experiments
- Building and executing Designer pipelines
- Managing compute resources
- Deploying and monitoring online endpoints

Screenshots in this repository show the workspace configuration and resource management in Azure ML Studio.

---

## Compute Infrastructure
- **Compute Type:** Azure ML Compute Cluster  

An Azure ML compute cluster was created and configured to support scalable execution of:
- Automated Machine Learning experiments
- Designer training and inference pipelines

The cluster enables efficient parallel processing and optimized resource utilization for machine learning workloads.

---

## Automated Machine Learning (AutoML)
An **AutoML classification experiment** was executed to automatically identify the best-performing model for the dataset.

### AutoML Capabilities Utilized
- Automatic algorithm selection  
- Hyperparameter optimization  
- Model evaluation and comparison  

### Best Model
- **Selected Model:** Voting Ensemble  
- **Primary Evaluation Metric:** AUC (Weighted)  

AutoML evaluated multiple candidate models and selected the best-performing model, which was registered as an Azure ML model asset and reused within Designer pipelines.

Screenshots included in this repository show the completed AutoML experiment, inputs and outputs, and best model metrics.

---

## Designer Pipelines

### Training and Evaluation Pipeline
A training pipeline was created using **Azure ML Designer** to define a structured and reproducible workflow that includes:
- Data preprocessing
- Handling missing values
- Train–test data split
- Model training
- Model scoring
- Model evaluation

This pipeline ensures transparency, modularity, and consistency in the model development process.

---

### Real-Time Inference Pipeline
A real-time inference pipeline was developed using Designer components:
- Web Service Input  
- Trained model  
- Score Model  
- Web Service Output  

This pipeline enables real-time predictions and serves as the foundation for model deployment.

Screenshots demonstrate both the training pipeline and the real-time inference pipeline built using Azure ML Designer.

---

## Model Deployment
- **Deployment Method:** Azure ML Designer Real-Time Inference  
- **Endpoint Type:** Managed Online Endpoint  
- **Authentication:** Key-based authentication  

The trained model was successfully deployed as a **real-time online endpoint**, enabling inference through a REST API. The endpoint configuration and deployment status are documented through screenshots included in this repository.

---

## End-to-End Workflow Summary
1. Created an Azure ML Workspace  
2. Registered and managed the dataset  
3. Configured an Azure ML compute cluster  
4. Executed AutoML experiments for model selection  
5. Registered the best-performing model  
6. Built training and inference pipelines using Designer  
7. Deployed the model as a managed online endpoint  

---

## Repository Structure
azure-ml-studio-end-to-end-project/
│
├── README.md
│
└── screenshots/
    ├── workspace.png
    ├── dataset.png
    ├── compute-cluster.png
    ├── automl-run.png
    ├── best-model.png
    ├── designer-training-pipeline.png
    ├── designer-inference-pipeline.png
    └── endpoint.png

---

## Key Skills Demonstrated
- Azure Machine Learning Studio  
- Automated Machine Learning (AutoML)  
- Designer Pipelines  
- Compute Cluster Configuration  
- Model Evaluation and Selection  
- Real-Time Model Deployment  
- End-to-End ML Lifecycle Management  

---

## Conclusion
This project demonstrates hands-on experience in building, training, and deploying an end-to-end machine learning solution using Azure ML Studio. It reflects practical exposure to enterprise-grade ML workflows and Azure-native machine learning tools.

---

## Author
**Mariyam Khan**

