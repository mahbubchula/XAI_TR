# Module 05: Model Development 🎯

**Status:** ✅ Complete and Ready to Learn!

---

## 📚 What You'll Learn in This Module

Welcome to Model Development! This is where the magic happens - you'll learn how to train AI models that can make predictions and decisions. Don't worry if you're not from a computer science background; we've designed this module with clear explanations, real-world examples, and step-by-step guidance.

---

## 🎨 Module Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    MODEL DEVELOPMENT JOURNEY                 │
├─────────────────────────────────────────────────────────────┤
│                                                               │
│  Step 1: Understanding ML Models 🧠                          │
│  ↓                                                            │
│  Step 2: Choosing the Right Model 🎯                         │
│  ↓                                                            │
│  Step 3: Training Your Model 🏋️                             │
│  ↓                                                            │
│  Step 4: Validating & Testing 📊                             │
│  ↓                                                            │
│  Step 5: Tuning for Better Performance ⚙️                    │
│  ↓                                                            │
│  Step 6: Avoiding Common Pitfalls ⚠️                         │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

---

## 📋 Prerequisites

Before starting this module, make sure you've completed:

- ✅ **Module 01**: Introduction to Machine Learning
- ✅ **Module 02**: Python Basics for ML
- ✅ **Module 03**: Data Collection and Understanding
- ✅ **Module 04**: Data Preprocessing and Feature Engineering

**Estimated Time:** 8-10 hours (self-paced)

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

- 🔍 Understand different types of ML models and when to use them
- 🎯 Select the right algorithm for your specific problem
- 🏗️ Build and train models using scikit-learn
- 📊 Validate models using cross-validation techniques
- ⚙️ Tune hyperparameters to improve model performance
- 🛡️ Recognize and prevent overfitting
- 🚀 Create complete end-to-end training pipelines

---

## 📖 Table of Contents

### [Section 1: Types of Machine Learning Models](#section-1) 🧠
- 1.1 Supervised Learning Models
- 1.2 Unsupervised Learning Models
- 1.3 Real-World Examples

### [Section 2: Choosing the Right Model](#section-2) 🎯
- 2.1 Decision Framework
- 2.2 Model Selection Flowchart
- 2.3 Common Use Cases

### [Section 3: Classification Models](#section-3) 📊
- 3.1 Logistic Regression
- 3.2 Decision Trees
- 3.3 Random Forests
- 3.4 Support Vector Machines (SVM)
- 3.5 K-Nearest Neighbors (KNN)

### [Section 4: Regression Models](#section-4) 📈
- 4.1 Linear Regression
- 4.2 Ridge and Lasso Regression
- 4.3 Decision Tree Regression
- 4.4 Random Forest Regression

### [Section 5: Clustering Models](#section-5) 🎨
- 5.1 K-Means Clustering
- 5.2 Hierarchical Clustering
- 5.3 DBSCAN

### [Section 6: Training and Validation](#section-6) ✅
- 6.1 Train-Test Split
- 6.2 Cross-Validation Explained
- 6.3 K-Fold Cross-Validation
- 6.4 Stratified Sampling

### [Section 7: Model Evaluation Metrics](#section-7) 📏
- 7.1 Classification Metrics
- 7.2 Regression Metrics
- 7.3 Clustering Metrics
- 7.4 Choosing the Right Metric

### [Section 8: Hyperparameter Tuning](#section-8) ⚙️
- 8.1 What are Hyperparameters?
- 8.2 Grid Search
- 8.3 Random Search
- 8.4 Best Practices

### [Section 9: Avoiding Overfitting](#section-9) 🛡️
- 9.1 Understanding Overfitting
- 9.2 Regularization Techniques
- 9.3 Early Stopping
- 9.4 Data Augmentation

### [Section 10: Complete Training Pipeline](#section-10) 🚀
- 10.1 Pipeline Components
- 10.2 Building Your First Pipeline
- 10.3 Saving and Loading Models

