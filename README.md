# End-to-End Machine Learning Project using Azure ML Studio – Diabetes Prediction

## Project Overview
This project demonstrates a complete **end-to-end machine learning workflow using Azure Machine Learning Studio**.  
It covers the full ML lifecycle, including **workspace creation, dataset registration, automated model training using AutoML, pipeline orchestration using Azure ML Designer, compute cluster configuration, and deployment of a real-time inference endpoint**.

The solution predicts diabetes outcomes using the **Pima Indians Diabetes Dataset** and showcases practical, enterprise-aligned machine learning practices using Azure-native tools.

---

## Problem Statement
To design, train, and deploy a scalable machine learning solution that predicts whether a patient is diabetic based on clinical attributes, using Azure Machine Learning Studio and cloud-based ML best practices.

---

## Dataset
- **Dataset Name:** Pima Indians Diabetes Dataset  
- **Data Type:** Structured tabular data  
- **Machine Learning Task:** Binary Classification  
- **Target Variable:** Diabetes Outcome  

The dataset was uploaded and registered within the Azure ML Workspace and used consistently across AutoML experiments and Designer pipelines to ensure reproducibility and traceability.

---

## Azure Machine Learning Workspace
- **Workspace Name:** `ms-azureml-ds-workspace`

An Azure ML Workspace was created as the central environment for:
- Managing datasets and model assets  
- Running AutoML experiments  
- Building and executing Designer pipelines  
- Managing compute resources  
- Deploying and validating real-time inference endpoints  

Screenshots included in this repository show the workspace configuration and resource setup in Azure ML Studio.

---

## Compute Infrastructure
- **Compute Type:** Azure ML Compute Cluster  

An Azure ML compute cluster was created and configured to support scalable execution of:
- Automated Machine Learning experiments  
- Designer-based training and inference pipelines  

The compute cluster enables efficient resource utilization and parallel execution of machine learning workloads.

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

---

## Designer Pipelines

### Training and Evaluation Pipeline
A training pipeline was built using **Azure ML Designer** to define a structured and reproducible workflow that includes:
- Data preprocessing  
- Handling missing values  
- Train–test data split  
- Model training  
- Model scoring  
- Model evaluation  

This pipeline ensures modularity, transparency, and consistency throughout the model development process.

---

### Real-Time Inference Pipeline
A real-time inference pipeline was developed using Designer components:
- Web Service Input  
- Trained Model  
- Score Model  
- Web Service Output  

This pipeline enables real-time predictions and serves as the foundation for deployment.

---

## Model Deployment and Real-Time Inference
- **Deployment Method:** Azure ML Designer Real-Time Inference  
- **Endpoint Type:** Real-time inference endpoint (Azure Container Instance)  
- **Authentication:** Key-based authentication  

The trained model was deployed as a real-time inference endpoint using Azure Machine Learning Designer.  
The deployment exposes the model as a REST API hosted on **Azure Container Instance**, allowing external clients to send HTTP POST requests and receive predictions in real time.


---

## API Testing using Postman
The deployed endpoint was tested using **Postman** to validate real-time inference functionality.  
A POST request containing patient health attributes was sent to the REST endpoint, and the service returned the predicted diabetes outcome along with a confidence score.

### Sample Request
```json
{
  "Inputs": {
    "input1": [
      {
        "Pregnancies": 6,
        "Glucose": 148,
        "BloodPressure": 72,
        "SkinThickness": 35,
        "Insulin": 0,
        "BMI": 33.6,
        "DiabetesPedigreeFunction": 0.627,
        "Age": 50
      }
    ]
  },
  "GlobalParameters": {}
}
{
  "Results": {
    "WebServiceOutput0": [
      {
        "Scored Labels": 1.0,
        "Scored Probabilities": 0.7124
      }
    ]
  }
}

---
## Author
**Mariyam Khan**  
