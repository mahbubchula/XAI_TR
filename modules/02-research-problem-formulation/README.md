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
 - **Have a **general research area, problem domain, or preliminary research question** in mind  
  *(a fully defined research problem is not required)*

## 🎯 Learning Objectives

By the end of this module, you will be able to:
1. Determine whether your research question is suitable for Machine Learning
2. Transform vague research ideas into well-defined ML problems
3. Define measurable success metrics for your ML project
4. Identify your data requirements and constraints
5. Create a structured problem formulation document

## 📚 Module Content

### Section 1: When Should You Use Machine Learning?

Not every research problem needs ML. Understanding when ML is appropriate will save you time and lead to better research.

**ML is a Good Fit When:**

✅ **You have patterns in data to learn from**
- Example: Predicting disease from patient symptoms and test results
- Why it works: Historical data shows patterns between symptoms and diagnoses

✅ **The problem is too complex for simple rules**
- Example: Identifying spam emails (too many variations for simple rules)
- Why it works: ML can learn complex combinations of features

✅ **You have sufficient data**
- Example: Classifying plant species from images (with hundreds of labeled images)
- Why it works: ML needs examples to learn from

✅ **The problem involves prediction or classification**
- Example: Forecasting crop yields based on weather and soil data
- Why it works: ML excels at finding predictive relationships

✅ **Manual analysis would be too time-consuming**
- Example: Analyzing thousands of research papers to identify trends
- Why it works: ML can process large volumes efficiently

**ML Might NOT Be the Best Fit When:**

❌ **You have very little data**
- If you only have 20-30 examples, traditional statistical methods may work better

❌ **Simple rules work well**
- If "IF temperature > 100°C THEN water boils" solves your problem, you don't need ML

❌ **You need 100% explainability from the start**
- Some highly regulated fields require complete transparency that complex ML can't provide

❌ **The cost of errors is extremely high**
- Life-critical systems may need more traditional, provably safe approaches

❌ **You don't have the right data**
- If your available data doesn't relate to what you want to predict, ML can't help

---

### Section 2: Types of ML Problems

Understanding what type of ML problem you have helps you choose the right approach.

#### 2.1 Classification Problems

**What it is:** Assigning items to predefined categories

**Question format:** "What category does this belong to?"

**Examples:**
- Is this email spam or not spam? (Binary Classification - 2 categories)
- What species is this plant? (Multi-class Classification - many categories)
- Which genres does this movie belong to? (Multi-label - multiple categories)

**Research Applications:**
- Diagnosing diseases (healthy, disease A, disease B)
- Classifying cell types from microscopy images
- Categorizing research papers by topic

#### 2.2 Regression Problems

**What it is:** Predicting a continuous numerical value

**Question format:** "How much?" or "How many?"

**Examples:**
- What will the temperature be tomorrow? (Predicting a number)
- How long will this patient stay in the hospital? (Predicting duration)
- What will be the crop yield this season? (Predicting quantity)

**Research Applications:**
- Predicting patient recovery time
- Estimating protein binding affinity
- Forecasting energy consumption

#### 2.3 Clustering Problems

**What it is:** Grouping similar items together without predefined categories

**Question format:** "What natural groups exist in this data?"

**Examples:**
- Grouping customers by purchasing behavior
- Identifying distinct patient populations
- Discovering different types of galaxy formations

**Research Applications:**
- Finding patient subgroups with similar responses to treatment
- Identifying ecosystem types from environmental data
- Discovering patterns in gene expression data

#### 2.4 Anomaly Detection

**What it is:** Identifying unusual or outlier instances

**Question format:** "Is this normal or unusual?"

**Examples:**
- Detecting fraudulent transactions
- Identifying equipment failures
- Finding unusual patterns in sensor data

**Research Applications:**
- Detecting rare disease cases
- Identifying unusual geological formations
- Finding experimental anomalies

---

### Section 3: From Research Question to ML Problem

Let's walk through transforming vague research questions into well-defined ML problems.

**The Framework:**

```
Research Question
      ↓
What are you trying to predict/understand?
      ↓
What type of ML problem is this?
      ↓
What data do you need?
      ↓
How will you measure success?
      ↓
Well-Defined ML Problem
```

**Example 1: Biology Research**

❓ **Vague Research Question:**
"I want to study protein functions"