---

<a name="section-1"></a>
## 📘 Section 1: Types of Machine Learning Models 🧠

### 1.1 Supervised Learning Models

**What is Supervised Learning?**

Imagine teaching a child to identify fruits. You show them pictures and tell them "this is an apple," "this is a banana." After seeing many examples, they can identify new fruits on their own. That's supervised learning!

**Key Characteristics:**
- 📝 Learns from labeled data (data with answers)
- 🎯 Makes predictions on new data
- 📊 Two main types: Classification and Regression

#### 🔹 Classification Models

**Purpose:** Predict categories or classes

**Real-World Examples:**
- 📧 Email: Spam or Not Spam?
- 🏥 Medical: Disease Present or Absent?
- 🚗 Transportation: Will traffic be Heavy, Medium, or Light?

**Visual Example:**
```
Input: Email text
        ↓
   [ML Model]
        ↓
Output: Spam ❌ or Not Spam ✅
```

#### 🔹 Regression Models

**Purpose:** Predict continuous numbers

**Real-World Examples:**
- 🏠 House Price Prediction ($200,000, $350,000, etc.)
- 🌡️ Temperature Forecasting (25°C, 30°C, etc.)
- 📈 Stock Price Prediction
- 🚕 Trip Duration Prediction (15 min, 45 min, etc.)

**Visual Example:**
```
Input: House features (size, location, bedrooms)
        ↓
   [ML Model]
        ↓
Output: Price = $325,000
```

---

### 1.2 Unsupervised Learning Models

**What is Unsupervised Learning?**

Imagine sorting a box of mixed buttons by color and size without being told how to group them. You naturally find patterns and create groups. That's unsupervised learning!

**Key Characteristics:**
- 🔍 Learns from unlabeled data (no answers given)
- 🎨 Finds hidden patterns
- 📊 Main type: Clustering

#### 🔹 Clustering Models

**Purpose:** Group similar items together

**Real-World Examples:**
- 🛍️ Customer Segmentation (group similar customers)
- 📰 News Article Grouping (similar topics together)
- 🧬 Gene Expression Analysis
- 🚦 Traffic Pattern Discovery

**Visual Example:**
```
Input: Customer shopping behaviors
        ↓
   [ML Model]
        ↓
Output: 
Group 1: Budget Shoppers 💰
Group 2: Premium Buyers 👑
Group 3: Seasonal Buyers 🎄
```

---

### 1.3 Quick Comparison Table

| **Aspect** | **Classification** | **Regression** | **Clustering** |
|------------|-------------------|----------------|----------------|
| **Output Type** | 🏷️ Categories | 🔢 Numbers | 🎨 Groups |
| **Has Labels?** | ✅ Yes | ✅ Yes | ❌ No |
| **Example** | Spam/Not Spam | House Price | Customer Segments |
| **Common Use** | Decision Making | Forecasting | Pattern Discovery |

---

<a name="section-2"></a>
## 🎯 Section 2: Choosing the Right Model

### 2.1 Decision Framework

**The Golden Question:** What problem are you trying to solve?

```
┌─────────────────────────────────────────────┐
│  START: What do you want to predict?        │
└──────────────────┬──────────────────────────┘
                   │
        ┌──────────┴──────────┐
        │                     │
        ▼                     ▼
   Do you have          Do you have
   labeled data?        labeled data?
        │                     │
   ┌────┴────┐           ┌────┴────┐
   │   YES   │           │   NO    │
   └────┬────┘           └────┬────┘
        │                     │
        ▼                     ▼
   What's the          Find patterns/
   output type?        group data
        │                     │
   ┌────┴────┐               │
   │         │               │
   ▼         ▼               ▼
Category   Number       CLUSTERING
   │         │         (K-Means, etc.)
   │         │
   ▼         ▼
CLASSIFICATION  REGRESSION
(Logistic, etc.) (Linear, etc.)
```

---

### 2.2 Model Selection Flowchart

