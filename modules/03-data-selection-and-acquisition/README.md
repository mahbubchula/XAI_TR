# **Module 03: Data Selection and Acquisition for Transportation and Traffic Engineering Research**

**Audience:** Transportation Engineering and Traffic Engineering Researchers
**Level:** Beginner to Intermediate (Non-CS Background Friendly)
**Status:** ✅ Complete
**Last Updated:** January 2026

---

## 📋 Module Overview

Data selection and acquisition constitute the **most critical empirical decision** in transportation and traffic engineering research.
Unlike laboratory sciences, transportation studies rely predominantly on **observational, opportunistic, and administrative data**, which introduces unavoidable bias, uncertainty, and measurement error.

This module provides a **research-driven, publication-oriented framework** for selecting, evaluating, and acquiring transportation data.
The emphasis is on **scientific defensibility**, **ethical responsibility**, and **reproducibility**, not merely technical data collection.

This module is explicitly designed for researchers **without a computer science background**, but it reflects the **expectations of top-tier journals**.

---

## ✅ Prerequisites

* **Module 01:** Foundations of AI, ML, and XAI for Research
* **Module 02:** Research Problem Formulation

You should already have:

* A clearly defined research question
* Identified dependent and independent variables
* An understanding of why data-driven methods are appropriate

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

* Select transportation data **based on research questions**, not availability
* Distinguish between data suitability, data convenience, and data bias
* Identify and access **high-quality open transportation datasets**
* Understand strengths and limitations of different transportation data types
* Apply ethical, privacy, and governance principles in mobility data
* Perform **pre-modeling data quality screening**
* Design a **reproducible and auditable data acquisition strategy**
* Prepare data documentation suitable for **Q1 journal submission**

---

## **3.1 Why Data Selection Matters in Transportation Research**

Transportation research is fundamentally **observational**, not experimental.

Researchers rarely control:

* Traffic demand
* Weather
* Human behavior
* Infrastructure conditions

As a result, **data quality and relevance directly determine scientific validity**.

### Consequences of Poor Data Selection

Poor data decisions lead to:

* Spurious correlations
* Overfitted models
* Misleading policy recommendations
* Ethical violations
* Rejection during peer review

In transportation research, **data selection is a methodological decision**, not a preprocessing step.

---

## **3.2 Conceptual Framework for Transportation Data**

Transportation data can be classified along **four orthogonal dimensions**:

1. Structural form
2. Temporal resolution
3. Spatial representation
4. Behavioral interpretation

A dataset is suitable **only if all four dimensions align with the research question**.

---

## **3.3 Types of Data in Transportation and Traffic Engineering**

### **3.3.1 Data by Structural Form**

| Data Type       | Description            | Examples                     | Typical Use       |
| --------------- | ---------------------- | ---------------------------- | ----------------- |
| Structured      | Fixed rows and columns | Traffic counts, crash tables | Regression, ML    |
| Semi-structured | Schema with hierarchy  | GTFS, JSON APIs              | Network analytics |
| Unstructured    | Free-form content      | Accident narratives, video   | NLP, CV           |

**Key Insight:**
Structured data is easiest to analyze, but unstructured data often contains **richer behavioral information**.

---

### **3.3.2 Data by Temporal Resolution**

| Category        | Definition           | Example                 | Typical Pitfall    |
| --------------- | -------------------- | ----------------------- | ------------------ |
| Cross-sectional | Single snapshot      | Household travel survey | No dynamics        |
| Time series     | Continuous over time | Speed every 30 seconds  | Non-stationarity   |
| Panel           | Same unit over time  | Vehicle trajectories    | Missing continuity |

Transportation systems are **dynamic**, making temporal alignment critical.

---

### **3.3.3 Data by Spatial Representation**

| Spatial Unit  | Example       | Research Implication   |
| ------------- | ------------- | ---------------------- |
| Point-based   | Bus stops     | High spatial precision |
| Link-based    | Road segments | Network dependency     |
| Network-based | OD matrices   | Flow conservation      |
| Area-based    | Traffic zones | Aggregation bias       |

⚠ Mixing spatial scales without justification is a **common reviewer criticism**.

---

### **3.3.4 Data by Behavioral Meaning**

| Data Type      | What It Represents  |
| -------------- | ------------------- |
| Traffic counts | Supply utilization  |
| GPS traces     | Individual movement |
| Surveys        | Stated preferences  |
| Ticketing data | Revealed behavior   |

**Important:**
Behavioral interpretation must be **explicitly stated** in your paper.

---

## **3.4 Open and Free Transportation Data Sources**

All sources below are **free**, **public**, and **widely cited in peer-reviewed literature**.

---

### **3.4.1 Government and Public Agency Data**

Typically available through:

* National open data portals
* City open data platforms
* Transport authority websites

**Common datasets include:**

* Traffic volumes and speeds
* Crash and safety records
* Road inventory
* Emissions and environment

| Provider Type      | Typical Research Use |
| ------------------ | -------------------- |
| National agencies  | Policy evaluation    |
| Municipal portals  | Urban mobility       |
| Police departments | Safety modeling      |

---

### **3.4.2 Public Transport and GTFS Data**

GTFS is a **global standard** for public transport data.

