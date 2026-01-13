# XAI Interpretation Guide Template

Use this guide to structure your explanation and interpretation of ML model predictions using Explainable AI techniques.

**Project Name:** [Your project]  
**Model:** [Model name/type]  
**Date:** [Date]  
**Analyst:** [Your name]

---

## 1. Overview

### Purpose
[What are you trying to explain? For whom?]

### Model Summary
- **Type:** [e.g., Random Forest, Neural Network]
- **Task:** [Classification / Regression / Other]
- **Performance:** [Key metric: value]
- **Dataset:** [Brief description]

### Audience
[Who will read these explanations? Adjust technical level accordingly]

---

## 2. Global Model Behavior

### 2.1 Overall Feature Importance

**Question:** Which features matter most to the model overall?

**Method Used:** [e.g., Built-in feature importance, Permutation importance]

**Results:**

| Rank | Feature | Importance Score | Interpretation |
|------|---------|------------------|----------------|
| 1 | [Feature name] | [Value] | [What this means] |
| 2 | | | |
| 3 | | | |
| ... | | | |

**Visualization:** [Include or describe feature importance plot]

**Key Insights:**
- [Insight 1]
- [Insight 2]
- [Insight 3]

### 2.2 Feature Relationships

**How do features interact?**

**Partial Dependence Plots:**
[Describe how individual features affect predictions]

For [Feature X]:
- When [Feature X] is low: [Effect on prediction]
- When [Feature X] is high: [Effect on prediction]
- Relationship: [Linear / Non-linear / Threshold effect]

**Interaction Effects:**
[Do any features work together?]

Example: [Feature A] and [Feature B]
- [Description of interaction]

### 2.3 Decision Rules (if applicable)

**What rules did the model learn?**

[For interpretable models like decision trees]

Example rules:
1. IF [condition] THEN [prediction]
2. IF [condition] AND [condition] THEN [prediction]

---

## 3. Local Explanations

### 3.1 Individual Prediction Explanations

Select 5-10 representative or interesting cases to explain in detail.

---

#### Case 1: [Brief description]

**Instance Details:**
| Feature | Value | Population Average |
|---------|-------|-------------------|
| [Feature 1] | [Value] | [Avg] |
| [Feature 2] | [Value] | [Avg] |
| ... | | |

**Prediction:**
- **Model output:** [Value]
- **Actual value:** [If known]
- **Confidence:** [If available]

**Explanation Method:** [SHAP / LIME / Other]

**Feature Contributions:**

| Feature | Contribution | Direction | Explanation |
|---------|--------------|-----------|-------------|
| [Feature 1] | +2.3 | Increases | [Why this pushes toward prediction] |
| [Feature 2] | -1.1 | Decreases | [Why this pushes away] |
| [Feature 3] | +0.8 | Increases | [Explanation] |

**Visualization:** [SHAP force plot, LIME explanation, etc.]

**Plain Language Explanation:**
[Explain this prediction as you would to a non-technical stakeholder]

*"The model predicted [outcome] primarily because [main reason]. Contributing factors include [factor 1] and [factor 2]. [Feature X] had a moderate opposing effect."*

**Verification:**
- Does this explanation make domain sense? [Yes/No]
- Does it align with expert knowledge? [Yes/No]
- Are there any surprising factors? [Describe]

---

#### Case 2: [Different scenario]

[Same structure as Case 1]

---

#### Case 3: [Edge case or error]

[Same structure, but focus on why model might be wrong]

---

### 3.2 Counterfactual Explanations

**Question:** What would need to change for a different prediction?

**Example:**

**Current:** Patient predicted HIGH risk
**Features:** Age=55, BP=140, BMI=32

**Counterfactual:** For LOW risk prediction, need:
- BP < 130 (reduce by 10+)
- BMI < 28 (reduce by 4+)

**Actionability:** [Are these changes realistic/possible?]

---

## 4. Model Trust and Reliability

### 4.1 Confidence Analysis

**How confident is the model in its predictions?**

**High Confidence Predictions:**
- Characteristics: [What makes model confident?]
- Accuracy in high-confidence cases: [%]

**Low Confidence Predictions:**
- Characteristics: [What makes model uncertain?]
- How to handle: [Recommendation]

### 4.2 Model Limitations Revealed by XAI

**What did explanations reveal about limitations?**

| Limitation | Evidence | Impact | Mitigation |
|------------|----------|--------|------------|
| [e.g., Spurious correlation] | [XAI finding] | [Concern level] | [How to address] |

### 4.3 Biases Detected

**Did explanations reveal any biases?**

- [ ] **Protected attributes inappropriately used**
  - Details: [Description]
  - Action: [What was done]