**For Classification Problems:**

```
Your classification problem
         │
         ▼
┌────────────────────┐
│ How many samples?  │
└────────────────────┘
         │
    ┌────┴────┐
    │         │
    ▼         ▼
 < 100K    > 100K
    │         │
    ▼         ▼
Linear    Neural
Model     Network
    │
    ├─→ Logistic Regression (simple, interpretable)
    ├─→ Decision Tree (visual, easy to explain)
    ├─→ Random Forest (accurate, robust)
    └─→ SVM (good for clear boundaries)
```

**For Regression Problems:**

```
Your regression problem
         │
         ▼
┌────────────────────────┐
│ Linear relationship?   │
└────────────────────────┘
         │
    ┌────┴────┐
    │         │
    ▼         ▼
  YES        NO
    │         │
    ▼         ▼
Linear    Non-linear
Regression  Models
    │
    ├─→ Simple Linear Regression
    ├─→ Ridge Regression (prevents overfitting)
    ├─→ Lasso Regression (feature selection)
    │
    └─→ Decision Tree Regression
        Random Forest Regression
```

---

### 2.3 Common Use Cases

| **Problem Type** | **Best Model** | **When to Use** | **Example** |
|------------------|----------------|-----------------|-------------|
| 📧 **Email Classification** | Logistic Regression | Simple, fast, interpretable | Spam detection |
| 🏠 **House Price** | Random Forest | Complex relationships | Real estate pricing |
| 👥 **Customer Groups** | K-Means | Find natural segments | Marketing campaigns |
| 🚗 **Traffic Prediction** | Decision Tree | Easy to explain to stakeholders | Urban planning |
| 📈 **Stock Trends** | LSTM/Neural Net | Sequential data | Financial forecasting |
| 🏥 **Disease Diagnosis** | Random Forest | High accuracy needed | Medical screening |

---

<a name="section-3"></a>
## 📊 Section 3: Classification Models

### 3.1 Logistic Regression 📈

**What is it?**
Despite the name "regression," it's actually used for classification! Think of it as drawing a line (or curve) to separate two groups.

**When to Use:**
- ✅ Binary classification (Yes/No, True/False)
- ✅ Need probability scores (not just predictions)
- ✅ Want interpretable results
- ✅ Linear relationships in data

**Real-World Example: Email Spam Detection**

```python
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

# Sample data: email features
# [word_count, has_links, exclamation_marks, capital_ratio]
X = [
    [50, 1, 0, 0.05],   # Normal email
    [30, 0, 0, 0.10],   # Normal email
    [100, 5, 10, 0.80], # Spam
    [80, 4, 8, 0.70],   # Spam
]

y = [0, 0, 1, 1]  # 0 = Not Spam, 1 = Spam

# Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Create and train model
model = LogisticRegression()
model.fit(X_train, y_train)

# Make predictions
predictions = model.predict(X_test)

# Check accuracy
accuracy = accuracy_score(y_test, predictions)
print(f"Accuracy: {accuracy * 100:.2f}%")

# Get probability scores
probabilities = model.predict_proba(X_test)
print(f"Spam probability: {probabilities[0][1] * 100:.2f}%")
```

**Visual Understanding:**
```
High Spam Probability
        ↑
      1 |           ✗ ✗
        |         ✗
   0.5  |-------/-------  Decision Boundary
        |     /
        |   ✓ ✓
      0 |_________________→
         Low              High
         Spam Features
         
✓ = Not Spam
✗ = Spam
```

**Pros:**
- ⚡ Fast training and prediction
- 📊 Provides probability scores
- 🔍 Easy to interpret
- 💾 Works well with small datasets

**Cons:**
- ⚠️ Assumes linear relationships
- ⚠️ May struggle with complex patterns
- ⚠️ Sensitive to outliers

---

### 3.2 Decision Trees 🌳

**What is it?**
Imagine playing "20 Questions" - you ask yes/no questions to narrow down the answer. A decision tree works the same way!

