# Student Sleep Quality Prediction

A machine learning pipeline designed to predict student sleep quality based on biometric and lifestyle-related input features. This solution utilizes a Random Forest model trained and deployed on **Amazon SageMaker**, with model artifacts managed in **Amazon S3**. It supports end-to-end processing—from training to real-time inference—using a custom entrypoint and containerized environment.

---

## Project Description

Sleep quality plays a critical role in students' academic performance and overall well-being. The goal of this project is to provide a scalable, cloud-based predictive system to classify the sleep quality of students on a scale of 1–10. It does this by analyzing physical and lifestyle metrics such as heart rate, stress level, and daily activity data.

By leveraging AWS SageMaker, the model can be trained and deployed efficiently, allowing seamless integration with applications or user interfaces for real-time predictions.

---

## Project Overview

This project provides a robust machine learning solution that follows a typical ML workflow:
- Preprocessing the dataset and feature engineering.
- Training a Random Forest Classifier using SageMaker's SKLearn Estimator.
- Storing the trained model in S3.
- Deploying the model to a live SageMaker endpoint.
- 
---

## Key Features

- Cloud-based model training and deployment with Amazon SageMaker.
- Real-time inference through SageMaker endpoint.
- Modular design with custom training and inference scripts.
- Scikit-learn Random Forest model with tunable parameters.
- Integration with Amazon S3 for data and model storage.
- Jupyter Notebook for experimentation.

---

## Tech Stack

| Category         | Tools / Services                          |
|------------------|-------------------------------------------|
| **Language**     | Python                                    |
| **ML Framework** | Scikit-learn (Random Forest Classifier)   |
| **Cloud**        | AWS SageMaker, Amazon S3                  |
| **IDE**          | Jupyter Notebook                          |
| **Deployment**   | SageMaker Endpoint                        |

---

## Key Steps

### 1. Exploratory Data Analysis (EDA) and Data Preprocessing
- Check missing values
- Check dtype of features
- Check class distribution
- Clean and format dataset.
- Encode input features as needed.

### 2. Model Training
- Use SageMaker SKLearn Estimator to train a Random Forest classifier.
- Entrypoint script (`script.py`) defines training logic.
- Trained model is saved automatically to S3.

### 3. Model Deployment
- Model is deployed to a real-time SageMaker endpoint.

### 4. Inference
- Accepts new input feature values and returns predicted sleep quality.
