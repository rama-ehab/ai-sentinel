# 🛡️ AI Sentinel

> An intelligent cybersecurity platform that combines **Static Rule-Based Detection**, **Machine Learning**, and **Deep Learning** to detect cyber threats, identify anomalies in real time, visualize security events, and automate incident response.

---

## 📌 Overview

AI Sentinel is a graduation project designed to enhance cybersecurity monitoring by integrating traditional security mechanisms with Artificial Intelligence.

The platform continuously collects and processes web server logs, analyzes incoming requests using both rule-based detection and AI models, visualizes security events through an interactive dashboard, and automatically responds to malicious activities.

Unlike conventional security systems that rely solely on predefined signatures, AI Sentinel combines **Static Rules**, **Machine Learning**, and **Deep Learning** to detect both known attacks and previously unseen anomalies.

---

## ✨ Features

- 🔍 Real-time web log monitoring
- ⚡ Streaming data pipeline
- 🤖 Hybrid detection using Static Rules + AI
- 🧠 Anomaly Detection using Machine Learning
- 🎯 Threat Detection using supervised learning
- 📊 Interactive React dashboard
- 🚨 Real-time alert generation
- 📱 Telegram bot notifications
- 🔒 Automatic malicious IP blocking
- 📈 Security analytics and reporting

---

## 🏗️ System Architecture

```
                 Web Server
                     │
                     ▼
                 Filebeat
                     │
                     ▼
                 Logstash
                     │
                     ▼
                 RabbitMQ
                     │
                     ▼
              FastAPI Backend
                     │
      ┌──────────────┼──────────────┐
      │              │              │
      ▼              ▼              ▼
 Static Rules   Threat Detection  Anomaly Detection
                    │                  │
        XGBoost • Random Forest   Isolation Forest
             LightGBM             (Best Model)
                    │
                    ▼
              Alert Engine
      ┌──────────┼──────────┐
      ▼          ▼          ▼
 Dashboard   Telegram Bot   IP Blocking
```

---

## 🧠 Detection Modules

### 1. Threat Detection

The Threat Detection module identifies known cyberattacks using supervised Machine Learning models trained on labeled HTTP request data.

### Models Evaluated

- XGBoost
- Random Forest
- LightGBM

### Attack Types

- SQL Injection
- Cross-Site Scripting (XSS)
- Brute Force
- Directory Traversal
- Remote File Inclusion (RFI)
- Command Injection
- Suspicious Requests

The best-performing model was selected and integrated into the platform for real-time threat detection.

---

### 2. Anomaly Detection

The Anomaly Detection module detects abnormal behaviors that may indicate unknown or zero-day attacks.

### Models Evaluated

- Isolation Forest
- One-Class SVM
- Autoencoder (Deep Learning)

An ensemble approach was also evaluated during experimentation.

Following model evaluation, **Isolation Forest** achieved the best balance between accuracy, precision, speed, and scalability and was selected for deployment.

---

## 📊 Dashboard

The React dashboard provides a centralized interface for monitoring system security.

### Dashboard Features

- Live alerts
- Threat statistics
- Attack distribution
- Anomaly monitoring
- Detection history
- System activity
- Alert management

---

## ⚡ Automated Response

When suspicious or malicious behavior is detected, AI Sentinel automatically:

- Generates security alerts
- Sends notifications through Telegram
- Blocks malicious IP addresses
- Logs incidents for future investigation

This significantly reduces response time and improves overall security operations.

---

## 🛠️ Technologies Used

### Frontend

- React
- TypeScript
- Tailwind CSS

### Backend

- FastAPI
- Python

### Artificial Intelligence

- Scikit-learn
- TensorFlow
- Keras
- Pandas
- NumPy

### Streaming & Data Pipeline

- Filebeat
- Logstash
- RabbitMQ

### Database

- PostgreSQL

### Notifications

- Telegram Bot API

---

## 🔄 Workflow

```
Incoming HTTP Requests
          │
          ▼
     Web Server Logs
          │
          ▼
       Filebeat
          │
          ▼
       Logstash
          │
          ▼
       RabbitMQ
          │
          ▼
   FastAPI Processing
          │
   ┌──────┼──────┐
   ▼      ▼      ▼
Rules  Threats  Anomalies
          │
          ▼
   Alert Generation
          │
   ┌──────┼──────┐
   ▼      ▼      ▼
Dashboard Telegram IP Blocking
```

---

## 🎯 Project Objectives

- Detect cyber threats in real time
- Identify both known attacks and unknown anomalies
- Reduce false positives using AI
- Automate incident response
- Provide an interactive security dashboard
- Improve cybersecurity monitoring using intelligent analytics

---

## 👨‍💻 My Contributions

As part of the graduation project, I contributed to:

- Developing the Anomaly Detection module
- Training and evaluating Machine Learning and Deep Learning models
- Comparing Isolation Forest, One-Class SVM, Autoencoder, and Ensemble models
- Feature engineering and model optimization
- Integrating AI models with the FastAPI backend
- Participating in system integration and testing

---

## 🚀 Future Improvements

- Explainable AI (XAI)
- Online model retraining
- Cloud deployment
- Docker & Kubernetes support
- SIEM integration
- Advanced behavioral analytics
- Multi-server monitoring

---

## 📸 Project Screenshots

> Add screenshots of:

- Dashboard
- Threat Detection
- Anomaly Detection
- Alert Management
- Telegram Notifications

---

## 🎥 Demo

Add a short demonstration video or GIF showcasing:

- Real-time detection
- Dashboard interaction
- Alert generation
- Automatic response

---

## 📄 License

This project was developed as a **Computer Engineering Graduation Project** for academic purposes.