✅ **Well-Defined ML Problem:**
- **Specific Goal:** Predict protein function categories from amino acid sequences
- **ML Problem Type:** Multi-class classification
- **Input Data:** Protein sequences (amino acid strings)
- **Output:** Function category (enzyme, structural protein, transporter, etc.)
- **Success Metric:** Accuracy of at least 80% on held-out test proteins
- **Why XAI Matters:** Identify which sequence patterns indicate specific functions

---

**Example 2: Environmental Science**

❓ **Vague Research Question:**
"I want to predict climate change impacts"

✅ **Well-Defined ML Problem:**
- **Specific Goal:** Predict regional temperature increases over the next decade
- **ML Problem Type:** Regression (time series)
- **Input Data:** Historical climate data, greenhouse gas measurements, ocean temperatures
- **Output:** Temperature change (°C) for specific regions and years
- **Success Metric:** Mean absolute error < 0.5°C compared to benchmark models
- **Why XAI Matters:** Understand which factors contribute most to temperature changes

---

**Example 3: Medical Research**

❓ **Vague Research Question:**
"Can we detect diseases earlier?"

✅ **Well-Defined ML Problem:**
- **Specific Goal:** Identify patients at high risk for Type 2 diabetes in the next 5 years
- **ML Problem Type:** Binary classification
- **Input Data:** Patient demographics, lab results, medical history, lifestyle factors
- **Output:** Risk prediction (high risk / low risk)
- **Success Metric:** Recall of 85% (catch 85% of future cases) with precision > 60%
- **Why XAI Matters:** Explain to doctors and patients which factors indicate risk

---

### Section 4: Defining Success Metrics

**Why This Matters:**
Success metrics tell you:
- When your model is "good enough"
- How to compare different approaches
- What to report in your research paper

**Common Metrics:**

#### For Classification:

**Accuracy:** Percentage of correct predictions
- Use when: Classes are balanced, all errors are equally important
- Example: 90% accuracy means 9 out of 10 predictions are correct

**Precision:** Of the items predicted as positive, how many were actually positive?
- Use when: False positives are costly
- Example: Of patients predicted to have disease, what % actually have it?

**Recall (Sensitivity):** Of the actual positive items, how many did we find?
- Use when: Missing positives is costly
- Example: Of patients who have disease, what % did we identify?

**F1-Score:** Balance between precision and recall
- Use when: You need both precision and recall to be good

#### For Regression:

**Mean Absolute Error (MAE):** Average difference between predictions and actual values
- Use when: You want easy-to-understand error in original units
- Example: Temperature predictions are off by 2.5°C on average

**Root Mean Square Error (RMSE):** Penalizes large errors more
- Use when: Large errors are particularly bad

**R² Score:** How much of the variance is explained (0-1, higher is better)
- Use when: You want to know if your model is better than a simple baseline

#### Choosing the Right Metric:

Ask yourself:
1. **What type of error is worse?**
   - Missing a disease case? Use Recall
   - False alarm that wastes resources? Use Precision
   
2. **How do I want to report results?**
   - In original units? Use MAE
   - As percentage of variance explained? Use R²

3. **What do reviewers expect in my field?**
   - Check published papers in your field for standard metrics

---

### Section 5: Understanding Your Data Needs

**Data Quantity:**

| ML Task | Typical Minimum | Good Amount | Excellent |
|---------|----------------|-------------|-----------|
| Simple Classification | 100-200 per class | 1,000 per class | 10,000+ per class |
| Complex Classification | 500-1,000 per class | 5,000 per class | 50,000+ per class |
| Simple Regression | 200-500 examples | 2,000 examples | 10,000+ examples |
| Complex Regression | 1,000-2,000 examples | 10,000 examples | 100,000+ examples |

*Note: These are rough guidelines. Quality > Quantity!*

**Data Quality Checklist:**

✅ **Relevance:** Does the data relate to what you want to predict?

✅ **Completeness:** How much missing data do you have?
- < 5% missing: Usually fine
- 5-20% missing: Manageable with techniques
- \> 20% missing: May need more data collection

✅ **Labels (for supervised learning):** Are your labels accurate?
- Who labeled the data?
- How reliable are the labels?
- Is there disagreement between labelers?

✅ **Representativeness:** Does the data cover all scenarios?
- All seasons, conditions, populations?
- Rare but important cases?