**When to Use:**
- ✅ Need easy-to-explain model
- ✅ Have mix of numerical and categorical data
- ✅ Non-linear relationships
- ✅ Don't need to scale features

**Real-World Example: Passenger Survival Prediction (Titanic)**

```python
from sklearn.tree import DecisionTreeClassifier
from sklearn import tree
import matplotlib.pyplot as plt

# Sample data: [age, fare, is_male, class]
X_train = [
    [22, 7.25, 1, 3],   # Young male, 3rd class → Died
    [38, 71.28, 0, 1],  # Adult female, 1st class → Survived
    [26, 7.92, 1, 3],   # Adult male, 3rd class → Died
    [35, 53.10, 0, 1],  # Adult female, 1st class → Survived
]

y_train = [0, 1, 0, 1]  # 0 = Died, 1 = Survived

# Create and train model
model = DecisionTreeClassifier(max_depth=3, random_state=42)
model.fit(X_train, y_train)

# Visualize the tree
plt.figure(figsize=(12, 8))
tree.plot_tree(
    model, 
    feature_names=['Age', 'Fare', 'Is_Male', 'Class'],
    class_names=['Died', 'Survived'],
    filled=True,
    rounded=True
)
plt.title("Decision Tree for Titanic Survival", fontsize=16)
plt.show()

# Make prediction
new_passenger = [[30, 50, 0, 2]]  # 30yo female, 2nd class, fare $50
prediction = model.predict(new_passenger)
print(f"Survival prediction: {'Survived' if prediction[0] else 'Died'}")
```

**Visual Understanding:**
```
                    [Root: All Passengers]
                            │
                    Is passenger male?
                    /                \
                 Yes                  No
                  │                    │
            [Died: 80%]          What class?
                                /     |     \
                              1st    2nd    3rd
                               │      │      │
                         [Survived] [Survived] [Died]
                           95%      80%      50%
```

**Pros:**
- 📖 Easy to understand and explain
- 🎯 Handles non-linear relationships
- 🔧 No feature scaling needed
- 📊 Works with mixed data types

**Cons:**
- ⚠️ Can overfit easily
- ⚠️ Unstable (small data changes = big tree changes)
- ⚠️ Biased toward dominant classes

**Tip for Non-CS People:**
> Think of a decision tree like a flowchart you might use to make decisions in everyday life!

---

### 3.3 Random Forests 🌲🌲🌲

**What is it?**
Instead of asking one person for advice, you ask 100 people and take a vote. Random Forest creates many decision trees and combines their predictions!

**When to Use:**
- ✅ Need high accuracy
- ✅ Have large dataset
- ✅ Want to prevent overfitting
- ✅ Need feature importance scores

**Real-World Example: Credit Card Fraud Detection**

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report
import numpy as np

# Sample data: [amount, time_since_last, merchant_category, distance_from_home]
X_train = np.array([
    [50.00, 2, 1, 5],      # Normal
    [25.00, 1, 2, 2],      # Normal
    [5000.00, 0, 5, 500],  # Fraud
    [3000.00, 0, 4, 300],  # Fraud
    [100.00, 3, 1, 10],    # Normal
])

y_train = [0, 0, 1, 1, 0]  # 0 = Normal, 1 = Fraud

# Create Random Forest with 100 trees
model = RandomForestClassifier(
    n_estimators=100,  # Number of trees
    max_depth=5,       # Maximum depth of each tree
    random_state=42
)

# Train the model
model.fit(X_train, y_train)

# Check feature importance
feature_names = ['Amount', 'Time_Since_Last', 'Merchant', 'Distance']
importances = model.feature_importances_

print("\n🎯 Feature Importance:")
for name, importance in zip(feature_names, importances):
    print(f"{name}: {importance:.2%}")

# Make prediction
new_transaction = [[2500, 0, 4, 250]]
prediction = model.predict(new_transaction)
probability = model.predict_proba(new_transaction)[0]

