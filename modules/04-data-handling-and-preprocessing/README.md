# Module 04: Data Handling and Preprocessing

**Audience:** Transportation Engineering and Traffic Engineering Researchers  
**Level:** Beginner to Intermediate (Non-CS Background Friendly)  
**Status:** ✅ Complete  
**Last Updated:** January 2026  

---

## Module Overview

Raw transportation data is **never ready for analysis or modeling**.  
Before applying machine learning, statistical models, or simulation tools, data must be **cleaned, validated, and transformed**.

This module provides a **step-by-step, research-oriented guide** to data handling and preprocessing using **Python and pandas**, written explicitly for **non-computer science backgrounds**.

The focus is not only technical execution, but also **scientific rigor, interpretability, and reproducibility**, which are essential for **Q1 journal publications**.

---

## Prerequisites

- Module 01: Introduction to Data-Driven Transportation Research  
- Module 02: Research Problem Formulation  
- Module 03: Data Selection and Acquisition  
- Basic Python familiarity (all examples are fully explained)

---

## Learning Objectives

By the end of this module, you will be able to:

- Load and inspect datasets using pandas
- Understand the physical meaning of data variables
- Detect and handle missing values and outliers
- Clean transportation datasets systematically
- Transform and normalize features correctly
- Perform basic feature engineering
- Split data into training and testing sets
- Prepare datasets for ML, XAI, and simulation studies

---

## 4.1 Why Data Preprocessing Is Critical in Transportation Research

Transportation data is typically:

- Collected for operational purposes, not research
- Subject to sensor malfunction
- Affected by human reporting errors
- Spatially and temporally inconsistent

Machine learning models **do not correct bad data**.  
They often **learn the errors**.

Poor preprocessing leads to:
- Inflated model performance
- Invalid behavioral interpretation
- Reviewer criticism
- Rejection during peer review

Data preprocessing is therefore a **scientific responsibility**, not a technical afterthought.

---

## 4.2 Loading Data Using pandas

### 4.2.1 Importing Required Libraries

