# 🚀 Real-Time IoT Machine Failure Prediction System

## 📌 Project Overview

This project implements a complete **real-time predictive maintenance pipeline** for industrial IoT systems using **Apache Kafka**, **PySpark Structured Streaming**, and **Spark MLlib**.

The system continuously streams machine sensor readings, processes them in real time, applies rule-based alerts, and predicts machine failures using a trained **Random Forest Classifier**.

The solution demonstrates how Big Data technologies can be combined with Machine Learning to enable proactive maintenance and reduce equipment downtime.

---

## 🎯 Objectives

* Simulate real-time IoT sensor streams
* Process streaming data using Apache Spark
* Detect abnormal machine behavior
* Predict machine failures using Machine Learning
* Generate real-time maintenance alerts
* Demonstrate an end-to-end Big Data Analytics pipeline

---

## 🏗️ System Architecture

```text
AI4I Dataset
      │
      ▼
Kafka Producer
      │
      ▼
Apache Kafka Topic
      │
      ▼
Kafka Consumer
      │
      ▼
PySpark Structured Streaming
      │
      ▼
Feature Engineering
      │
      ▼
Random Forest Model
      │
      ▼
Failure Prediction
      │
      ▼
Alert Generation & Visualization
```

---

## 🛠 Technologies Used

| Technology                 | Purpose                     |
| -------------------------- | --------------------------- |
| Python                     | Core Development            |
| Apache Kafka               | Real-Time Data Streaming    |
| PySpark                    | Distributed Data Processing |
| Spark Structured Streaming | Stream Analytics            |
| Spark MLlib                | Machine Learning            |
| Random Forest              | Failure Prediction          |
| Pandas                     | Data Manipulation           |
| Matplotlib                 | Data Visualization          |
| Google Colab               | Development Environment     |

---

## 📊 Dataset

### AI4I 2020 Predictive Maintenance Dataset

The dataset contains **10,000 industrial machine records** with sensor measurements:

Features:

* Air Temperature (K)
* Process Temperature (K)
* Rotational Speed (RPM)
* Torque (Nm)
* Tool Wear (min)

Target Variable:

* Machine Failure

  * 0 = Normal Operation
  * 1 = Failure

---

## ⚙️ Pipeline Workflow

### Step 1: Data Loading

The AI4I dataset is loaded and cleaned for processing.

### Step 2: Kafka Producer

Sensor readings are converted into JSON messages and streamed into a Kafka topic.

Example:

```json
{
  "air_temp": 298.1,
  "process_temp": 308.6,
  "rpm": 1551,
  "torque": 42.8,
  "tool_wear": 0,
  "label": 0
}
```

### Step 3: Kafka Consumer

The consumer receives incoming sensor events and performs real-time monitoring.

### Step 4: Structured Streaming

Spark processes incoming events as a continuous stream.

### Step 5: Alert Detection

Rule-based thresholds identify:

* Overspeed Risk
* Overload Risk
* Excessive Tool Wear
* Thermal Risk

### Step 6: Machine Learning Prediction

A trained Random Forest model predicts machine failure probability.

### Step 7: Real-Time Monitoring

Predictions and alerts are displayed for maintenance decision-making.

---

## 🤖 Machine Learning Model

### Model Used

**Random Forest Classifier**

Reason for Selection:

* High Accuracy
* Handles Nonlinear Relationships
* Robust to Noise
* Suitable for Industrial Sensor Data

Input Features:

```text
air_temp
process_temp
rpm
torque
tool_wear
```

Output:

```text
0 → Normal
1 → Failure
```

---

## 🚨 Alert Levels

| Risk Score | Alert    |
| ---------- | -------- |
| 0          | SAFE     |
| 1          | WARNING  |
| 2+         | CRITICAL |

---

## 📈 Key Features

✅ Real-Time Data Streaming

✅ Kafka Producer-Consumer Architecture

✅ Spark Structured Streaming

✅ Predictive Maintenance

✅ Machine Failure Prediction

✅ Rule-Based Risk Detection

✅ Machine Learning Integration

✅ Big Data Processing

---

## 📂 Project Structure

```text
iot_failure_project/
│
├── datasets/
│   └── ai4i2020.csv
│
├── notebooks/
│   └── IoT_Failure_Prediction.ipynb
│
├── models/
│   ├── rf_model/
│   └── saved_model/
│
├── architecture/
│   └── architecture_diagram.png
│
├── screenshots/
│
├── visuals/
│
└── report/
    └── IoT_Failure_Prediction_Report.pdf
```

---

## 📷 Results

The project successfully demonstrates:

* End-to-End Streaming Analytics
* Real-Time Failure Detection
* Predictive Maintenance Workflow
* Integration of Kafka, Spark, and Machine Learning

---

## 👩‍💻 Author

**Fatima**
BS Data Science
Big Data Analytics Project

---


