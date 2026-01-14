# Module 03: Data Selection and Acquisition

**Audience:** Transportation Engineering and Traffic Engineering Researchers  
**Level:** Beginner to Intermediate (Non-CS Background Friendly)  
**Status:** ✅ Complete  
**Last Updated:** January 2026  

---

## Module Overview

Data selection and acquisition form the foundation of empirical transportation research.  
This module introduces **how to identify, evaluate, and collect data** for transportation and traffic engineering studies, with emphasis on **open data**, **ethical research practice**, and **publication-quality workflows**.

This module is designed for researchers **without a computer science background**.

---

## Prerequisites

- Module 01: Introduction to Data-Driven Transportation Research  
- Module 02: Research Problem Formulation  

---

## Learning Objectives

By the end of this module, you will be able to:

- Identify suitable data types for transportation research
- Locate high-quality open and free transportation datasets
- Select data based on research questions rather than convenience
- Apply ethical and privacy principles in data collection
- Assess data quality before modeling
- Plan a reproducible data acquisition strategy

---

## 3.1 Why Data Selection Matters in Transportation Research

Transportation research relies primarily on **observational data**, not controlled experiments.  
This makes data quality and suitability critical.

Poor data selection can lead to:
- Biased results
- Invalid conclusions
- Model overfitting
- Rejection during peer review

Data selection is therefore a **scientific decision**, not merely a technical step.

---

## 3.2 Types of Data in Transportation and Traffic Engineering

### 3.2.1 Data by Structure

| Data Type | Description | Examples |
|---------|------------|----------|
| Structured | Tabular rows and columns | Traffic counts, crash databases |
| Semi-structured | Fixed schema but complex | GTFS Realtime, JSON APIs |
| Unstructured | Free-form content | Accident narratives, CCTV footage |

---

### 3.2.2 Data by Temporal Nature

| Category | Definition | Example |
|-------|------------|--------|
| Cross-sectional | One-time snapshot | Household travel survey |
| Time series | Continuous over time | Speed every 30 seconds |
| Panel | Same unit tracked over time | Vehicle trajectories |

---

### 3.2.3 Data by Spatial Representation

| Spatial Scale | Example |
|-------------|--------|
| Point-based | Bus stop boarding counts |
| Link-based | Road segment speed |
| Network-based | Origin–destination matrices |
| Area-based | Zone-level emissions |

---

## 3.3 Open and Free Transportation Data Sources

All data sources below are **free**, **open**, and **widely used in peer-reviewed research**.

---

### 3.3.1 Government and Public Agency Data

Commonly available through **open data portals**.

**Typical datasets**
- Traffic volume and speed
- Crash and safety records
- Infrastructure inventories
- Policy and planning indicators

| Source Type | Example Use Case |
|-----------|----------------|
| National transport agencies | Policy evaluation |
| City open data portals | Urban traffic analysis |
| Police departments | Crash severity modeling |

---

### 3.3.2 Public Transport and GTFS Data

GTFS (General Transit Feed Specification) is a global standard.

| Dataset | Description | Applications |
|-------|-------------|--------------|
| GTFS Static | Routes, stops, schedules | Accessibility analysis |
| GTFS Realtime | Delays, vehicle positions | Service reliability |
| AVL GPS data | Vehicle trajectories | Headway and bunching |

---

### 3.3.3 Traffic Sensors and ITS Data

| Sensor Type | Data Collected |
|-----------|----------------|
| Loop detectors | Volume, occupancy |
| Bluetooth sensors | Travel time |
| Radar sensors | Speed and spacing |
| ANPR cameras | OD estimation |

---

### 3.3.4 Road Safety and Accident Data

| Data Component | Typical Fields |
|--------------|---------------|
| Location | Latitude, longitude |
| Time | Date, hour |
| Severity | Fatal, injury, PDO |
| Environment | Weather, lighting |

Used for:
- Crash prediction
- Hotspot analysis
- Safety performance functions

---

### 3.3.5 Survey and Behavioral Data

| Survey Type | Application |
|------------|------------|
| Household travel survey | Mode choice |
| Stated preference | EV adoption |
| Revealed preference | Route choice |

> **Note:** Survey data requires ethics approval and informed consent.

---

### 3.3.6 Social Media and Textual Data

| Source | Research Use |
|------|-------------|
| Twitter X | Incident detection |
| Facebook public pages | Sentiment analysis |
| Online reviews | Service quality assessment |

⚠ Only **publicly accessible content** may be used.

---

## 3.4 Data Acquisition Methods

### 3.4.1 Direct Download (Recommended for Beginners)

Formats commonly used:
- CSV
- Excel
- Parquet
- Shapefiles

Advantages:
- Simple
- Transparent
- Easy to document

---

### 3.4.2 APIs (Application Programming Interfaces)

Used for **dynamic or real-time data**.

Conceptual workflow:


Examples:
- Traffic speed APIs
- Public transport APIs
- Weather APIs

No advanced programming is required initially.

---

### 3.4.3 Web Scraping (Advanced)

Used when data is public but not downloadable.

⚠ Must comply with:
- Terms of service
- Ethical research standards
- Journal policies

---

## 3.5 Ethical and Privacy Considerations

Transportation data often reflects **human mobility behavior**.

### Core Ethical Principles

| Principle | Explanation |
|---------|-------------|
| Anonymization | Remove personal identifiers |
| Aggregation | Prefer zone-level analysis |
| Consent | Required for surveys |
| Transparency | Clear data description |

Most journals require an **Ethics Statement**.

---

## 3.6 Data Quality Assessment

### 3.6.1 Core Quality Dimensions

| Dimension | Key Question |
|---------|--------------|
| Completeness | Are values missing |
| Accuracy | Are values realistic |
| Consistency | Are units consistent |
| Timeliness | Is data outdated |
| Bias | Is sample representative |

---

### 3.6.2 Transportation-Specific Checks

- Speed greater than 200 km/h is unrealistic
- Negative traffic volume is invalid
- Duplicate GPS points indicate sensor errors
- Spatial outliers often reflect GPS drift

---

## 3.7 Planning a Data Collection Strategy

Always follow a **research-driven approach**.

### Step-by-Step Strategy

1. Define the research question
2. Identify required variables
3. Map variables to data sources
4. Check availability and coverage
5. Estimate preprocessing effort
6. Document assumptions

---

## 3.8 Documentation and Reproducibility

Create a **Data Description Table** for your paper.

| Item | Description |
|----|-------------|
| Data source | Agency or provider |
| Time period | Start and end |
| Spatial coverage | City or region |
| Variables | Key features |
| Limitations | Known issues |

This is essential for **Q1 journal submissions**.

---

## 3.9 Common Mistakes to Avoid

- Collecting data without a clear research question
- Ignoring missing values
- Mixing incompatible spatial scales
- Using outdated datasets
- Failing to document preprocessing

---

## 3.10 Module Summary

After completing this module, you should be able to:

- Select appropriate transportation datasets
- Use open and free data sources confidently
- Address ethics and privacy concerns
- Evaluate data quality before modeling
- Prepare for data preprocessing and analysis

---

## Next Module

**Module 04: Data Cleaning, Preprocessing, and Exploratory Analysis**

---

## Suggested Extensions

- Hands-on exercises with real datasets  
- Case studies for safety, transit, and traffic flow  
- Slide deck version for teaching  
- IEEE and TRB-aligned research examples  

---

**Contributions are welcome.**  
Please follow the guidelines in `CONTRIBUTING.md`.
