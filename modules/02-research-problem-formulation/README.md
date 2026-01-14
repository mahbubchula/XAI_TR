# Module 02: Research Problem Formulation
<img width="1408" height="768" alt="Gemini_Generated_Image_g3z5r1g3z5r1g3z5" src="https://github.com/user-attachments/assets/bb9ebf26-7f63-455b-8cbd-b20f0aa03c6e" />





![Status](https://img.shields.io/badge/Module-Research-blue)
![Level](https://img.shields.io/badge/Level-Beginner-green)

## 📋 Overview

Turning a research question into a well-defined Machine Learning (ML) problem is the most critical and foundational step in Artificial Intelligence research. Many AI projects fail—not because of poor models—but because the problem itself is vaguely defined, incorrectly framed, or misaligned with available data. This module focuses on helping learners avoid these pitfalls by teaching a structured, research-oriented approach to problem formulation.

In this module, you will learn how to critically evaluate whether a research question truly benefits from Machine Learning, and how to transform broad, abstract ideas into precise, measurable, and actionable ML problems. You will explore how to identify the appropriate ML problem type (classification, regression, clustering, or anomaly detection), define clear objectives and success metrics, and align your research goals with data availability, ethical constraints, and explainability requirements.

Beyond technical framing, this module emphasizes research thinking—helping you understand why certain problems are suitable for ML, what assumptions are being made, and how your formulation choices impact model design, evaluation, and interpretation. Special attention is given to Explainable AI (XAI) considerations, ensuring that your problem formulation supports transparency, trust, and real-world usability from the very beginning.

By the end of this module, you will be able to produce a complete problem formulation document that serves as a blueprint for the rest of your AI research pipeline, including data collection, modeling, evaluation, and reporting. This module is designed to build strong conceptual foundations for students, researchers, and practitioners before they write a single line of code.


**Duration:** 3-4 hours  
**Difficulty:** Beginner

## ✅ Prerequisites

Before starting this module, you should:
- [x] Have completed [Module 01 - Introduction](../01-introduction/)
- [x] Understand what AI, ML, and XAI are
  - **Artificial Intelligence (AI)**
  - **Machine Learning (ML)**
  - **Explainable Artificial Intelligence (XAI)**
- [x] Have a research area or question in mind (or be curious to learn!)
  - Have a **general research area, problem domain, or preliminary research question** in mind  
  *(a fully defined research problem is not required)*

## 🎯 Learning Objectives

This module focuses on developing a strong conceptual and research-oriented foundation for Machine Learning problem formulation. Rather than jumping directly into algorithms or code, learners will gain the ability to critically think about **whether Machine Learning is appropriate**, **how a problem should be framed**, and **what success means** in a research context.

By the end of this module, you will be able to:

- 🔍 **Critically Evaluate ML Suitability**  
  Analyze a research question to determine whether Machine Learning is an appropriate and effective approach compared to traditional methods.

- 🧠 **Translate Research Questions into ML Problems**  
  Convert broad, abstract, or ambiguous research ideas into clear, structured, and well-defined Machine Learning problem statements.

- 🏷️ **Identify the Correct ML Problem Type**  
  Distinguish between classification, regression, clustering, and anomaly detection problems, and select the most suitable type for a given research goal.

- 📐 **Define Clear Objectives and Success Metrics**  
  Establish measurable performance criteria and evaluation metrics that align with the research objectives and domain requirements.

- 🗂️ **Assess Data Requirements and Constraints**  
  Identify required data sources, feature types, data quantity, quality issues, and practical constraints that may affect model development.

- 📝 **Develop a Formal Problem Formulation Document**  
  Create a structured, research-ready document that clearly defines the ML problem, assumptions, inputs, outputs, evaluation strategy, ethical considerations, and explainability needs.

- ⚖️ **Incorporate Explainability and Ethical Considerations**  
  Recognize the importance of explainability (XAI), fairness, and ethical constraints, and integrate them into the problem formulation process from the outset.


Below is a concise summary of the key skills and competencies you will develop by completing this module. 
These learning objectives outline what you will be able to do in practice, helping you understand how this module prepares you to formulate clear, effective, and research-ready Machine Learning problems.

| Skill Area | What You Will Learn |
|-----------|---------------------|
| 🔍 ML Suitability | Critically evaluate whether a research question truly benefits from Machine Learning compared to traditional approaches |
| 🧩 Problem Framing | Transform vague or broad research ideas into clear, well-defined, and actionable ML problem statements |
| 🏷️ Problem Type Selection | Identify and select the correct ML problem type (classification, regression, clustering, anomaly detection) |
| 📐 Evaluation & Metrics | Define meaningful, measurable success metrics and evaluation strategies aligned with research goals |
| 🗂️ Data Awareness | Assess data requirements, availability, quality issues, imbalance, and practical constraints |
| 🧠 Explainability & Ethics | Recognize explainability (XAI), fairness, and ethical considerations and incorporate them early |
| 📝 Documentation | Develop a structured, research-ready ML problem formulation document for reproducibility and reporting |

## 📚 Module Content

### Section 1: When Should You Use Machine Learning?

Before applying Machine Learning, it is essential to ask a fundamental question:  
**Does this research problem actually benefit from ML?**  
Using ML where it is not needed can waste time, data, and computational resources. This section helps you build the intuition to make informed decisions.

---

#### ✅ When Machine Learning Is a Good Fit

Machine Learning is well-suited for a research problem when **patterns exist in data that are difficult to define manually**, and sufficient examples are available for learning.

| Situation | Example | Why ML Works |
|---------|--------|-------------|
| 📊 **Patterns exist in data** | Predicting diseases from patient symptoms and lab results | Historical data reveals consistent relationships between symptoms and diagnoses |
| 🧠 **Problem is too complex for simple rules** | Identifying spam emails | Spam patterns change and involve many interacting features |
| 📁 **Sufficient data is available** | Classifying plant species from images | ML improves as it learns from many labeled examples |
| 🔮 **Prediction or classification is required** | Forecasting crop yield using weather and soil data | ML excels at discovering predictive relationships |
| ⏱️ **Manual analysis is impractical** | Analyzing thousands of research papers | ML can scale to large datasets efficiently |

---

#### ❌ When Machine Learning May NOT Be the Best Choice

Machine Learning is not always the right tool. In some cases, simpler or more transparent methods are preferable.

| Situation | Explanation |
|---------|-------------|
| 📉 **Very little data is available** | With only 20–30 samples, traditional statistical methods are often more reliable |
| 🧮 **Simple rules already solve the problem** | If a clear rule exists (e.g., *if temperature > 100°C, water boils*), ML adds no value |
| 🔍 **Full explainability is required from the start** | Highly regulated domains may require transparent, rule-based systems |
| ⚠️ **Cost of errors is extremely high** | Life-critical systems may require provably safe approaches |
| ❓ **Relevant data is missing** | ML cannot compensate for data that does not reflect the target outcome |

---
#### 📌 Mini Case Example

**Scenario:** A researcher wants to detect fake news articles.

- Data: Thousands of labeled news articles
- Problem: Complex linguistic patterns
- Output: Fake / Real label

**Decision:** ✅ Machine Learning is appropriate because simple rules cannot capture language complexity.

#### 🧠 Key Insight

> **Machine Learning should be chosen because it adds value—not because it is fashionable.**  
> A well-formulated research problem always starts with selecting the *right tool* for the task.
--


### Section 2: Types of Machine Learning Problems

Before selecting algorithms or building models, it is essential to clearly understand **what type of Machine Learning problem you are trying to solve**. Machine Learning problems differ primarily in **the nature of their outputs**, the **availability of labeled data**, and the **goal of the analysis**—whether it is prediction, estimation, discovery, or detection.

In research settings, misidentifying the problem type is a common and costly mistake. For example, treating a continuous prediction task as a classification problem can lead to information loss, while using unsupervised methods when labeled data already exists can result in inefficient or misleading analyses. A correct problem-type formulation ensures that the **chosen models, evaluation metrics, data requirements, and explainability techniques** are all aligned with the research objective.

Broadly, most Machine Learning research problems fall into four major categories: **classification**, **regression**, **clustering**, and **anomaly detection**. Each category answers a different kind of research question, requires different forms of data, and serves different scientific goals. This section introduces these problem types, explains their defining characteristics, and provides research-oriented examples to help you accurately identify the category that best matches your research question.


---

## 🧩 At a Glance: ML Problem Types

| Problem Type | Output | Key Question | Example |
|-------------|--------|--------------|--------|
| 🏷️ Classification | Category | *Which class?* | Disease diagnosis |
| 📈 Regression | Number | *How much?* | Temperature prediction |
| 🧬 Clustering | Groups | *What patterns exist?* | Patient subgroups |
| 🚨 Anomaly Detection | Normal / Abnormal | *Is this unusual?* | Fraud detection |

---

## 🏷️ 2.1 Classification Problems
Classification problems focus on assigning each input instance to one or more **predefined categories or labels**. The goal is to learn a decision boundary from labeled examples so that the model can correctly categorize unseen data. Classification is one of the most widely used ML problem types, especially in research domains where decisions are categorical rather than numerical.

**Ask this question:**  
> *“Which class does this belong to?”*

**Common forms**
- Binary (2 classes)
- Multi-class (many classes)
- Multi-label (multiple classes per item)

**Examples**
- Is this email spam or not spam?
- What species is this plant?
- Which genres does this movie belong to?

**Research applications**
- Disease diagnosis
- Cell type identification
- Document categorization

🧠 **When to use classification**  
✔ When your output is a **label or category**


---

## 📈 2.2 Regression Problems
Regression problems aim to predict a **continuous numerical value** based on input features. Unlike classification, where outputs are discrete categories, regression outputs are real-valued quantities. These problems are common in scientific research where estimation, forecasting, or measurement prediction is required.


**Ask this question:**  
> *“How much or how many?”*

**Examples**
- What will the temperature be tomorrow?
- How long will a patient stay in the hospital?
- What will be the crop yield this season?

**Research applications**
- Recovery time prediction
- Protein binding affinity estimation
- Energy demand forecasting

🧠 **When to use regression**  
✔ When your output is a **number**


---

## 🧬 2.3 Clustering Problems
Clustering problems involve **grouping similar data points together without predefined labels**. The objective is not prediction, but discovery—uncovering hidden structures or natural groupings within the data. Clustering is especially useful in exploratory research and early-stage data analysis.


**Ask this question:**  
> *“What natural groups exist in this data?”*

**Examples**
- Customer segmentation
- Patient stratification
- Galaxy morphology discovery

**Research applications**
- Treatment response analysis
- Ecosystem identification
- Gene expression analysis

🧠 **When to use clustering**  
✔ When you want **discovery**, not prediction


---

## 🚨 2.4 Anomaly Detection
Anomaly detection focuses on identifying **rare, unusual, or abnormal instances** that deviate significantly from normal patterns in the data. These problems are important in research areas where rare events carry high significance, such as fraud detection, fault diagnosis, or rare disease identification.


**Ask this question:**  
> *“Is this normal or unusual?”*

**Examples**
- Fraud detection
- Equipment failure detection
- Sensor malfunction detection

**Research applications**
- Rare disease detection
- Geological anomaly discovery
- Experimental error identification

🧠 **When to use anomaly detection**  
✔ When **rare events matter more than average cases**

---

## 🧭 How to Choose the Right Problem Type (1-Minute Rule)

- Predict a **category** → 🏷️ Classification  
- Predict a **number** → 📈 Regression  
- Discover **hidden structure** → 🧬 Clustering  
- Detect **rare events** → 🚨 Anomaly Detection  

---

## ⚠️ Common Beginner Confusions

- ❌ Turning a regression problem into classification by arbitrary thresholds  
- ❌ Using clustering when labels already exist  
- ❌ Ignoring imbalance in classification or anomaly detection  
- ❌ Choosing the problem type after seeing model results

---

## 🔑 Core Takeaway

> **Problem type selection is a thinking task, not a coding task.**  
> Get this right, and the rest of your ML pipeline becomes much easier.


--
### Section 3: From Research Question to a Well-Defined ML Problem

Transforming a research question into a well-defined Machine Learning (ML) problem is one of the most important skills in ML research. A research question is often written in broad, human-friendly language (e.g., “Can we detect diseases earlier?”), while an ML problem must be expressed in a precise, testable form that a model can learn from data and that researchers can evaluate objectively.

A **well-defined ML problem** clearly specifies:

- **What the system should learn to do** (the objective)
- **What information it will use** (inputs/features)
- **What it must produce** (outputs/targets)
- **What learning setup fits best** (problem type and supervision)
- **How success will be measured** (metrics + baselines)
- **What constraints matter** (data limits, ethics, compute, explainability)

When these elements are missing, researchers often face common failures such as unclear scope, data mismatch, misleading evaluation, or models that cannot be trusted or reproduced. This section provides a structured approach to reduce ambiguity and turn ideas into research-ready ML tasks.
----
## 🔁 The Problem Formulation Framework

Use this step-by-step framework to transform a broad research idea into a clear, research-ready Machine Learning problem.

```text
Research Question
      ↓
Clarify the objective  
(What do you want to predict or understand?)
      ↓
Define the unit of analysis  
(What represents one data instance?)
      ↓
Select the ML problem type  
(Classification / Regression / Clustering / Anomaly Detection)
      ↓
Specify inputs and outputs  
(Features → Target variable)
      ↓
Assess data requirements  
(Quantity, quality, representativeness, labels)
      ↓
Choose metrics and baselines  
(How will success be measured objectively?)
      ↓
Add constraints  
(Ethics, fairness, privacy, computation, explainability)
      ↓
Well-Defined ML Problem  
(Ready for modeling, experimentation, and evaluation)

```


🧪 Example 1: Biology Research

Biology research focuses on understanding the structure, function, and behavior of living systems, ranging from molecules and cells to organisms and ecosystems. Modern biological research generates large, complex datasets through technologies such as DNA sequencing, proteomics, microscopy, and high-throughput experiments. These data-rich environments make Machine Learning a powerful tool when biological questions are framed carefully.

Biological systems are often highly complex and non-linear, with interactions occurring across multiple scales. As a result, traditional rule-based or purely statistical approaches may struggle to capture hidden patterns in biological data. Machine Learning can help identify relationships, classify biological entities, and make predictions that support discovery and hypothesis generation.

❓ Vague Research Question

“I want to study protein functions.”

Why this is vague:
It does not specify what should be predicted, how data will be used, or how success will be evaluated.

✅ Well-Defined ML Problem

Specific Goal
Predict protein function categories directly from amino acid sequences.

ML Problem Type
Multi-class classification (multiple functional categories).

Input Data
Protein sequences represented as amino acid strings.

Output
Functional class (enzyme, structural protein, transporter, etc.).

Success Metric
Accuracy ≥ 80% on a held-out test dataset.

Why XAI Matters
Researchers must understand which sequence patterns influence predictions to gain biological insight and trust results.

🧠 Learning insight:
A descriptive biological interest becomes actionable only after defining labels, data, and evaluation.
--
🌍 Example 2: Environmental Science

Environmental science focuses on understanding natural systems and human–environment interactions, including climate, ecosystems, air and water quality, and land use. These systems are inherently complex, interconnected, and dynamic, often influenced by long-term trends as well as short-term variability. As a result, environmental research increasingly relies on data-driven approaches, making Machine Learning a valuable tool when problems are carefully formulated.

Environmental datasets are typically large, heterogeneous, and spatiotemporal, coming from sources such as satellite imagery, weather stations, remote sensors, climate models, and historical records. Machine Learning can help uncover patterns, relationships, and trends in these data that are difficult to model using simple rules or traditional analytical methods alone.

❓ Vague Research Question

“I want to predict climate change impacts.”

Why this is vague:
“Impacts” can mean many things (temperature, rainfall, sea level), across different regions and time horizons.

✅ Well-Defined ML Problem

Specific Goal
Predict regional temperature increases over the next decade.

ML Problem Type
Regression (time-series forecasting).

Input Data
Historical climate records, greenhouse gas concentrations, ocean temperature indicators.

Output
Temperature change (°C) for specific regions and years.

Success Metric
Mean Absolute Error (MAE) < 0.5°C compared to benchmark models.

Why XAI Matters
Policymakers and scientists need to know which environmental factors contribute most to predicted changes.

🧠 Learning insight:
Clear temporal and spatial scope is essential in forecasting problems.


🚦 Example 3: Transportation Research

Transportation research focuses on understanding, predicting, and improving the movement of people and goods across transportation systems such as roads, railways, public transit, and logistics networks. With the growth of sensors, GPS devices, traffic cameras, and smart infrastructure, transportation systems now generate large volumes of spatiotemporal data, making them well-suited for Machine Learning approaches.

However, transportation problems are often complex and dynamic. Traffic conditions change over time, depend heavily on location, and are influenced by many interacting factors such as human behavior, weather, road infrastructure, and unexpected events (accidents, roadworks). As a result, successful ML applications in transportation require careful problem formulation.

In Machine Learning–based transportation research, problems typically involve one or more of the following goals:

Prediction (e.g., travel time, congestion level, demand)

Classification (e.g., accident severity, incident type)

Pattern discovery (e.g., identifying traffic regimes or travel behavior)

Anomaly detection (e.g., detecting sensor failures or abnormal traffic patterns)

A key challenge in transportation research is the need to clearly define:

Spatial scope (which roads, intersections, or regions)

Temporal scope (minutes, hours, days, or long-term trends)

Unit of analysis (road segment, vehicle, trip, or time window)

Without these definitions, a transportation research question remains too vague for ML modeling.

❓ Vague Research Question

“I want to improve traffic conditions.”

Why this is vague:

“Improve traffic conditions” is unclear because it does not specify:

What aspect of traffic (congestion, travel time, accidents, emissions)

Which location (city-wide, highways, intersections)

Over what time period (minutes, hours, days)

Without these details, the problem cannot be formulated as an ML task.

✅ Well-Defined ML Problem

Specific Goal
Predict traffic congestion levels on major urban roads 30 minutes in advance to support traffic management and route planning.

ML Problem Type
Regression (time-series forecasting).

Input Data

Historical traffic speed and volume data

Road network information

Time-related features (hour of day, day of week)

Weather conditions (rain, temperature)

Incident data (accidents, road works)

Output
Predicted traffic congestion level (e.g., average speed or congestion index) for specific road segments and time intervals.

Success Metric
Mean Absolute Error (MAE) below a predefined threshold (e.g., MAE < 5 km/h compared to ground-truth speed measurements).

Why XAI Matters
Transportation planners and traffic operators need to understand:

Which factors (weather, time of day, incidents) most influence congestion

Whether predictions align with known traffic patterns
This supports trust, operational decisions, and policy planning.

🧠 Learning Insight:
In transportation research, clearly defining location, time horizon, and prediction target is critical for building useful and deployable ML forecasting models.

📊 Section 4: Defining Success Metrics

Defining success metrics is a critical step in Machine Learning research because metrics determine how model performance is measured, compared, and interpreted. Without clearly defined metrics, it is impossible to know whether a model is effective, whether improvements are meaningful, or whether results are suitable for reporting in a research paper.

A success metric translates a research goal into a quantitative measure. It answers the question:
“What does it mean for this model to perform well?”

Different Machine Learning problems require different evaluation metrics. Choosing an inappropriate metric can lead to misleading conclusions, even if the model appears to perform well.

🧠 Why Success Metrics Matter

Well-chosen success metrics help you:

Determine when a model is good enough for your research objective

Compare multiple models or approaches fairly and objectively

Align model evaluation with real-world or domain-specific priorities

Communicate results clearly to reviewers, stakeholders, and collaborators

Poorly chosen metrics often result in:

Inflated performance claims

Models that optimize the wrong objective

Reviewer criticism due to unclear or inappropriate evaluation

🏷️ Classification 

Classification is a type of Machine Learning problem where the goal is to assign each input to one or more predefined categories or labels. In classification tasks, the output is discrete, meaning it belongs to a fixed set of possible classes.

In classification, the model learns from labeled examples, where each training instance is already associated with a correct class. Based on patterns in the input data, the model learns decision boundaries that allow it to assign labels to new, unseen data.

### 📌 Common Metrics for Classification

| Metric | What It Measures | Use When |
|------|------------------|----------|
| **Accuracy** | Overall correctness of predictions | Classes are balanced and all errors are equally important |
| **Precision** | Correctness of positive predictions | False positives are costly |
| **Recall (Sensitivity)** | Coverage of actual positive cases | Missing positive cases is costly |
| **F1-Score** | Balance between precision and recall | Both false positives and false negatives matter |

---
📈 Regression 

Regression is a type of Machine Learning problem where the goal is to predict a continuous numerical value. Unlike classification, regression outputs are not categories, but real-valued numbers.

Regression models learn relationships between input features and a numerical target variable. These problems are common in scientific and engineering research where estimation, forecasting, or measurement prediction is required.

### 📌 Common Metrics for Regression

| Metric | Description | Use When |
|------|-------------|----------|
| **MAE (Mean Absolute Error)** | Average absolute difference between predictions and actual values | You want errors in interpretable, real-world units |
| **RMSE (Root Mean Square Error)** | Penalizes large errors more heavily | Large prediction errors are especially costly |
| **R² (Coefficient of Determination)** | Proportion of variance explained by the model | Comparing performance against a simple baseline |



## 📂 Section 5: Understanding Your Data Needs
Understanding your data needs is a foundational step in Machine Learning research. Even the most advanced algorithms cannot compensate for insufficient, low-quality, or mismatched data. Before building models, researchers must carefully evaluate whether the available data can realistically support the defined ML problem.

Data needs are not limited to the amount of data. They also include data quality, relevance, representativeness, and labeling. A well-formulated ML problem must be aligned with what the data can provide; otherwise, the model may learn misleading patterns or fail to generalize to real-world scenarios.
### 📊 Data Quantity Guidelines

The following table provides **rough guidelines** for the amount of data typically required for different types of Machine Learning tasks.  
Actual requirements may vary depending on data quality, feature complexity, and model choice.

| ML Task | Typical Minimum | Good | Excellent |
|--------|----------------|------|-----------|
| Simple Classification | 100–200 per class | 1,000 per class | 10,000+ per class |
| Complex Classification | 500–1,000 per class | 5,000 per class | 50,000+ per class |
| Simple Regression | 200–500 examples | 2,000 examples | 10,000+ examples |
| Complex Regression | 1,000–2,000 examples | 10,000 examples | 100,000+ examples |

> **Note:** These are general guidelines. In practice, **data quality often matters more than data quantity**.


✅ Data Quality Checklist

Assessing data quality is essential before building any Machine Learning model. High-quality data ensures that models learn meaningful, reliable, and generalizable patterns, while poor-quality data often leads to misleading results.

🔹 Relevance

Does the data actually relate to the target?

Relevance refers to how directly the input features are connected to the prediction target. If the data does not capture information that influences the outcome, even the best ML model will fail.

Ask whether each feature has a logical or scientific relationship with the target

Irrelevant features add noise and reduce model performance

Domain knowledge is crucial for judging relevance

📌 Example:
Using patient age and blood glucose levels is relevant for diabetes risk prediction, but eye color is not.

🔹 Completeness

How much data is missing?

Completeness measures the extent of missing values in the dataset. Missing data can bias models and reduce usable sample size.

Small amounts of missing data (< 5%) are often manageable

Moderate missingness (5–20%) may require imputation techniques

High missingness (> 20%) may indicate the need for additional data collection

📌 Key consideration:
Understand why data is missing—randomly or systematically—as this affects how it should be handled.

🔹 Label Quality

Who labeled the data, and how reliable are they?

Label quality is critical for supervised learning. Incorrect or inconsistent labels limit the maximum performance a model can achieve.

Labels created by experts are generally more reliable

Multiple annotators may disagree, introducing noise

Consistency across time and annotators should be checked

📌 Example:
Medical diagnoses labeled by specialists are more reliable than self-reported outcomes.

🔹 Representativeness

Does the data cover all relevant conditions?

Representativeness refers to whether the dataset reflects the real-world population or conditions where the model will be used.

Data should include diverse scenarios, locations, and time periods

Rare but important cases should not be excluded

Lack of representativeness leads to biased predictions

📌 Example:
A traffic dataset collected only during daytime may perform poorly at night.

🔹 Balance

Are classes heavily imbalanced?

Class balance is especially important in classification problems. Severe imbalance can cause models to favor the majority class.

Highly imbalanced datasets may produce misleading accuracy

Minority classes often represent critical cases (e.g., fraud, disease)

Special techniques may be required to address imbalance

📌 Example:
If 99% of transactions are normal and 1% are fraudulent, a model predicting “normal” always would have 99% accuracy—but be useless.

🔑 Key Takeaway

High-quality data is relevant, complete, accurately labeled, representative, and balanced.
Addressing data quality issues early prevents misleading models and strengthens the credibility of ML research.

📝 Problem Formulation Worksheet (Explanation)

The Problem Formulation Worksheet is a guided tool designed to help researchers systematically convert a broad research idea into a clear, precise, and research-ready Machine Learning problem. Rather than jumping directly into algorithms or code, this worksheet encourages structured thinking about what the problem is, why it matters, and how it can be solved using ML.

In Machine Learning research, many projects fail not because of poor models, but because the problem itself is vaguely defined, misaligned with data, or evaluated incorrectly. The worksheet helps prevent these issues by forcing clarity at every stage of problem definition.

🎯 Purpose of the Worksheet

The worksheet is designed to help you:

Clearly articulate your research goal

Identify the correct ML problem type

Define precise inputs and outputs

Assess whether your data can support the problem

Plan evaluation and explainability from the start

Create a single reference document for your entire ML project

Once completed, the worksheet becomes the blueprint for data collection, modeling, evaluation, and reporting.


🧩 How the Worksheet Is Structured

### 🔹 Part 1: Research Context

This section helps you clarify the **domain and motivation** behind your research.

**1. What is your research field?**

[Your answer]

Describe the broad academic or applied domain your research belongs to.  
This helps place your ML problem in the correct context and determines:
- Common data sources
- Typical evaluation metrics
- Ethical and explainability expectations

Examples:
- Biology
- Environmental Science
- Medical Research
- Transportation
- Social Science
- Agriculture
- Finance
- Computer Vision
- Natural Language Processing (NLP)

Example answer:
Medical Research

**2. What is your broad research interest?**

(Describe the general topic or area you want to study. This does not need to be a fully defined problem.)

[Your answer]

This should capture the *overall theme* of your research rather than a specific prediction task.  
It helps clarify the motivation behind your work and guides later decisions about data, models, and evaluation.

Examples:
- Early disease detection using patient data
- Climate change impact analysis
- Traffic congestion prediction in urban areas
- Protein function analysis from biological sequences
- Air quality monitoring using sensor data
- Student performance analysis in education systems

Example answer:
Early disease detection using patient data

**3. What specific question do you want to answer?**

(Write a clear and focused research question in natural language.)

[Your answer]

This question should be more specific than your broad research interest and should describe **what you want to understand or predict**.  
At this stage, it does not need to be written in ML terminology, but it should be precise and answerable.

Examples:
- Can we identify patients at high risk of diabetes before diagnosis?
- Can traffic congestion be predicted 30 minutes in advance in urban areas?
- Can satellite data be used to estimate regional temperature changes?
- Can protein sequences be used to predict protein function?
- Can air quality levels be forecasted for the next 24 hours?

Example answer:
Can we identify patients at high risk of diabetes before diagnosis?

🔹 Part 2: ML Problem Definition

This section converts your research idea into a Machine Learning task.

**4. What exactly do you want to predict or discover?**

(Be specific about the prediction target or discovery goal.)

[Your answer]

This question defines the **core objective** of your Machine Learning problem.  
Your answer should clearly state **what the model will produce as output**, leaving no ambiguity.

Guidelines:
- Use precise terms (avoid words like *improve*, *analyze*, or *study*)
- Specify the prediction target or discovery outcome
- Include a time horizon or scope if relevant

Examples:
- Risk category of developing diabetes within 5 years
- Average traffic speed on major roads 30 minutes ahead
- Regional temperature change (°C) over the next decade
- Protein function category based on amino acid sequence
- Air quality index (AQI) for the next 24 hours

Example answer:
Risk category of developing diabetes within 5 years


**5. What type of ML problem is this?**

(Choose the option that best matches your objective.)

[ ] Classification (predicting categories or labels)  
[ ] Regression (predicting continuous numerical values)  
[ ] Clustering (discovering groups or patterns)  
[ ] Anomaly Detection (finding rare or unusual cases)  
[ ] Other: ______________________

This question helps identify the **core Machine Learning task** your research problem belongs to.  
Choosing the correct problem type is critical because it determines:
- The type of models you can use
- The kind of data you need
- The evaluation metrics for measuring success

Guidance:
- Choose **Classification** if your output is a category or label  
  *(e.g., disease / no disease, spam / not spam)*
- Choose **Regression** if your output is a numerical value  
  *(e.g., temperature, price, duration)*
- Choose **Clustering** if you want to discover natural groups without labels  
  *(e.g., patient subgroups, customer segments)*
- Choose **Anomaly Detection** if you want to identify rare or abnormal cases  
  *(e.g., fraud, equipment failure)*

Example selections:
- Diabetes risk (high / low) → ☑ Classification  
- Traffic speed prediction → ☑ Regression  
- Grouping patients by symptoms → ☑ Clustering  
- Detecting fraudulent transactions → ☑ Anomaly Detection


**6. Is the learning setup supervised or unsupervised?**

(Do you have labeled data or not?)

[Your answer]

This question determines **how the model will learn from the data**.  
The learning setup depends on whether your dataset includes **ground-truth labels** for the prediction target.

Guidance:
- Choose **Supervised learning** if:
  - Each data instance has a known label or target value
  - You are training the model using example input–output pairs  
  *(e.g., patient data with known diagnoses)*

- Choose **Unsupervised learning** if:
  - Your data does not include labels
  - The goal is to discover hidden patterns or structures  
  *(e.g., clustering patients by symptoms without predefined categories)*

- In some cases, you may also note:
  - **Semi-supervised learning** (limited labeled data + large unlabeled data)
  - **Self-supervised learning** (labels derived automatically from data)

Examples:
- Predicting disease risk using labeled patient records → **Supervised learning**
- Grouping customers based on purchasing behavior → **Unsupervised learning**
- Detecting anomalies in sensor data without labeled failures → **Unsupervised learning**

Example answer:
Supervised learning (labels available)

🔹 Part 3: Input and Output

This section defines what information the model uses and what it produces.

**7. What input features will you use?**

(List all relevant variables or data sources.)

[Your answer]

Input features are the **information the model will use to make predictions or discover patterns**.  
These features should be directly relevant to the prediction target and supported by domain knowledge.

Guidelines:
- List all variables, measurements, or data sources used as inputs
- Include both raw data and derived features (if applicable)
- Avoid irrelevant or weakly related features
- Mention data modality if useful (tabular, image, text, sensor, time series)

Examples by domain:
- Medical: Age, BMI, blood glucose level, blood pressure, family history, lifestyle factors
- Environmental: Temperature, rainfall, CO₂ concentration, satellite indices, location
- Transportation: Traffic speed, vehicle count, time of day, weather conditions, incident reports
- Biology: Amino acid sequences, gene expression levels, protein length
- Education: Attendance rate, exam scores, assignment submission history

Example answer:
Age, BMI, blood glucose level, family history, lifestyle factors

**8. What is the output variable?**

(Describe exactly what the model will predict.)

[Your answer]

The output variable (also called the **target** or **label**) defines the **final result produced by the Machine Learning model**.  
It should be specified clearly and unambiguously, as it determines the ML problem type, evaluation metrics, and learning setup.

Guidelines:
- Clearly state what the model predicts
- Specify the format of the output (category, number, score, group, etc.)
- Include time horizon or scope if relevant
- Avoid vague terms such as “risk”, “performance”, or “impact” without definition

Examples by problem type:
- Classification: Disease risk (high / low), Spam status (spam / not spam)
- Regression: Temperature change (°C), Travel time (minutes), House price (USD)
- Clustering: Cluster ID representing similar behavior patterns
- Anomaly Detection: Normal / abnormal flag

Examples by domain:
- Medical: Diabetes risk (high / low)
- Environmental: Predicted temperature increase (°C) for a given region and year
- Transportation: Average traffic speed (km/h) for a road segment
- Biology: Protein function category

Example answer:
Diabetes risk (high / low)

🔹 Part 4: Data Assessment

A Machine Learning problem is only as strong as the data used to solve it.  
Before proceeding to model development, it is critical to **assess whether the available data is sufficient, reliable, and appropriate** for the defined ML problem.

Use the following questions to evaluate your data readiness:


**9. How much data do you currently have?

[Your answer]

Provide a quantitative summary of your available data. Include:
- Number of samples or instances
- Time span covered (if applicable)
- Number of classes (for classification problems)
- Data split availability (train / validation / test)

Example:
- Total samples: 8,500 patient records
- Time span: 2015–2024
- Classes: 2 (high risk / low risk)
- Current split: 70% training, 15% validation, 15% test

**10. What is the quality of your data?
Completeness (percentage of missing data):  
[Your answer]

Label reliability (if supervised learning):  
- Who labeled the data?
- How consistent and accurate are the labels?

Representativeness:  
- Does the data cover all relevant populations, conditions, or scenarios?
- Are rare but important cases included?

Class balance (for classification problems):  
- Are the classes evenly distributed?
- If imbalanced, what mitigation strategies might be needed?

**11. What is the quality of your data?**

Assess the quality of your dataset across the following key dimensions.  
Honest answers here are critical for determining whether your ML problem is feasible.

---

**Completeness (percentage of missing data):**
```md
[Your answer]
Example: Approximately 10% of records have missing values, primarily in laboratory test results.

**12. Do you need more data? If so, how will you get it?**

[Your answer]

Indicate whether the currently available data is sufficient to support your Machine Learning problem.

Options:
```md
[ ] No, the current dataset is sufficient  
[ ] Yes, additional data is required

🔹 Part 5: Success Criteria
```
**13. What metrics will you use to evaluate success?**

Define how you will measure whether your Machine Learning model is performing well.
Clearly distinguish between your **primary metric** (main success criterion) and **secondary metrics** (supporting evaluation measures).

---

**Primary metric:**
[Your answer]
Example: Recall


**14. What performance level would make the model useful?**

Define a **clear, quantitative performance threshold** that determines when the model is considered practically useful.
This threshold should be realistic, measurable, and aligned with domain expectations.

[Your answer]

Guidelines:
- Use a **specific numerical threshold**
- Align the threshold with your **primary evaluation metric**
- Base it on domain standards, literature, or baseline performance
- Avoid vague terms like “high accuracy” or “low error”

Examples by problem type:
- Classification: Accuracy above 85%
- Classification (healthcare): Recall ≥ 85% with Precision ≥ 60%
- Regression: MAE below 3 days
- Forecasting: RMSE lower than baseline model by at least 10%
- Anomaly Detection: Recall above 90% for rare events

Example answer:
Accuracy above 85% on a held-out test set.

**15. What would you compare against (baseline)?**

Specify the **baseline method or reference point** against which your ML model’s performance will be compared.
A baseline represents a simple, existing, or commonly accepted approach.

[Your answer]

Why this matters:
- Baselines show whether your model provides **real improvement**
- Reviewers expect ML models to outperform simple or existing methods
- Without a baseline, performance numbers lack context

Guidelines for choosing a baseline:
- Use a **simple and interpretable method**
- Prefer methods already used in your domain
- Choose a baseline that reflects current practice or common heuristics

Common baseline examples:
- Majority class prediction (for classification)
- Mean or median prediction (for regression)
- Rule-based or threshold-based systems
- Expert or human judgment
- Existing statistical or domain-specific models

Examples by domain:
- Medical research: Current clinical guidelines
- Environmental science: Historical averages or physics-based models
- Transportation: Simple time-of-day average traffic models
- Biology: Sequence similarity or rule-based annotation methods

Example answer:
Current clinical guidelines used for diabetes risk screening.

🔹 Part 6: Explainability Needs

16. Why is explainability important for your problem?

Explainability (XAI) refers to the ability to understand why and how a Machine Learning model makes its predictions.
This question asks you to justify why interpretability is necessary for your specific research problem.

Guidelines:

Consider who will use or be affected by the model

Think about trust, accountability, and decision-making

Reflect on ethical, legal, or safety requirements

Explain what could go wrong if the model behaves as a black box

Common reasons explainability is important:

To build trust with domain experts (e.g., doctors, scientists, engineers)

To support decision-making rather than replace it

To identify bias, errors, or spurious correlations

To meet regulatory or ethical requirements

To generate scientific insight, not just predictions

Examples by domain:

Medical: Clinicians must understand why a patient is predicted high-risk

Environmental: Policymakers need to know which factors drive predictions

Transportation: Traffic planners need interpretable reasons for congestion forecasts

Biology: Researchers want biological meaning, not just labels

Example answer:
Explainability is important because clinicians need to understand which factors contribute to a patient being classified as high risk in order to trust and act on the model’s predictions.

17. What would you want the model to explain?

This question asks you to specify what aspects of the model’s behavior should be interpretable.
Rather than explaining the entire model, focus on the key insights that matter for decision-making or scientific understanding.

Guidelines:

Identify which features or patterns should be explained

Decide whether explanations are needed at:

the global level (overall model behavior), or

the local level (individual predictions)

Align explanations with domain needs and stakeholders

Common explanation goals:

Which input features contribute most to predictions?

Why was a specific instance classified or predicted a certain way?

How changes in input variables affect the output?

Whether the model relies on sensible, domain-relevant patterns

Examples by domain:

Medical: Which symptoms or lab results most indicate disease risk?

Environmental: Which environmental factors most influence temperature change?

Transportation: Which factors contribute most to traffic congestion at a given time?

Biology: Which sequence patterns indicate specific protein functions?

Example answer:
The model should explain which clinical features (e.g., blood glucose level, BMI, age) contribute most to predicting high diabetes risk for individual patients.

18. Who needs to understand the explanations?

This question identifies the intended audience for the model’s explanations.
Different audiences require different levels and types of explainability.

Guidelines:

List all stakeholders who will interpret or rely on the model’s outputs

Consider their technical background and decision-making role

Tailor explanations to the needs of each group

Common audiences:

Fellow researchers and data scientists (technical validation)

Domain experts (e.g., clinicians, biologists, engineers)

Decision-makers (e.g., policy makers, planners, managers)

End users (e.g., patients, drivers, citizens)

Regulators or ethics committees

Examples by domain:

Medical: Clinicians, patients, hospital administrators

Environmental: Scientists, policy makers, public agencies

Transportation: Traffic engineers, city planners, operators

Biology: Researchers, experimental scientists

Example answer:
Clinicians and patients need to understand the explanations in order to trust and act on the model’s predictions.

🔹 Part 7: Constraints and Considerations

**19. Are there ethical considerations?**

[Your answer]

This question asks you to identify any **ethical, social, or legal concerns** related to your Machine Learning problem.
Ethical considerations should be addressed **during problem formulation**, not after the model is built.

Guidelines:
- Consider how data is collected, stored, and used
- Think about who might be harmed or disadvantaged by model errors
- Reflect on fairness, bias, privacy, and consent
- Consider compliance with laws, regulations, or institutional guidelines

Common ethical considerations:
- **Privacy:** Handling sensitive or personal data (e.g., patient, location, biometric data)
- **Fairness:** Unequal performance across demographic or social groups
- **Bias:** Historical or sampling bias reflected in the data
- **Transparency:** Ability to explain decisions to affected individuals
- **Misuse:** Potential for predictions to be used in harmful or unintended ways

Examples by domain:
- Medical: Patient privacy, informed consent, bias across age or gender groups
- Environmental: Fair representation of vulnerable regions or communities
- Transportation: Surveillance concerns, fairness across neighborhoods
- Education: Bias against certain student groups
- Finance: Discrimination in credit or loan decisions

Example answer:
Ethical considerations include patient privacy, secure handling of medical records, and ensuring that the model performs fairly across different demographic groups.


**20. What are your computational constraints?**

Select all options that apply to your project.

[ ] Limited computing resources  
[ ] Need fast predictions (low latency)  
[ ] Need to run on mobile or edge devices  
[ ] No major computational constraints  

[Your answer]

This question helps identify **practical limitations** related to computation, deployment, and runtime performance.
Computational constraints often influence:
- Model choice and complexity
- Training time and cost
- Feasibility of deployment in real-world settings

Guidance:
- **Limited computing resources:**  
  Applies when you have restricted access to GPUs, cloud services, or high-performance computing.
- **Need fast predictions:**  
  Important for real-time or near-real-time systems (e.g., traffic control, medical alerts).
- **Need to run on mobile/edge devices:**  
  Models must be lightweight, memory-efficient, and energy-aware.
- **No major constraints:**  
  Suitable for offline analysis or research-focused experiments.

Examples by domain:
- Medical monitoring: ☑ Need fast predictions  
- Transportation systems: ☑ Need fast predictions, ☑ Edge deployment  
- Academic research: ☑ Limited computing resources  
- Climate modeling: ☑ No major constraints (offline analysis)

Example answer:
Limited computing resources and need fast predictions.

**21. Timeline and resources**

Describe the practical constraints related to time, expertise, and budget for your Machine Learning project.
This information helps determine whether the proposed ML problem is **realistic and achievable**.

---

**Time available:**
[Your answer]
Example: 3 months for data preparation, modeling, and evaluation.

### Section 7: Common Pitfalls and How to Avoid Them
pitfall: In Machine Learning research, pitfalls refer to recurring errors in problem formulation, data handling, evaluation, or ethical consideration that may lead to misleading results, inefficient models, or invalid conclusions.

**Pitfall 1: Problem Too Vague**
❌ "I want to use AI for cancer research"
✅ "I want to classify tumor images as benign or malignant with >90% accuracy"
Explanation:
A vague problem statement does not clearly define what is being predicted, what data will be used, or how success will be measured. As a result, it is impossible to choose the right ML approach, dataset, or evaluation metric.

In contrast, a well-defined problem:

Specifies a clear prediction task (classification of tumor images)

Identifies the output variable (benign vs. malignant)

Defines a measurable success criterion (>90% accuracy)
**Pitfall 2: Insufficient Data Consideration**
❌ Starting model development before checking data availability
✅ Assess data first, then adjust problem scope if needed
Explanation:
Many ML projects fail because models are designed without verifying whether suitable data actually exists. Starting with model selection or training before understanding data quantity, quality, and relevance often leads to unrealistic expectations and wasted effort.

A proper approach requires assessing:

How much data is available

Whether the data is relevant to the prediction target

Data quality issues such as missing values or noisy labels

Class balance and representativeness

If data is limited or incomplete, the problem scope should be adjusted—for example, simplifying the task, reducing the prediction horizon, or choosing a different ML approach.

**Pitfall 3: Unrealistic Expectations**
❌ "My model must be 100% accurate"
✅ "My model should outperform current clinical guidelines by 10%"
Explanation:
Unrealistic performance expectations are a common mistake in Machine Learning research. Real-world data is noisy, incomplete, and uncertain, which makes perfect accuracy scientifically unrealistic in most domains.

Expecting 100% accuracy ignores:

Measurement errors in data

Ambiguity in labels

Inherent uncertainty in real-world processes

A realistic goal is to compare the ML model against a meaningful baseline, such as existing expert rules, clinical guidelines, or simple statistical models. Improvement over these baselines represents real progress.
**Pitfall 4: Ignoring Explainability from the Start**
❌ "I'll worry about explaining the model after it works"
✅ "I'll choose interpretable models and plan XAI techniques early"
Explanation:
Explainability is not an optional add-on—it is a core requirement in many Machine Learning applications, especially in research and high-impact domains such as healthcare, environmental policy, biology, and transportation. Treating explainability as an afterthought often leads to models that are accurate but unusable or untrustworthy.

Once a highly complex or opaque model is trained, it can be difficult or even impossible to extract meaningful explanations. Planning explainability early allows researchers to:

Select models that balance accuracy and interpretability

Design experiments that support explanation needs

Ensure alignment with ethical, legal, and domain requirements
**Pitfall 5: Wrong Problem Type**
❌ Treating a regression problem as classification or vice versa
✅ Carefully identify whether you're predicting categories or continuous values
Explanation:
Choosing the wrong ML problem type is a serious mistake because it leads to incorrect modeling decisions, wrong evaluation metrics, and misleading results.

The key difference is the form of the output:

Classification predicts discrete categories/labels
(e.g., disease: yes/no, spam/not spam, risk: high/low)

Regression predicts a continuous numerical value
(e.g., temperature, price, travel time, health score)

If you treat a regression problem as classification, you often lose important information by forcing numeric outcomes into arbitrary categories. If you treat a classification problem as regression, predictions become difficult to interpret and evaluate properly.
**Pitfall 6: Overlooking Ethical Issues**
❌ Not considering bias, fairness, or privacy until publication
✅ Address ethical considerations in problem formulation phase
Explanation:
Ethical issues in Machine Learning are often deeply embedded in the problem definition and data, not just in the model itself. Delaying ethical considerations until the end of a project can result in biased, unfair, or even harmful outcomes that are difficult to fix later.

Ethical concerns may include:

Bias and fairness: Unequal performance across demographic or social groups

Privacy: Handling sensitive or personal data responsibly

Transparency: Ability to explain decisions to affected individuals

Potential misuse: Predictions being applied in harmful or unintended ways

By addressing ethics during problem formulation, researchers can:

Choose appropriate data sources

Define fair evaluation metrics

Plan explainability requirements

Reduce risks of harm and misuse
---

## 💡 Key Takeaways

> **Remember These Points:**
> - 🔑 Not every research question needs ML—make sure yours benefits from it
> - 🔑 Transform vague questions into specific, measurable ML problems
> - 🔑 Identify your problem type (classification, regression, clustering, etc.)
> - 🔑 Define clear success metrics before starting
> - 🔑 Assess your data availability and quality early
> - 🔑 Plan for explainability from the beginning, not as an afterthought

## 🔬 Hands-On Exercise

### Exercise 1: Problem Formulation Practice

**Objective:** Transform a vague research question into a well-defined ML problem.

**Scenario:**
Dr. Sarah is a marine biologist studying coral reefs. She's noticed that some reefs are more resilient to temperature changes than others. She has 5 years of data including water temperature, coral species composition, reef location, depth, and human activity levels. Every month, she's assessed each reef's health on a scale of 0-100.

**Your Task:**

1. **Define the specific ML goal:**
   - What should the model predict?
   - For whom or what?

2. **Identify the problem type:**
   - Is this classification, regression, clustering, or anomaly detection?
   - Why?

3. **List the input features:**
   - What data will the model use to make predictions?

4. **Define the output:**
   - What exactly is being predicted?

5. **Choose success metrics:**
   - How will you measure if the model works well?

6. **Explain why XAI matters here:**
   - What would you want to understand about the model's decisions?

**Example Solution:**
<details>
<summary>Click to reveal solution</summary>

1. **Specific ML Goal:**
   Predict coral reef health score (0-100) for the next month based on environmental and human activity factors.

2. **Problem Type:**
   Regression - predicting a continuous numerical value (health score)

3. **Input Features:**
   - Water temperature (current and past 3 months)
   - Coral species diversity (number of species)
   - Reef location (latitude, longitude)
   - Depth
   - Human activity level (tourism, fishing pressure)
   - Previous health scores (time series)

4. **Output:**
   Predicted health score (0-100) for next month

5. **Success Metrics:**
   - Primary: Mean Absolute Error < 5 points
   - Secondary: R² score > 0.75
   - Baseline: Compare against "predict same as last month"

6. **XAI Importance:**
   Need to understand which factors most affect reef health to guide conservation efforts. Want to identify if temperature, human activity, or species diversity is the main driver, which can inform policy decisions and interventions.
</details>

---

### Exercise 2: Your Own Research Problem

**Objective:** Formulate your own research question as an ML problem.

**Your Task:**
Complete the Problem Formulation Worksheet (Section 6) for your own research question or area of interest.

**Steps:**
1. Think of a research question from your field
2. Work through all 20 questions in the worksheet
3. Share your formulation in [GitHub Discussions](../../discussions) for feedback

**No research question yet?**
Choose one of these example scenarios and complete the worksheet:

- **Education Research:** Predicting student performance to identify those who need extra support
- **Agricultural Research:** Forecasting crop disease outbreaks based on weather patterns
- **Social Science:** Understanding factors that predict community health outcomes
- **Engineering:** Predicting equipment failure to schedule preventive maintenance

## 📖 Glossary

**Classification**: Predicting which category something belongs to

**Regression**: Predicting a continuous numerical value

**Clustering**: Finding natural groups in data without predefined categories

**Supervised Learning**: Learning from labeled data (you have examples with correct answers)

**Unsupervised Learning**: Finding patterns in unlabeled data

**Features**: The input variables or measurements used for prediction

**Labels**: The correct answers or outputs in supervised learning

**Metric**: A quantitative measure of model performance

**Baseline**: A simple method to compare your model against

## 🔗 Resources and Further Reading

### Essential Reading
- 📄 [How to Define a Machine Learning Problem](https://machinelearningmastery.com/how-to-define-your-machine-learning-problem/) - Practical guide
- 📄 [Choosing the Right ML Approach](https://developers.google.com/machine-learning/problem-framing) - Google's framework

### Video Tutorials
- 🎥 [Problem Framing in ML](https://www.youtube.com/watch?v=Jn8c3oe_GWU) - [15 min] - Google's approach
- 🎥 [Classification vs Regression](https://www.youtube.com/watch?v=i_LwzRVP7bg) - [12 min] - Understanding problem types

### Research Papers
- 📑 "A Few Useful Things to Know About Machine Learning" by Pedro Domingos - Classic paper on ML fundamentals
- 📑 "Developing and Validating Clinical Prediction Models" - Guidelines for medical ML research

### Tools
- 🛠️ [Problem Formulation Template](../../resources/templates/problem-formulation-template.md) - Downloadable worksheet

## ❓ Self-Check Questions

Test your understanding:

1. **What are the four main types of ML problems covered in this module?**
   <details>
   <summary>Show Answer</summary>
   Classification (predicting categories), Regression (predicting numbers), Clustering (finding groups), and Anomaly Detection (identifying unusual cases).
   </details>

2. **Why is it important to define success metrics before building your model?**
   <details>
   <summary>Show Answer</summary>
   Success metrics help you: (1) know when your model is good enough, (2) compare different approaches objectively, (3) set clear research goals, and (4) report results in publications. Without them, you can't evaluate whether your ML approach is working.
   </details>

3. **How would you distinguish between a classification and regression problem?**
   <details>
   <summary>Show Answer</summary>
   Classification predicts discrete categories (e.g., spam/not spam, disease type). Regression predicts continuous numerical values (e.g., temperature, price, time). Ask: "Am I predicting a category or a number?"
   </details>

4. **What should you do if you realize you don't have enough data for your ML problem?**
   <details>
   <summary>Show Answer</summary>
   Options include: (1) collect more data, (2) simplify the problem, (3) use techniques for small datasets (transfer learning, data augmentation), (4) collaborate to pool data, or (5) reconsider whether ML is the right approach.
   </details>

## 💬 Discussion Questions

Engage with these questions in [GitHub Discussions](../../discussions):

1. In your research field, what makes a good ML problem formulation particularly challenging?

2. How do you balance the need for model accuracy with the need for explainability in research?

3. What ethical considerations are most important when formulating ML problems in your domain?

## ➡️ What's Next?

**You've completed Module 02!** 🎉

You now know how to transform research questions into well-defined ML problems.

**Next Module:** [Module 03 - Data Selection and Acquisition](../03-data-selection-and-acquisition/)

In the next module, you'll learn how to:
- Find and select appropriate datasets
- Collect data effectively
- Assess data quality
- Handle ethical considerations in data collection

**Before moving on:**
- [ ] Review the key takeaways
- [ ] Complete the problem formulation worksheet for your research
- [ ] Try at least one hands-on exercise
- [ ] Share your problem formulation in Discussions for feedback

**Alternative Paths:**
- Want to review basics? Go back to [Module 01](../01-introduction/)
- Want to see data in action? Preview [Module 03](../03-data-selection-and-acquisition/)

---

## 📞 Need Help?

- **Questions about formulating your problem?** Open a [Discussion](https://github.com/mahbubchula/XAI_TR/discussions)
- **Unsure about problem type?** Ask in Discussions with your research question
- **Found an error?** Open an [Issue](https://github.com/mahbubchula/XAI_TR/issues)

**Module Contributors:** Mahbub Chula  
**Last Updated:** January 2026

---

**Great progress!** 🚀 You're building a solid foundation. See you in Module 03!
