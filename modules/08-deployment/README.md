# 🚀 Module 08: Deployment

**Status:** ✅ Complete and Ready to Learn (Deep Version)
**Last Updated:** January 2026

---

## 📚 What You’ll Learn in This Module

Deployment means turning a trained model into a **usable system** that can be accessed by users, decision makers, or other software.

A deployed ML system must answer five research critical questions:

1. **Correctness**: Does it produce valid predictions for the intended use case
2. **Reproducibility**: Can we reproduce results across machines and time
3. **Reliability**: Does it fail safely under unexpected input
4. **Transparency**: Can we explain outputs to stakeholders
5. **Maintainability**: Can we update it without breaking the system

This module teaches you to build a deployment pipeline that is **simple but scientifically rigorous**.

---

## 🎨 Module Overview

```
┌────────────────────────────────────────────────────────────────┐
│                     DEPLOYMENT LEARNING JOURNEY                 │
├────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1️⃣ Define Deployment Goal and Users 🎯                          │
│  ↓                                                               │
│  2️⃣ Freeze Preprocessing and Feature Schema 🧾                    │
│  ↓                                                               │
│  3️⃣ Package Model as a Single Predictive Artifact 📦              │
│  ↓                                                               │
│  4️⃣ Create Interfaces (CLI, API, Web UI) 🌐                       │
│  ↓                                                               │
│  5️⃣ Deploy Locally and Validate End-to-End ✅                     │
│  ↓                                                               │
│  6️⃣ Deploy to Cloud (Demo or Production) ☁️                      │
│  ↓                                                               │
│  7️⃣ Add Monitoring, Logging, and Drift Checks 📊                  │
│  ↓                                                               │
│  8️⃣ Plan Updates, Versioning, and Governance 🔄                   │
│                                                                  │
└────────────────────────────────────────────────────────────────┘
```

---

## 📋 Prerequisites

* ✅ Modules 01–07 completed
* ✅ Trained model(s) with evaluation results
* ✅ Understanding of what inputs the model expects
* ✅ Clear problem statement and scope

**Estimated Time:** 14–18 hours

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

* Package models into reproducible artifacts
* Validate end-to-end inference with correct feature schema
* Build deployment interfaces using Streamlit and Flask
* Deploy to accessible platforms
* Monitor performance and detect drift
* Maintain and update deployments safely
* Write a deployment subsection for a journal paper

---

## 📖 Table of Contents

### [Section 1: Deployment Fundamentals](#section-1) 🎯

### [Section 2: Saving and Loading Models Correctly](#section-2) 💾

### [Section 3: Preprocessing and Feature Schema Locking](#section-3) 🧾

### [Section 4: Deployment Interface Types](#section-4) 🌐

### [Section 5: Streamlit Deployment in Research](#section-5) 🚀

### [Section 6: Flask API Deployment](#section-6) ⚙️

### [Section 7: Cloud Deployment Options](#section-7) ☁️

### [Section 8: Monitoring, Logging, and Drift](#section-8) 📊

### [Section 9: Model Updating and Version Governance](#section-9) 🔄

### [Section 10: Production Best Practices and Research Reporting](#section-10) 🏗️

---

<a name="section-1"></a>

## 🎯 Section 1: Deployment Fundamentals

### 1.1 What Exactly Is Deployment

Deployment is the process of converting this:

```
Notebook + Trained model + Manual feature steps
```

into this:

```
A repeatable prediction service that works on new data
```

---

### 1.2 Deployment Categories

```
┌───────────────────────────────┐
│        DEPLOYMENT TYPES        │
├───────────────────────────────┤
│  1) Offline deployment         │
│     • batch predictions        │
│     • reporting pipelines      │
│                               │
│  2) Interactive deployment     │
│     • Streamlit dashboards     │
│     • decision support tools   │
│                               │
│  3) API deployment             │
│     • Flask / FastAPI service  │
│     • system integration       │
└───────────────────────────────┘
```

**Research recommendation:** start with **interactive deployment**, then add an API if needed.

---

<a name="section-2"></a>

## 💾 Section 2: Saving and Loading Models Correctly

### 2.1 Why Saving Models Is Not Enough

Saving only the model object is risky because:

* Feature order may change
* Preprocessing may be inconsistent
* Categories may be missing in new data
* Scaling may be different
* Model outputs become unreproducible

---

### 2.2 Correct Saving Strategy (Preferred)

**Save everything required for prediction as one unit.**

```python
import joblib
from sklearn.pipeline import Pipeline

pipeline = Pipeline([
    ("preprocess", preprocessor),
    ("model", model)
])

joblib.dump(pipeline, "pipeline.joblib")
```

---

### 2.3 Model Metadata (Research grade)

Create a metadata file.

```python
import json
from datetime import datetime

metadata = {
    "model_name": "LightGBM_trip_duration",
    "created_at": str(datetime.utcnow()),
    "features": list(X_train.columns),
    "target": "trip_duration_seconds",
    "metrics": {
        "MAE": float(mae),
        "RMSE": float(rmse),
        "R2": float(r2)
    },
    "training_data_version": "v1.0",
    "random_seed": 42
}

with open("model_metadata.json", "w") as f:
    json.dump(metadata, f, indent=2)
```

This supports:

* reproducibility
* peer review
* future updates

---

<a name="section-3"></a>

## 🧾 Section 3: Preprocessing and Feature Schema Locking

### 3.1 The Feature Schema Problem

Most deployment failures happen because the system receives:

* missing features
* wrong feature type
* wrong unit
* wrong category mapping
* wrong feature order

---

### 3.2 Schema Locking Strategy

Create a strict schema.

```python
FEATURE_SCHEMA = {
    "Speed_km_h": "float",
    "Weather_Severity": "int",
    "Road_Condition": "int",
    "Driver_Age": "float"
}
```