print(f"\n Prediction: {'⚠️ FRAUD' if prediction[0] else '✅ Normal'}")
print(f"Fraud Probability: {probability[1]*100:.1f}%")
```

**Visual Understanding:**
```
Random Forest = Voting System

Tree 1: Fraud (70% sure)
Tree 2: Fraud (85% sure)
Tree 3: Normal (40% sure)
Tree 4: Fraud (90% sure)
Tree 5: Fraud (75% sure)
...
Tree 100: Fraud (80% sure)

Final Vote: 85 trees say FRAUD → Result: FRAUD ⚠️
```

**Pros:**
- 🎯 High accuracy
- 🛡️ Less prone to overfitting
- 📊 Handles large datasets well
- 🔍 Provides feature importance

**Cons:**
- ⏱️ Slower to train
- 💾 Uses more memory
- 🔒 Less interpretable than single tree

---

### 3.4 Support Vector Machines (SVM) 🎯

**What is it?**
Imagine drawing the best possible line (or hyperplane) to separate two groups, maximizing the "safety margin" between them.

**When to Use:**
- ✅ Clear separation between classes
- ✅ High-dimensional data
- ✅ Small to medium datasets
- ✅ Need robust boundaries

**Real-World Example: Image Classification (Cat vs Dog)**

```python
from sklearn.svm import SVC
from sklearn.preprocessing import StandardScaler
import numpy as np

# Sample data: simplified image features
# [ear_pointiness, nose_length, tail_curl, fur_texture]
X_train = np.array([
    [8, 2, 9, 5],    # Cat
    [9, 1, 8, 6],    # Cat
    [2, 8, 2, 8],    # Dog
    [3, 9, 1, 7],    # Dog
    [7, 3, 7, 4],    # Cat
])

y_train = [1, 1, 0, 0, 1]  # 1 = Cat, 0 = Dog

# IMPORTANT: SVM needs scaled features!
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)

# Create SVM with RBF kernel (handles non-linear boundaries)
model = SVC(
    kernel='rbf',     # Radial Basis Function
    C=1.0,            # Regularization
    probability=True  # Enable probability estimates
)

# Train the model
model.fit(X_train_scaled, y_train)

# Make prediction
new_animal = [[7, 3, 8, 5]]
new_animal_scaled = scaler.transform(new_animal)

prediction = model.predict(new_animal_scaled)
probability = model.predict_proba(new_animal_scaled)[0]

print(f"Prediction: {'🐱 Cat' if prediction[0] else '🐶 Dog'}")
print(f"Cat probability: {probability[1]*100:.1f}%")
```

**Visual Understanding:**
```
       Ear Pointiness
              ↑
            9 | 🐱 🐱
              |   /
            6 |  / ← Maximum Margin
              | /
            3 |/_________ ← Decision Boundary
              |🐶     🐶
            0 |_________________→
              0   3   6   9      Nose Length
```

**Pros:**
- 🎯 Effective in high dimensions
- 💪 Works well with clear margins
- 🔧 Versatile with different kernels
- 📊 Memory efficient

**Cons:**
- ⏱️ Slow on large datasets
- ⚙️ Needs careful parameter tuning
- 📏 Requires feature scaling
- 🔒 Less interpretable

---

### 3.5 K-Nearest Neighbors (KNN) 👥

**What is it?**
"You are the average of the 5 people you hang out with" - KNN predicts based on the K closest neighbors!

**When to Use:**
- ✅ Small to medium datasets
- ✅ Simple, interpretable predictions
- ✅ No training time needed
- ✅ Non-parametric problems

**Real-World Example: Movie Recommendation**

```python
from sklearn.neighbors import KNeighborsClassifier
import numpy as np

# Sample data: [action_%, comedy_%, drama_%, runtime_hours]
movies_features = np.array([
    [80, 10, 10, 2.0],  # Action movie → User liked
    [85, 5, 10, 2.5],   # Action movie → User liked
    [10, 80, 10, 1.5],  # Comedy → User disliked
    [5, 85, 10, 1.8],   # Comedy → User disliked
    [20, 20, 60, 2.2],  # Drama → User liked
])

