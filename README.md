# MindMeter – ML-Based Cognitive Fatigue Detection System

## Overview

MindMeter is a behavioral analytics system designed to detect cognitive fatigue using machine learning. The system collects user interaction data from a quiz-based interface and analyzes behavioral patterns such as response time, completion time, and interaction events to classify fatigue levels.

The project integrates a full AI pipeline including data collection, storage, feature engineering, machine learning model training, and fatigue prediction.


## Problem Statement

Cognitive fatigue affects decision-making, productivity, and mental performance. Detecting fatigue using behavioral signals can help improve human–computer interaction systems, productivity tools, and mental health monitoring platforms.

This project explores whether user interaction data can be used to predict fatigue levels using machine learning models.


## System Architecture

User → React Quiz Interface
↓
Behavior Tracking (Response time, clicks, scores)
↓
Node.js Backend API
↓
MongoDB Database
↓
Data Export & Feature Engineering (Python)
↓
Machine Learning Model Training
↓
Fatigue Level Prediction


## Technologies Used

Frontend
• React.js

Backend
• Node.js
• Express.js

Database
• MongoDB

Machine Learning
• Python
• Pandas
• Scikit-learn

Visualization
• Matplotlib


## Dataset Features

The dataset was generated from user interactions with the quiz application.

Primary Features:

* totalScore
* totalTime
* averageResponseTime

Behavioral Features:

* avgQuestionTime
* timeVariance
* totalClicks
* avgClicksPerQuestion

Target Variable:

* fatigueLevel

  * Low Fatigue
  * Moderate Fatigue
  * High Fatigue


## Machine Learning Models

The following models were trained and evaluated:

| Model                        | Description                               |
| ---------------------------- | ----------------------------------------- |
| Logistic Regression          | Baseline classification model             |
| Support Vector Machine (SVM) | Effective for small datasets              |
| Random Forest                | Ensemble model used for final predictions |

## Model Evaluation

Evaluation metrics used:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

Example performance:

| Model               | Accuracy   |
| ------------------- | ---------- |
| Logistic Regression | ~0.62      |
| SVM                 | ~0.75      |
| Random Forest       | ~0.80–0.87 |

## Feature Importance

Random Forest was used to identify the most influential behavioral features affecting fatigue prediction.

Important features include:

* totalScore
* averageResponseTime
* totalTime
* avgQuestionTime

## Project Workflow

1. User completes cognitive fatigue quiz
2. Behavioral interaction data is recorded
3. Data is stored in MongoDB
4. Dataset is exported and processed
5. Behavioral features are extracted
6. Machine learning models are trained
7. Model predicts fatigue levels

## Future Improvements

* Increase dataset size for better model generalization
* Deploy ML model as an API for real-time fatigue prediction
* Implement deep learning models for behavioral analysis
* Integrate real-time monitoring dashboards

