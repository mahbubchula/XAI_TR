# Problem Formulation Template

Use this template to structure your Machine Learning research problem.

**Date:** [Today's date]  
**Your Name:** [Your name]  
**Research Field:** [Your field]

---

## 1. Research Context

### 1.1 Research Field
[Describe your field in 1-2 sentences]

### 1.2 Broad Research Interest
[What general area are you investigating?]

### 1.3 Specific Research Question
[What specific question do you want to answer?]

---

## 2. ML Problem Definition

### 2.1 Prediction/Discovery Goal
[What exactly do you want to predict or discover?]

### 2.2 ML Problem Type
Select one:
- [ ] **Classification** - Predicting categories
  - [ ] Binary (2 classes)
  - [ ] Multi-class (3+ classes)
  - [ ] Multi-label (multiple categories per instance)
- [ ] **Regression** - Predicting continuous numbers
- [ ] **Clustering** - Finding natural groups
- [ ] **Anomaly Detection** - Finding unusual cases
- [ ] **Other:** [Specify]

### 2.3 Learning Type
- [ ] **Supervised** (I have labeled data)
- [ ] **Unsupervised** (I don't have labels)
- [ ] **Semi-supervised** (I have some labels)

---

## 3. Input and Output Specification

### 3.1 Input Features
List all the data/features you will use for prediction:

| Feature Name | Type | Description | Example Value |
|--------------|------|-------------|---------------|
| [e.g., Age] | [Numeric] | [Patient age in years] | [45] |
| | | | |
| | | | |

### 3.2 Output/Target
**What are you predicting?**
- Variable name: [e.g., Disease Risk]
- Type: [Category / Number]
- Possible values: [e.g., High/Low or 0-100]

---

## 4. Data Assessment

### 4.1 Current Data
- **Data source:** [Where is your data from?]
- **Amount of data:** [How many samples/records?]
- **Time period:** [When was data collected?]
- **Data format:** [CSV, images, text, etc.]

### 4.2 Data Quality

**Completeness:**
- Missing data: [%]
- Which features have missing data? [List]

**Label Quality (for supervised learning):**
- Who labeled the data? [Expert / Automated / Crowdsourced]
- Label reliability: [High / Medium / Low]
- Inter-rater agreement: [If applicable]

**Class Balance (for classification):**
- Samples per class:
  - Class 1: [Number]
  - Class 2: [Number]
  - [Continue for all classes]
- Is the data imbalanced? [Yes / No]

**Representativeness:**
- Does data cover all important scenarios? [Yes / No / Partially]
- What's missing? [Describe]

### 4.3 Additional Data Needs
- [ ] I need more data
  - How will you get it? [Describe]
  - Timeline: [Estimate]
- [ ] Current data is sufficient

---

## 5. Success Criteria

### 5.1 Evaluation Metrics

**Primary Metric:**
[e.g., Accuracy, F1-Score, Mean Absolute Error]

**Why this metric?**
[Explain why this is the right metric for your problem]

**Secondary Metrics:**
- [Metric 2]
- [Metric 3]

### 5.2 Target Performance
[What performance level would make the model useful?]

**Minimum acceptable:** [e.g., 80% accuracy]  
**Target goal:** [e.g., 90% accuracy]  
**Aspirational:** [e.g., 95% accuracy]

### 5.3 Baseline Comparison
What will you compare your model against?
- [ ] Random guessing
- [ ] Simple rule-based approach
- [ ] Current clinical/expert guidelines
- [ ] Existing published models
- [ ] Other: [Specify]

**Baseline performance (if known):** [Number/description]

---

## 6. Explainability Requirements

### 6.1 Why Explainability Matters
[Explain why understanding the model's reasoning is important for your research]

### 6.2 What to Explain
[What aspects of the model's decisions need explanation?]

Examples:
- Which features are most important overall?
- Why did it make this specific prediction?
- How confident is the model?
- What patterns did it learn?

### 6.3 Audience for Explanations
Who needs to understand the model?
- [ ] Fellow researchers
- [ ] Domain experts (doctors, scientists, etc.)
- [ ] Policy makers
- [ ] End users/patients
- [ ] Reviewers for publication
- [ ] Other: [Specify]

### 6.4 XAI Techniques to Consider
- [ ] Feature importance
- [ ] SHAP (SHapley Additive exPlanations)
- [ ] LIME (Local Interpretable Model-agnostic Explanations)
- [ ] Attention mechanisms
- [ ] Decision rules
- [ ] Other: [Specify]

---

## 7. Constraints and Considerations

### 7.1 Ethical Considerations
- **Privacy concerns:** [Describe]
- **Fairness across groups:** [Important groups to consider]
- **Potential biases:** [Possible bias sources]
- **Dual use concerns:** [Could this be misused?]

**Mitigation strategies:**
[How will you address these concerns?]

### 7.2 Computational Constraints
- [ ] Limited computing resources
- [ ] Need real-time/fast predictions
- [ ] Need to run on mobile/edge devices
- [ ] Must work offline
- [ ] No major constraints

**Details:** [Describe limitations]

### 7.3 Regulatory/Publication Requirements
- [ ] Must comply with regulations (GDPR, HIPAA, etc.)
- [ ] Must meet journal requirements
- [ ] Need institutional review board (IRB) approval
- [ ] Other: [Specify]

---

## 8. Timeline and Resources

### 8.1 Project Timeline
- **Start date:** [Date]
- **Target completion:** [Date]
- **Key milestones:**
  - Data collection: [Date]
  - Model development: [Date]
  - Evaluation: [Date]
  - Publication: [Date]

### 8.2 Available Resources
- **Team members:** [List roles and expertise]
- **Computing resources:** [Describe]
- **Budget:** [If applicable]
- **External support:** [Collaborators, consultants]

### 8.3 Skills Gap
What skills do you need to develop or acquire help for?
- [ ] Programming (Python)
- [ ] ML algorithms
- [ ] Data preprocessing
- [ ] Statistical analysis
- [ ] XAI techniques
- [ ] Other: [Specify]

---

## 9. Risk Assessment

### 9.1 Potential Challenges
| Challenge | Impact (Low/Med/High) | Mitigation Strategy |
|-----------|----------------------|---------------------|
| [e.g., Insufficient data] | [High] | [Collect more data or simplify problem] |
| | | |

### 9.2 Alternative Approaches
If ML doesn't work, what are your backup options?
1. [Alternative 1]
2. [Alternative 2]

---

## 10. Expected Outcomes and Impact

### 10.1 Research Contribution
How will this work advance your field?
[Describe expected contribution]

### 10.2 Practical Applications
How will the results be used?
[Describe real-world applications]

### 10.3 Publications and Dissemination
Where will you publish/present?
- Target journals: [List]
- Conferences: [List]
- Other outlets: [List]

---

## 11. Summary

### One-Sentence Problem Statement
[Concisely describe your ML problem in one sentence]

### Key Requirements Checklist
- [ ] Problem clearly defined
- [ ] Data availability confirmed
- [ ] Success metrics identified
- [ ] Explainability needs specified
- [ ] Ethical considerations addressed
- [ ] Resources and timeline planned

---

## 12. Next Steps

Immediate actions:
1. [Action 1]
2. [Action 2]
3. [Action 3]

---

**Notes and Additional Thoughts:**
[Any other relevant information]

---

**Version:** 1.0  
**Last Updated:** [Date]  
**Review Date:** [When will you review/update this?]