- [ ] **Proxy variables for sensitive attributes**
  - Details: [Description]
  - Action: [What was done]

- [ ] **Unexpected feature dependencies**
  - Details: [Description]
  - Action: [What was done]

---

## 5. Domain Expert Validation

### 5.1 Expert Review
[Have domain experts reviewed the explanations?]

**Reviewer:** [Name, credentials]  
**Date:** [Date]

**Findings:**
- ✅ **Aligned with domain knowledge:** [List aspects]
- ⚠️ **Questionable patterns:** [List concerns]
- ❌ **Contradicts domain knowledge:** [List issues]

### 5.2 Expert Feedback Integration
[How did you address expert concerns?]

---

## 6. XAI Method Details

### Methods Used

#### Method 1: [e.g., SHAP]
- **Type:** [Global / Local / Both]
- **Pros:** [Benefits for your use case]
- **Cons:** [Limitations for your use case]
- **Computational cost:** [Time/resources needed]

#### Method 2: [e.g., LIME]
- **Type:** [Global / Local / Both]
- **Pros:** [Benefits]
- **Cons:** [Limitations]
- **Computational cost:** [Time/resources needed]

### Method Comparison
[Did different methods give consistent results?]

| Case | SHAP Top Feature | LIME Top Feature | Agreement? |
|------|------------------|------------------|------------|
| 1 | | | |
| 2 | | | |

**Consistency:** [High / Medium / Low]
**Interpretation:** [What does this tell us?]

---

## 7. Actionable Insights

### 7.1 For Model Improvement
Based on XAI analysis, recommend:
1. [Recommendation 1]
2. [Recommendation 2]

### 7.2 For End Users
[What should users know about how the model works?]

**Key Messages:**
- [Message 1]
- [Message 2]

**Usage Guidelines:**
- When to trust the model: [Conditions]
- When to be cautious: [Conditions]
- When to override: [Conditions]

### 7.3 For Domain Understanding
[What new scientific/domain insights emerged?]

**Novel Findings:**
1. [Finding 1]
2. [Finding 2]

**Confirmed Knowledge:**
- [What known relationships were confirmed?]

**Challenged Assumptions:**
- [What assumptions were questioned?]

---

## 8. Communication Strategy

### 8.1 For Different Audiences

**For Researchers/Peers:**
[Technical explanation with full details]

**For Practitioners/Clinicians:**
[Practical interpretation focused on application]

**For Patients/Public:**
[Simple, non-technical explanation]

**For Regulators:**
[Transparency and compliance focus]

### 8.2 Visualization Strategy
[What visualizations best convey explanations?]

- Feature importance bar charts
- SHAP summary plots
- Individual force plots
- Partial dependence plots
- [Other visualizations]

---

## 9. Documentation for Publication

### 9.1 Methods Section Content
[Draft text for methodology describing XAI approach]

### 9.2 Results Section Content
[Draft text presenting XAI findings]

### 9.3 Supplementary Materials
[What to include as supplementary information]

- Full feature importance rankings
- Additional case explanations
- XAI method validation
- Code and notebooks

---

## 10. Checklist

### Explanation Completeness
- [ ] Global model behavior explained
- [ ] Representative individual cases explained
- [ ] Both positive and negative predictions covered
- [ ] Edge cases and errors analyzed
- [ ] Counterfactuals provided where relevant
- [ ] Explanations validated by domain experts
- [ ] Biases and limitations identified
- [ ] Explanations appropriate for intended audience

### Quality Checks
- [ ] Explanations are consistent across methods
- [ ] Findings align with domain knowledge
- [ ] Unexpected patterns investigated
- [ ] Explanations are actionable
- [ ] Technical and plain language versions created
- [ ] Visualizations clear and informative

---

## 11. Appendices

### Appendix A: XAI Method Parameters
[Detailed parameters for reproducibility]

```python
# Example SHAP configuration
shap.TreeExplainer(
    model=model,
    data=background_data,
    ...
)
```

### Appendix B: Additional Visualizations
[Extra plots and figures]

### Appendix C: Code
[Link to analysis code/notebooks]

---

## 12. Lessons Learned

### What Worked Well
[Successful aspects of XAI approach]

### Challenges Encountered
[Difficulties and how they were addressed]

### Recommendations for Future
[Advice for next XAI analysis]

---

## Document Information

**Guide Version:** 1.0  
**Created:** [Date]  
**Last Updated:** [Date]  
**Reviewed by:** [Name(s)]

---

## 📞 Contact

**Author:** [Name, Email]  
**Domain Expert:** [Name, Email]  
**Questions:** [Contact information]

---

**Template by XAI_TR Course**