| Dataset       | Description              | Applications  |
| ------------- | ------------------------ | ------------- |
| GTFS Static   | Routes, stops, schedules | Accessibility |
| GTFS Realtime | Delays, positions        | Reliability   |
| AVL GPS       | Vehicle movement         | Bunching      |

GTFS data is especially powerful for:

* Network-level analysis
* Service quality assessment
* Real-time decision support

---

### **3.4.3 Traffic Sensors and ITS Data**

| Sensor         | Data Collected    | Typical Bias      |
| -------------- | ----------------- | ----------------- |
| Loop detectors | Volume, occupancy | Lane bias         |
| Bluetooth      | Travel time       | Sample bias       |
| Radar          | Speed             | Angle sensitivity |
| ANPR           | OD flows          | Privacy concerns  |

Sensor limitations must be **explicitly acknowledged**.

---

### **3.4.4 Road Safety and Accident Data**

| Attribute   | Typical Fields    |
| ----------- | ----------------- |
| Location    | Coordinates       |
| Time        | Timestamp         |
| Severity    | Injury level      |
| Environment | Weather, lighting |

Used for:

* Crash prediction
* Black-spot analysis
* Safety performance functions

⚠ Under-reporting bias is common and must be discussed.

---

### **3.4.5 Survey and Behavioral Data**

| Survey Type         | Application  |
| ------------------- | ------------ |
| Household travel    | Mode choice  |
| Stated preference   | EV adoption  |
| Revealed preference | Route choice |

⚠ Requires:

* Ethics approval
* Informed consent
* Secure data handling

---

### **3.4.6 Social Media and Textual Data**

| Source            | Research Use       |
| ----------------- | ------------------ |
| Twitter X         | Incident detection |
| Facebook (public) | Public sentiment   |
| Online reviews    | Service quality    |

⚠ Only **public content** is permissible.
Private or scraped personal data is ethically unacceptable.

---

## **3.5 Data Acquisition Methods**

### **3.5.1 Direct Download (Recommended)**

Formats:

* CSV
* Excel
* Parquet
* Shapefiles

Advantages:

* Simple
* Transparent
* Reviewer-friendly

---

### **3.5.2 APIs (Dynamic Data)**

Used for:

* Real-time traffic
* Public transport feeds
* Weather integration

Conceptual workflow:

```
Request → Response → Storage → Documentation
```

No advanced programming is required initially.

---

### **3.5.3 Web Scraping (Advanced and Sensitive)**

Used only when:

* Data is public
* No download option exists

⚠ Must comply with:

* Terms of service
* Institutional ethics
* Journal policies

---

## **3.6 Ethical and Privacy Considerations**

Transportation data reflects **human mobility**, which is inherently sensitive.

### Core Principles

| Principle     | Explanation           |
| ------------- | --------------------- |
| Anonymization | Remove identifiers    |
| Aggregation   | Prefer zones          |
| Consent       | Mandatory for surveys |
| Transparency  | Clear disclosure      |

Most Q1 journals require:

* Ethics statement
* Data governance description

---

## **3.7 Data Quality Assessment Before Modeling**

### **3.7.1 Core Quality Dimensions**

| Dimension    | Question           |
| ------------ | ------------------ |
| Completeness | Missing values     |
| Accuracy     | Realistic values   |
| Consistency  | Unit alignment     |
| Timeliness   | Temporal relevance |
| Bias         | Representativeness |

---

### **3.7.2 Transportation-Specific Sanity Checks**

* Speed > 200 km/h → sensor error
* Negative flow → invalid
* Duplicate GPS points → device fault
* Sudden jumps → GPS drift

These checks must be **reported**, not hidden.

---

## **3.8 Designing a Data Collection Strategy**

Always follow a **research-driven workflow**.

### Step-by-Step Framework

1. Define research question
2. Identify required variables
3. Map variables to datasets
4. Check spatial and temporal coverage
5. Assess preprocessing effort
6. Document assumptions and exclusions

This process should be **explicitly described in your methodology section**.

---

## **3.9 Documentation and Reproducibility**

Every paper must include a **Data Description Table**.

| Item        | Description   |
| ----------- | ------------- |
| Source      | Provider      |
| Period      | Time span     |
| Coverage    | Spatial scope |
| Variables   | Features      |
| Limitations | Known issues  |

This table is **mandatory** in most Q1 journals.

---

## **3.10 Common Data-Related Mistakes**

* Data collection without a research question
* Using data simply because it is available
* Ignoring missingness patterns
* Mixing incompatible spatial units
* Using outdated datasets
* Poor documentation

These errors are frequently cited in **reviewer rejection comments**.

---

## **3.11 Module Summary**

After completing this module, you should be able to:

* Select transportation data scientifically
* Use open data confidently
* Address ethics and privacy
* Screen data quality rigorously
* Prepare for preprocessing and modeling

---

## **Next Module**

**Module 04: Data Cleaning, Preprocessing, and Exploratory Analysis**

---

## **Suggested Extensions**

* Hands-on notebooks with real datasets
* Case studies: safety, transit, congestion
* Teaching slide deck
* IEEE / TRB / Transportation Research examples

---

### **Final Framing Statement**

> In transportation research,
> models fail because data fails first.
> Scientific rigor begins at data selection.

---
