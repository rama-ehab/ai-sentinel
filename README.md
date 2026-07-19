AI Sentinel

An intelligent cybersecurity platform that combines rule-based detection, Machine Learning, and Deep Learning to identify cyber threats, detect anomalies in real time, and automate incident response through an interactive dashboard.

Overview

AI Sentinel is a graduation project developed to improve cybersecurity monitoring by integrating traditional security mechanisms with Artificial Intelligence. The platform continuously processes web server logs, detects suspicious activities, visualizes security events through a real-time dashboard, and automatically responds to critical threats.

Unlike traditional security systems that rely only on predefined signatures, AI Sentinel combines static rules, Machine Learning, and Deep Learning to detect both known attacks and previously unseen anomalies.

Key Features
Real-time log collection and processing
Hybrid threat detection using static rules and AI
Anomaly Detection using Machine Learning
Threat Detection using supervised learning models
Interactive React dashboard
Automated alert generation
Telegram bot notifications
Automatic blocking of malicious IPs
Real-time security monitoring and analytics
System Architecture
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
     ├─────────────── Static Rule Engine
     │
     ├─────────────── Threat Detection Models
     │                    ├── XGBoost
     │                    ├── Random Forest
     │                    └── LightGBM
     │
     ├─────────────── Anomaly Detection
     │                    └── Isolation Forest
     │
     ▼
Alert Engine
     │
     ├── React Dashboard
     ├── Telegram Bot
     └── Automatic IP Blocking
Detection Modules
Threat Detection

The Threat Detection module identifies known cyberattacks using supervised Machine Learning models trained on labeled HTTP request data.

Models Evaluated
XGBoost
Random Forest
LightGBM

The models detect attacks such as:

SQL Injection
Cross-Site Scripting (XSS)
Brute Force
Directory Traversal
Remote File Inclusion (RFI)
Command Injection
Suspicious Requests

After evaluation, the best-performing model was integrated into the platform for real-time prediction.

Anomaly Detection

The Anomaly Detection module focuses on identifying previously unseen or abnormal behavior that traditional signatures cannot detect.

Multiple unsupervised models were evaluated:

Isolation Forest
One-Class SVM
Autoencoder (Deep Learning)

An ensemble model was also tested during experimentation.

Following performance evaluation, Isolation Forest was selected for deployment because it achieved the best balance between accuracy, precision, speed, and scalability for real-time monitoring.

Dashboard

The React dashboard provides a centralized interface for monitoring the security status of the system.

Features include:

Live alerts
Threat statistics
Attack distribution
Anomaly monitoring
System activity overview
Detection history
Alert management
Automated Response

When malicious behavior is detected, AI Sentinel can automatically:

Generate alerts
Notify administrators through Telegram
Block malicious IP addresses
Record security events for future analysis

This reduces response time and helps mitigate attacks before they escalate.

Technologies Used
Frontend
React
TypeScript
Tailwind CSS
Backend
FastAPI
Python
Machine Learning & AI
Scikit-learn
TensorFlow / Keras
Pandas
NumPy
Data Pipeline
Filebeat
Logstash
RabbitMQ
Database
PostgreSQL
Visualization
React Dashboard
Notifications
Telegram Bot API
Project Workflow
Incoming Requests
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
        ├── Static Rules
        ├── Threat Detection
        └── Anomaly Detection
        │
        ▼
Alert Generation
        │
        ├── Dashboard
        ├── Telegram Notification
        └── IP Blocking
Project Goals
Improve real-time cyber threat detection
Detect both known attacks and unknown anomalies
Reduce false positives using AI models
Automate incident response
Provide an intuitive monitoring dashboard
Enhance cybersecurity through intelligent analytics
Team Contributions

My primary contributions included:

Developing and evaluating the Anomaly Detection models
Building and comparing Machine Learning and Deep Learning approaches
Performing feature engineering and model evaluation
Integrating AI models into the FastAPI backend
Contributing to system integration and overall platform development
Future Improvements
Online model retraining
Explainable AI (XAI) for predictions
SIEM integration
Cloud deployment
Containerization with Docker and Kubernetes
Advanced behavioral analytics
Multi-server monitoring
License

This project was developed as a Computer Engineering Graduation Project for academic purposes.