```python
import pandas as pd
import numpy as np
These two libraries are sufficient for most preprocessing tasks.

4.2.2 Loading Common Transportation Data Formats
CSV Files
df = pd.read_csv("traffic_data.csv")

Excel Files
df = pd.read_excel("survey_data.xlsx")

Parquet Files (Large Datasets)
df = pd.read_parquet("vehicle_trajectories.parquet")

JSON Files (APIs)
df = pd.read_json("api_response.json")

4.2.3 Initial Inspection Checklist

Always inspect data before any processing.

df.head()
df.tail()
df.shape
df.columns
df.info()


Key questions to answer:

How many rows and columns exist

What does each column represent

Are data types correct

Are missing values present

4.3 Understanding Data Semantics (Extremely Important)

Never treat columns as abstract variables.

Each variable must be understood in engineering terms.

Ask:

What does this variable physically represent

What unit is used

What is a realistic range

Examples:

Speed should not exceed realistic limits

Traffic volume cannot be negative

Density must be consistent with lane count

Time variables must follow logical order

Create a variable dictionary early.

Example:

Variable	Meaning	Unit
speed	Vehicle speed	km/h
volume	Traffic flow	veh/h
density	Traffic density	veh/km

This improves clarity and publication quality.

4.4 Handling Missing Values
4.4.1 Identifying Missing Data
df.isnull().sum()


Missing values are common due to:

Sensor failures

GPS signal loss

Survey non-response

Data merging errors

4.4.2 Types of Missingness (Conceptual)
Type	Description
MCAR	Missing completely at random
MAR	Missing related to other variables
MNAR	Missing related to the missing value itself

Understanding this helps justify your handling strategy.

4.4.3 Common Handling Strategies
Strategy	When to Use
Drop rows	Very small proportion missing
Mean or median	Continuous variables
Mode	Categorical variables
Forward fill	Time-series data

Example:

df["speed"] = df["speed"].fillna(df["speed"].median())


⚠ Always justify your approach in the methodology section.

4.5 Detecting and Handling Outliers
4.5.1 Why Outliers Matter in Transportation Data

Outliers may represent:

Sensor malfunction

Data entry errors

Rare but important traffic events

Removing all outliers blindly is scientifically incorrect.

4.5.2 Statistical Detection Methods
Interquartile Range (IQR)
Q1 = df["speed"].quantile(0.25)
Q3 = df["speed"].quantile(0.75)
IQR = Q3 - Q1

lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

4.5.3 Engineering-Based Thresholds

Use domain knowledge.

Examples:

Speed above 200 km/h is unrealistic

Density above jam density is invalid

Negative delay is impossible

df = df[df["speed"] <= 200]


Always explain whether outliers were:

Removed

Capped

Retained as rare events

4.6 Data Cleaning Techniques
4.6.1 Removing Duplicate Records
df = df.drop_duplicates()


Duplicates often occur after merging datasets.

4.6.2 Fixing Data Types
df["timestamp"] = pd.to_datetime(df["timestamp"])
df["lane_count"] = df["lane_count"].astype(int)


Incorrect data types can silently corrupt analysis.

4.6.3 Standardizing Units

Ensure unit consistency.

Example:

Convert speed from m/s to km/h

df["speed_kmh"] = df["speed_ms"] * 3.6

4.7 Data Transformation and Normalization
4.7.1 Why Transformation Is Needed

Many ML models assume:

Comparable feature scales

No extreme skewness

Transportation variables often violate these assumptions.

4.7.2 Common Scaling Methods
Min-Max Scaling
df["speed_scaled"] = (
    df["speed"] - df["speed"].min()
) / (
    df["speed"].max() - df["speed"].min()
)

Standardization
df["speed_std"] = (
    df["speed"] - df["speed"].mean()
) / df["speed"].std()


Choose scaling after understanding model requirements.

4.8 Feature Engineering Basics

Feature engineering converts raw data into meaningful explanatory variables.

4.8.1 Creating Time-Based Features
df["hour"] = df["timestamp"].dt.hour
df["day_of_week"] = df["timestamp"].dt.dayofweek


These are essential for capturing traffic patterns.

4.8.2 Aggregation Features
df["avg_speed_by_link"] = df.groupby("link_id")["speed"].transform("mean")


Captures spatial context.

4.8.3 Interaction Features
df["flow_density"] = df["volume"] * df["density"]


Used frequently in traffic flow modeling.

4.9 Train-Test Splitting
4.9.1 Why Splitting Is Necessary

Models must be evaluated on unseen data.

Without splitting:

Performance is overestimated

Results are misleading

4.9.2 Random Split
from sklearn.model_selection import train_test_split

X = df.drop("target", axis=1)
y = df["target"]

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

4.9.3 Time-Based Split (Recommended for Traffic Data)
train = df[df["timestamp"] < "2024-01-01"]
test = df[df["timestamp"] >= "2024-01-01"]


Prevents data leakage in time-series studies.

4.10 Data Leakage: A Critical Warning

Data leakage occurs when:

Future information enters training data

Aggregations use full dataset

Scaling is applied before splitting

Leakage leads to invalid scientific conclusions.

Always:

Split first

Then preprocess within training data only

4.11 Preprocessing Documentation for Publications

Every paper should include:

Item	Description
Missing value handling	Method and rationale
Outlier treatment	Criteria used
Feature transformations	Scaling and encoding
Train-test split	Ratio and method

This is often checked by reviewers.

4.12 Common Mistakes by Non-CS Researchers

Filling missing values without justification

Removing outliers without domain reasoning

Mixing spatial and temporal scales

Applying normalization before splitting

Not documenting preprocessing steps

4.13 Module Summary

After completing this module, you can:

Prepare raw transportation data for modeling

Apply scientifically justified preprocessing

Avoid common methodological errors

Produce reproducible and publication-ready datasets

Next Module

Module 05: Exploratory Data Analysis and Visualization

Suggested Extensions

Jupyter notebook exercises

Case studies with GTFS and crash data

Preprocessing checklists for journals

Reusable preprocessing templates

Contributions are welcome.
Please follow CONTRIBUTING.md.


---

### What will happen next
In the **next response**, I can optionally:

- Add **hands-on exercises section**
- Add **real transportation datasets links**
- Convert this module into **teaching slides**
- Align preprocessing steps with **IEEE Access methodology style**

I will wait for your instruction after confirming you received **Module 04 fully**.