user_preferences = [1, 1, 0, 0, 1]  # 1 = Like, 0 = Dislike

# Create KNN classifier (K=3 means look at 3 nearest neighbors)
model = KNeighborsClassifier(n_neighbors=3)
model.fit(movies_features, user_preferences)

# New movie to predict
new_movie = [[75, 15, 10, 2.1]]  # Action-focused movie

# Find nearest neighbors
distances, indices = model.kneighbors(new_movie)

print("📽️ Nearest neighbor movies:")
for i, (dist, idx) in enumerate(zip(distances[0], indices[0]), 1):
    print(f"  {i}. Movie {idx+1} (distance: {dist:.2f})")

# Make prediction
prediction = model.predict(new_movie)
probability = model.predict_proba(new_movie)[0]

print(f"\n{'👍 User will like' if prediction[0] else '👎 User will dislike'}")
print(f"Confidence: {max(probability)*100:.1f}%")
```

**Visual Understanding:**
```
        Comedy %
            ↑
          80|  ⭕ ⭕  (Disliked comedies)
            |
          40|     🎬 ← New Movie
            |        \
            |         \__3 nearest neighbors
            |    ⭐ ⭐   (2 liked, 1 disliked)
            |     ⭐
            |________________→ Action %
                  80

Prediction: Majority vote = LIKE 👍
```

**Pros:**
- 🚀 No training time
- 📖 Simple to understand
- 🎯 Naturally handles multi-class
- 🔧 No assumptions about data

**Cons:**
- 🐢 Slow predictions on large data
- 💾 High memory usage
- 📏 Needs feature scaling
- ⚠️ Sensitive to irrelevant features

---

### 📊 Classification Models Comparison

| **Model** | **Speed** | **Accuracy** | **Interpretability** | **Best For** |
|-----------|-----------|--------------|----------------------|--------------|
| Logistic Regression | ⚡⚡⚡ | ⭐⭐ | 📖📖📖 | Simple binary problems |
| Decision Tree | ⚡⚡⚡ | ⭐⭐ | 📖📖📖 | Explainable decisions |
| Random Forest | ⚡⚡ | ⭐⭐⭐ | 📖 | High accuracy needed |
| SVM | ⚡ | ⭐⭐⭐ | 📖 | Clear boundaries |
| KNN | ⚡ | ⭐⭐ | 📖📖 | Small datasets |

---

<a name="section-4"></a>
## 📈 Section 4: Regression Models

### 4.1 Linear Regression 📏

**What is it?**
Drawing the best straight line through your data points to predict numbers. Like predicting height based on age!

**Real-World Example: House Price Prediction**

```python
from sklearn.linear_model import LinearRegression
import matplotlib.pyplot as plt
import numpy as np

# Sample data: House size (sq ft) and Price ($1000s)
house_sizes = np.array([1000, 1500, 2000, 2500, 3000]).reshape(-1, 1)
prices = np.array([150, 200, 250, 300, 350])

# Create and train model
model = LinearRegression()
model.fit(house_sizes, prices)

# Get the equation: Price = slope × size + intercept
slope = model.coef_[0]
intercept = model.intercept_

print(f"📐 Equation: Price = {slope:.2f} × Size + {intercept:.2f}")

# Predict price for 2200 sq ft house
new_house = [[2200]]
predicted_price = model.predict(new_house)
print(f"🏠 Predicted price for 2200 sq ft: ${predicted_price[0]:.0f}k")