Validate before prediction.

```python
def validate_input(data_dict, schema):
    for key, dtype in schema.items():
        if key not in data_dict:
            raise ValueError(f"Missing feature: {key}")
        if dtype == "float":
            float(data_dict[key])
        if dtype == "int":
            int(data_dict[key])
    return True
```

---

### 3.3 Unit Consistency

In transportation, unit mistakes are common:

* km/h vs m/s
* minutes vs seconds
* meters vs kilometers

Add unit conversions explicitly in deployment.

---

<a name="section-4"></a>

## 🌐 Section 4: Deployment Interface Types

### 4.1 Interface Options

```
┌───────────────────────────────────────────────────┐
│ INTERFACE TYPE → WHO USES IT                       │
├───────────────────────────────────────────────────┤
│ CLI tool → researchers, batch runs                 │
│ Streamlit UI → students, stakeholders              │
│ Flask API → system integration, scalability         │
└───────────────────────────────────────────────────┘
```

---

<a name="section-5"></a>

## 🚀 Section 5: Streamlit Deployment in Research

### 5.1 Why Streamlit Is Ideal for Academic Tools

* Minimal code overhead
* Best for interactive decision support
* Easy to deploy and share
* Works well with plots and XAI results

---

### 5.2 Minimum Research Grade Streamlit Structure

```
app.py
pipeline.joblib
model_metadata.json
requirements.txt
```

---

### 5.3 Streamlit App Template

```python
import streamlit as st
import joblib
import json
import numpy as np

st.title("Accident Severity Prediction System")

pipeline = joblib.load("pipeline.joblib")

with open("model_metadata.json") as f:
    meta = json.load(f)

st.sidebar.header("Input Features")

speed = st.sidebar.number_input("Speed (km/h)", 0.0, 150.0, 60.0)
weather = st.sidebar.selectbox("Weather Severity", [1,2,3,4,5])
road = st.sidebar.selectbox("Road Condition", [1,2,3])
age = st.sidebar.number_input("Driver Age", 16.0, 90.0, 35.0)

X = np.array([[speed, weather, road, age]])

if st.button("Predict"):
    pred = pipeline.predict(X)[0]
    prob = pipeline.predict_proba(X)[0][1]

    st.subheader("Prediction Result")
    st.write(f"Predicted class: {pred}")
    st.write(f"Severe crash probability: {prob:.2%}")

    st.subheader("Model Metadata")
    st.json(meta)
```

---

<a name="section-6"></a>

## ⚙️ Section 6: Flask API Deployment

### 6.1 Why Use an API

An API enables:

* integration with other applications
* automated requests
* scalability
* mobile and system usage

---

### 6.2 Flask Prediction Endpoint

```python
from flask import Flask, request, jsonify
import joblib
import numpy as np

app = Flask(__name__)
pipeline = joblib.load("pipeline.joblib")

@app.route("/predict", methods=["POST"])
def predict():
    payload = request.json
    x = np.array(payload["features"]).reshape(1, -1)
    pred = pipeline.predict(x)[0]
    prob = pipeline.predict_proba(x)[0][1]
    return jsonify({"prediction": int(pred), "probability": float(prob)})

app.run(host="0.0.0.0", port=5000)
```

---

<a name="section-7"></a>

## ☁️ Section 7: Cloud Deployment Options

### 7.1 Deployment Options

| Platform          | Best For                |
| ----------------- | ----------------------- |
| Streamlit Cloud   | Research demos          |
| Render / Railway  | Small APIs              |
| AWS / GCP / Azure | Scalable production     |
| Local Server      | Controlled environments |

---

### 7.2 requirements.txt Example

```
scikit-learn==1.4.2
joblib==1.4.2
streamlit==1.39.0
numpy==2.0.1
pandas==2.2.2
```

Pin versions for reproducibility.

---

<a name="section-8"></a>

## 📊 Section 8: Monitoring, Logging, and Drift

### 8.1 Deployment Without Monitoring Is Unsafe

After deployment:

* distributions change
* accuracy declines
* bias increases

---

### 8.2 Logging Predictions

Store input and output.

```python
import pandas as pd
from datetime import datetime

def log_prediction(inputs, pred, prob, file="logs.csv"):
    row = {**inputs, "pred": pred, "prob": prob, "time": datetime.utcnow()}
    df = pd.DataFrame([row])
    df.to_csv(file, mode="a", header=not pd.io.common.file_exists(file), index=False)
```

---

### 8.3 Simple Drift Check

Compare new inputs with training distributions.

```
If mean or variance shifts strongly, drift is likely.
```

---

<a name="section-9"></a>

## 🔄 Section 9: Model Updating and Version Governance

### 9.1 Why Updates Must Be Controlled

Uncontrolled updates create:

* inconsistent results
* lost reproducibility
* invalid papers

---

### 9.2 Version Naming Convention

```
pipeline_v1.joblib
pipeline_v2.joblib
metadata_v1.json
metadata_v2.json
```

---

### 9.3 Safe Update Protocol

```
1) train new model
2) evaluate and compare
3) statistical testing
4) stakeholder validation
5) deploy as new version
6) archive old version
```

---

<a name="section-10"></a>

## 🏗️ Section 10: Production Best Practices and Research Reporting

### 10.1 Research Paper Deployment Subsection Template

> The trained model and preprocessing pipeline were packaged as a unified predictive artifact using a reproducible pipeline. A lightweight user interface was implemented using Streamlit to support interactive inference and decision support. The deployment package includes version pinned dependencies, feature schema validation, and logging mechanisms to ensure reliability and reproducibility.

---

## 🎓 Final Takeaway

```
A model in a notebook is research.
A model in a tool is impact.
A monitored model is responsible science.
```