✅ **Balance (for classification):**
- Do you have similar numbers of each class?
- Very imbalanced? (e.g., 99% one class, 1% other) - Special techniques needed

**Potential Data Sources:**

1. **Your Own Data Collection**
   - Experiments, surveys, observations
   - Most relevant but time-intensive

2. **Public Datasets**
   - Government databases, research repositories
   - Quick start but may not fit perfectly

3. **Collaborations**
   - Partner institutions, multi-site studies
   - Increases data volume and diversity

4. **Historical Records**
   - Existing databases, archived measurements
   - Already available but may have quality issues

---

### Section 6: The Problem Formulation Worksheet

Complete this worksheet to formulate your ML research problem:

#### Part 1: Research Context
```
1. What is your research field?
   [Your answer]

2. What is your broad research interest?
   [Your answer]

3. What specific question do you want to answer?
   [Your answer]
```

#### Part 2: ML Problem Definition
```
4. What exactly do you want to predict or discover?
   [Your answer]

5. What type of ML problem is this?
   [ ] Classification (predicting categories)
   [ ] Regression (predicting numbers)
   [ ] Clustering (finding groups)
   [ ] Anomaly Detection (finding unusual cases)
   [ ] Other: __________

6. Is this supervised (have labels) or unsupervised (no labels)?
   [Your answer]
```

#### Part 3: Input and Output
```
7. What are your input features (what data will you use)?
   Example: Age, weight, blood pressure, genetic markers
   
   [Your answer - list all features]

8. What is your output (what are you predicting)?
   Example: Disease risk (high/low) or Recovery time (days)
   
   [Your answer]
```

#### Part 4: Data Assessment
```
9. How much data do you currently have?
   [Your answer]

10. What is the quality of your data?
    Completeness (% missing): [Your answer]
    Label reliability: [Your answer]
    Balance across classes: [Your answer]

11. Do you need more data? If so, how will you get it?
    [Your answer]
```

#### Part 5: Success Criteria
```
12. What metrics will you use to evaluate success?
    Primary metric: [Your answer]
    Secondary metrics: [Your answer]

13. What performance level would make the model useful?
    Example: "Accuracy above 85%" or "MAE below 3 days"
    
    [Your answer]

14. What would you compare against (baseline)?
    Example: "Current clinical guidelines" or "Expert predictions"
    
    [Your answer]
```

#### Part 6: Explainability Needs
```
15. Why is explainability important for your problem?
    [Your answer]

16. What would you want the model to explain?
    Example: "Which symptoms most indicate disease?" or
             "Which environmental factors affect outcome?"
    
    [Your answer]

17. Who needs to understand the explanations?
    Example: Fellow researchers, clinicians, policy makers, patients
    
    [Your answer]
```

#### Part 7: Constraints and Considerations
```
18. Are there ethical considerations?
    Example: Patient privacy, fairness across groups
    
    [Your answer]

19. What are your computational constraints?
    [ ] Limited computing resources
    [ ] Need fast predictions
    [ ] Need to run on mobile/edge devices
    [ ] No major constraints

20. Timeline and resources?
    Time available: [Your answer]
    Available expertise: [Your answer]
    Budget for tools/compute: [Your answer]
```

---

### Section 7: Common Pitfalls and How to Avoid Them

**Pitfall 1: Problem Too Vague**
❌ "I want to use AI for cancer research"
✅ "I want to classify tumor images as benign or malignant with >90% accuracy"

**Pitfall 2: Insufficient Data Consideration**
❌ Starting model development before checking data availability
✅ Assess data first, then adjust problem scope if needed

**Pitfall 3: Unrealistic Expectations**
❌ "My model must be 100% accurate"
✅ "My model should outperform current clinical guidelines by 10%"

**Pitfall 4: Ignoring Explainability from the Start**
❌ "I'll worry about explaining the model after it works"
✅ "I'll choose interpretable models and plan XAI techniques early"

**Pitfall 5: Wrong Problem Type**
❌ Treating a regression problem as classification or vice versa
✅ Carefully identify whether you're predicting categories or continuous values

**Pitfall 6: Overlooking Ethical Issues**
❌ Not considering bias, fairness, or privacy until publication
✅ Address ethical considerations in problem formulation phase

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