# Visualize
plt.scatter(house_sizes, prices, color='blue', label='Actual')
plt.plot(house_sizes, model.predict(house_sizes), color='red', label='Prediction')
plt.xlabel('House Size (sq ft)')
plt.ylabel('Price ($1000s)')
plt.legend()
plt.title('Linear Regression: House Prices')
plt.show()
```

---

### 4.2 Ridge and Lasso Regression 🛡️

**What are they?**
Enhanced versions of Linear Regression that prevent overfitting by adding penalties.

**When to Use:**
- ✅ Many features (possible overfitting)
- ✅ Correlated features
- ✅ Need feature selection (Lasso)

```python
from sklearn.linear_model import Ridge, Lasso

# Ridge: Keeps all features, shrinks coefficients
ridge_model = Ridge(alpha=1.0)  # alpha controls penalty

# Lasso: Can eliminate features by setting coefficients to zero
lasso_model = Lasso(alpha=1.0)

# Both trained same way as Linear Regression
ridge_model.fit(X_train, y_train)
lasso_model.fit(X_train, y_train)
```

---

<a name="section-6"></a>
## ✅ Section 6: Training and Validation

### 6.1 Train-Test Split 🎯

**Why Split Data?**

Imagine studying for an exam:
- 📚 **Training Set** = Practice problems you study from
- 📝 **Test Set** = Actual exam questions (should be unseen!)

```python
from sklearn.model_selection import train_test_split

# Split data: 80% training, 20% testing
X_train, X_test, y_train, y_test = train_test_split(
    X, y, 
    test_size=0.2,     # 20% for testing
    random_state=42    # For reproducibility
)

print(f"Training samples: {len(X_train)}")
print(f"Testing samples: {len(X_test)}")
```

---

### 6.2 Cross-Validation Explained 🔄

**Visual Understanding:**
```
Original Data: [████████████████████]

Split 1:  [■■■■TEST■■■■|TRAIN|TRAIN|TRAIN|TRAIN]
Split 2:  [TRAIN|■■■■TEST■■■■|TRAIN|TRAIN|TRAIN]
Split 3:  [TRAIN|TRAIN|■■■■TEST■■■■|TRAIN|TRAIN]
Split 4:  [TRAIN|TRAIN|TRAIN|■■■■TEST■■■■|TRAIN]
Split 5:  [TRAIN|TRAIN|TRAIN|TRAIN|■■■■TEST■■■■]

Final Score = Average of all 5 tests
```

```python
from sklearn.model_selection import cross_val_score

model = RandomForestClassifier()

# Perform 5-fold cross-validation
scores = cross_val_score(model, X, y, cv=5)

print(f"Scores for each fold: {scores}")
print(f"Average accuracy: {scores.mean():.2%} (+/- {scores.std():.2%})")
```

---

<a name="section-7"></a>
## 📏 Section 7: Model Evaluation Metrics

### 7.1 Classification Metrics

**Confusion Matrix Explained:**

```
                    Predicted
                 No  |  Yes
              _____|_____
        No   | TN  | FP  |  ← False Positive (False Alarm)
Actual       |_____|_____|
        Yes  | FN  | TP  |  ← True Positive (Correct!)
             |_____|_____|
               ↑
        False Negative
        (Missed Detection)
```

**Medical Example:**
```python
from sklearn.metrics import classification_report, confusion_matrix

# Disease prediction
y_true = [0, 0, 1, 1, 0, 1]  # Actual
y_pred = [0, 1, 1, 1, 0, 1]  # Predicted

print(confusion_matrix(y_true, y_pred))
print(classification_report(y_true, y_pred))
```

---

<a name="section-8"></a>
## ⚙️ Section 8: Hyperparameter Tuning

**What are Hyperparameters?**

Think of baking a cake:
- 🌡️ Oven temperature
- ⏰ Baking time  
- 🥄 Ingredient amounts

These are settings you choose BEFORE baking (training)!

```python
from sklearn.model_selection import GridSearchCV

# Define parameter grid
param_grid = {
    'n_estimators': [50, 100, 200],      # Number of trees
    'max_depth': [5, 10, 15],            # Tree depth
    'min_samples_split': [2, 5, 10]      # Min samples to split
}

