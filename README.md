# ML-Basics-and-fundamentals


Here is the complete, high-level map of Machine Learning structured as a flowchart/tree, followed by a categorical breakdown of each branch, when to use them, and which algorithms belong where.

---

### Machine Learning Taxonomy (The Map)

```text
                        MACHINE LEARNING
                               │
       ┌───────────────────────┼───────────────────────┐
       ▼                       ▼                       ▼
  SUPERVISED              UNSUPERVISED           REINFORCEMENT
   LEARNING                 LEARNING                LEARNING
 (Labeled Data)         (Unlabeled Data)        (Reward/Penalty)
       │                       │                       │
 ┌─────┴─────┐           ┌─────┴─────┐                 │
 ▼           ▼           ▼           ▼                 ▼
REGRESSION  CLASS-  CLUSTERING  DIMENSIONALITY    Game AI,
           IFICATION              REDUCTION       Robotics
```

---

## 1. Types of Machine Learning

Machine Learning is divided into **three main types**:

### A. Supervised Learning
* **What it is:** The algorithm is trained on a dataset where the **correct answers (labels) are already given**. 
* **Input ($X$):** Features (e.g., house size, location).
* **Output ($y$):** Known target label (e.g., house price).
* **Goal:** Learn the mapping function between $X$ and $y$.

---

### B. Unsupervised Learning
* **What it is:** The algorithm gets data **without any answers or labels**.
* **Goal:** Find hidden patterns, groupings, or structures in the raw data automatically.

---

### C. Reinforcement Learning
* **What it is:** An agent learns by interacting with an environment through **trial and error**, getting **rewards** for good actions and **penalties** for bad ones.
* **Goal:** Maximize cumulative reward (e.g., self-driving cars, chess-playing bots).

---

## 2. Deep Dive: Supervised Learning

Supervised learning is split into two categories based on **what you are trying to predict**:

```text
                  SUPERVISED LEARNING
                           │
         ┌─────────────────┴─────────────────┐
         ▼                                   ▼
    REGRESSION                         CLASSIFICATION
(Predicting Numbers)               (Predicting Categories)
```

---

### Branch 1: REGRESSION

#### **When to use Regression?**
Use Regression when your target variable ($y$) is a **Continuous Numerical Value** (a number that can vary smoothly across a scale).

* **Examples:**
  * Predicting employee salary (e.g., ₹50,000 to ₹1,50,000).
  * Predicting house prices based on square footage.
  * Predicting daily temperature in Celsius.

#### **Algorithms under Regression:**

| Algorithm | Simple Definition | Best For |
| :--- | :--- | :--- |
| **Linear Regression** | Draws a straight line through the data points. | Simple, linear relationships. |
| **Decision Tree Regressor** | Splits data into branches based on "if/then" rules to predict a number. | Non-linear data. |
| **Random Forest Regressor** | Combines predictions from multiple decision trees to average out errors. | Complex, high-accuracy needs. |
| **Support Vector Regressor (SVR)** | Finds a boundary line that keeps predictions within a specific margin of error. | Medium-sized, tricky datasets. |
| **KNN Regressor** | Takes the average output of the $K$ closest data points. | Simple datasets with clear physical proximity. |

---

### Branch 2: CLASSIFICATION

#### **When to use Classification?**
Use Classification when your target variable ($y$) is a **Discrete Category or Class** (labels, groups, or yes/no outputs).

* **Examples:**
  * Predicting whether an email is **Spam** or **Not Spam**.
  * Predicting whether a loan applicant will **Default** or **Not Default**.
  * Predicting image type: **Cat**, **Dog**, or **Bird**.

#### **Types of Classification:**
1. **Binary Classification:** Only 2 outcomes (e.g., Yes/No, 0/1).
2. **Multi-class Classification:** More than 2 distinct categories (e.g., Red/Blue/Green).

#### **Algorithms under Classification:**

| Algorithm | Simple Definition | Best For |
| :--- | :--- | :--- |
| **Logistic Regression** | *Note: Despite the name "Regression", this is a Classification model!* Outputs probabilities between 0 and 1. | Simple binary choices (Yes/No). |
| **K-Nearest Neighbors (KNN)** | Classifies an unknown point based on the majority class of its nearest neighbors. | Simple, small datasets. |
| **Decision Tree Classifier** | Uses a flowchart-like structure of "if/then" questions to assign a class label. | Easy-to-explain classification rules. |
| **Random Forest Classifier** | Builds an "ensemble" (forest) of many decision trees and picks the majority vote. | High accuracy, complex multi-feature data. |
| **Support Vector Machine (SVM)** | Finds the best hyper-plane (decision boundary) that separates classes with maximum margin. | Clear-cut separation between classes. |
| **Naive Bayes** | Calculates output probability using Bayes' Theorem (assumes features are independent). | Text classification (e.g., spam detection). |

---

## 3. Deep Dive: Unsupervised Learning

```text
                 UNSUPERVISED LEARNING
                           │
         ┌─────────────────┴─────────────────┐
         ▼                                   ▼
    CLUSTERING                     DIMENSIONALITY REDUCTION
(Grouping Data)                        (Simplifying Data)
```

1. **Clustering:** Automatically groups similar items together.
   * *Algorithms:* **K-Means Clustering**, **Hierarchical Clustering**, **DBSCAN**.
   * *When to use:* Customer segmentation (grouping users by buying habits without pre-existing labels).

2. **Dimensionality Reduction:** Reduces the number of features/columns in a large dataset while keeping essential information.
   * *Algorithms:* **PCA (Principal Component Analysis)**, **t-SNE**.
   * *When to use:* Data visualization, compressing datasets with hundreds of features.

---

## Summary Decision Tree: How to Pick Your Model

```text
                        START
                          │
             Is your data labeled (has target y)?
                          │
               ┌──────────┴──────────┐
               YES                   NO
               │                     │
      SUPERVISED LEARNING    UNSUPERVISED LEARNING
               │                     │
      Is Target (y) a        Are you trying to group data
      Number or Category?    or shrink features?
         ┌─────┴─────┐              ┌─────┴─────┐
      NUMBER     CATEGORY        GROUPING    SHRINK
         │           │              │           │
     REGRESSION  CLASSIFICATION CLUSTERING  DIM. REDUCTION
         │           │              │           │
     - Linear     - Logistic     - K-Means   - PCA
     - Forest     - Random       - DBSCAN    - t-SNE
       Regressor    Forest 
                  - KNN
```

---

### Ready for your files!
Send over your training files, assignments, or slides whenever you are ready. I will review them and explain the exact code, models, or data structures being used in them based on this taxonomy.