# Create grid search
grid_search = GridSearchCV(
    RandomForestClassifier(),
    param_grid,
    cv=5,              # 5-fold cross-validation
    scoring='accuracy'
)

# Find best parameters
grid_search.fit(X_train, y_train)

print(f"🏆 Best parameters: {grid_search.best_params_}")
print(f"🎯 Best score: {grid_search.best_score_:.2%}")
```

---

<a name="section-9"></a>
## 🛡️ Section 9: Avoiding Overfitting

**Visual Understanding:**

```
Underfitting          Good Fit           Overfitting
     ⭐                   ⭐                   ⭐
   ⭐  ⭐               ⭐  ⭐               ⭐  ⭐
  ⭐    ⭐             ⭐    ⭐             ⭐────⭐
   ────                  ╱╲                  ╱│╲
                       ╱    ╲              ╱  │  ╲
                                          ╱   │   ╲

Too Simple          Just Right         Too Complex
(High Bias)      (Balanced)      (High Variance)
```

**Prevention Techniques:**

1. **More Data** 📊
2. **Cross-Validation** 🔄
3. **Regularization** 🛡️
4. **Early Stopping** ⏸️
5. **Feature Selection** ✂️

---

<a name="section-10"></a>
## 🚀 Section 10: Complete Pipeline

**Full Example: End-to-End Model Development**

```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split, cross_val_score
import joblib

# 1️⃣ Load and split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 2️⃣ Create pipeline
pipeline = Pipeline([
    ('scaler', StandardScaler()),                    # Step 1: Scale
    ('classifier', RandomForestClassifier(n_estimators=100))  # Step 2: Classify
])

# 3️⃣ Train with cross-validation
cv_scores = cross_val_score(pipeline, X_train, y_train, cv=5)
print(f"CV Scores: {cv_scores.mean():.2%} (+/- {cv_scores.std():.2%})")

# 4️⃣ Fit final model
pipeline.fit(X_train, y_train)

# 5️⃣ Evaluate
test_score = pipeline.score(X_test, y_test)
print(f"Test Accuracy: {test_score:.2%}")

# 6️⃣ Save model
joblib.dump(pipeline, 'my_model.pkl')

# 7️⃣ Load and use later
loaded_model = joblib.load('my_model.pkl')
predictions = loaded_model.predict(new_data)
```

---

## 🎓 Practice Exercises

### Exercise 1: Simple Classification
Build a spam detector using logistic regression with the provided email dataset.

### Exercise 2: Regression Challenge
Predict taxi trip duration using random forest regression.

### Exercise 3: Model Comparison
Compare 3 different models and explain which performs best.

### Exercise 4: Full Pipeline
Create an end-to-end pipeline with preprocessing and model training.

---

## 📚 Additional Resources

- 📖 [Scikit-learn Documentation](https://scikit-learn.org/)
- 🎥 [StatQuest YouTube Channel](https://youtube.com/statquest)
- 📊 [Kaggle Learn](https://www.kaggle.com/learn)
- 💡 [Machine Learning Mastery](https://machinelearningmastery.com/)

---

## ✅ Module Completion Checklist

- [ ] Understand different model types
- [ ] Can choose appropriate model for problem
- [ ] Can train classification models
- [ ] Can train regression models
- [ ] Understand cross-validation
- [ ] Can evaluate model performance
- [ ] Can tune hyperparameters
- [ ] Understand overfitting prevention
- [ ] Can build complete pipeline

---

## 🤝 Contributing

Found an error? Have suggestions? We welcome contributions!

See [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines.

---

## 📞 Need Help?

- 💬 Join our [Discussion Forum](link)
- 📧 Email: support@mlcourse.com
- 🐛 Report issues on [GitHub](link)

---

**Last Updated:** January 2026
**Module Status:** ✅ Complete
**Estimated Time:** 8-10 hours

---

**Next Module:** [Module 06: Model Evaluation and Interpretation](../module-06/README.md) 🎯
