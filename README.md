# 🌳 Decision Tree Classification on Iris Dataset

## 📌 Project Overview

This project demonstrates how to build and evaluate a **Decision Tree Classifier** using the famous **Iris Dataset** from Scikit-learn.

The project covers the complete Machine Learning workflow:

* Loading and exploring the dataset
* Data visualization (EDA)
* Train-Test splitting
* Training Decision Tree models
* Comparing **Entropy** and **Gini Index**
* Evaluating model performance
* Visualizing the decision boundaries
* Visualizing the Decision Tree structure

This project was created as part of my Machine Learning practice to understand how Decision Trees make classification decisions.

---

# 📂 Dataset

The project uses the built-in **Iris Dataset** available in Scikit-learn.

The dataset contains **150 flower samples** belonging to three different species:

* Iris Setosa
* Iris Versicolor
* Iris Virginica

Each flower has four features:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

For this project, only the first two features were used:

* Sepal Length
* Sepal Width

---

# 🛠 Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

# 📊 Exploratory Data Analysis (EDA)

Before training the model, the dataset was explored using:

* Dataset preview
* Dataset information
* Missing value checking
* Pairplot visualization

This helps us understand feature relationships before building the model.

---

# 🌳 What is a Decision Tree?

A Decision Tree is a Machine Learning algorithm that learns by asking a series of simple questions.

Think of it like a flowchart.

Example:

```
Is Sepal Length ≤ 5.5 ?

       Yes
        |
     Predict Setosa

       No
        |
 Is Sepal Width ≤ 3.2 ?

     Yes      No
      |        |
Versicolor  Virginica
```

The tree keeps asking questions until it reaches the final prediction.

---

# 🧠 How the Decision Tree Algorithm Works  

Imagine you have a basket of different flowers.

The Decision Tree wants to separate these flowers into the correct categories.

### Step 1 — Look at all features

The algorithm checks every feature.

For example:

* Sepal Length
* Sepal Width

It asks:

> "Which feature separates the flowers the best?"

---

### Step 2 — Find the Best Split

The algorithm tests many possible splitting points.

Example:

```
Sepal Length ≤ 5.4 ?

Yes
No

Sepal Length ≤ 5.8 ?

Yes
No

Sepal Length ≤ 6.1 ?

Yes
No
```

It calculates which split creates the purest groups.

---

### Step 3 — Create the First Decision

The best split becomes the root of the tree.

Example:

```
           Sepal Length ≤ 5.45
             /            \
          Yes              No
```

---

### Step 4 — Repeat the Same Process

The algorithm repeats the same process for every branch.

Each branch asks another question.

```
             Root
            /    \
         Node    Node
         /          \
      Leaf        Node
                  /   \
               Leaf  Leaf
```

This process continues until:

* Maximum depth is reached
* All samples belong to one class
* No better split exists

---

### Step 5 — Make Predictions

When a new flower is given,

the algorithm starts from the root.

It answers each question.

It follows the path until it reaches a leaf node.

The leaf node gives the final prediction.

---

# 🌟 Recursive Nature of Decision Trees

Decision Trees are **recursive algorithms**.

Recursion means:

The same process is repeated again and again on smaller subsets of data.

Example:

```
Whole Dataset
      |
 Best Split
      |
-----------------
|               |
Subset A      Subset B
|               |
Split Again   Split Again
|               |
More Splits   More Splits
```

Each child node behaves exactly like the parent node.

It again searches for the best feature.

It again finds the best split.

It again creates new branches.

This recursive process continues until stopping conditions are met.

---

# 📐 Splitting Criteria

This project compares two methods for finding the best split.

## 1️⃣ Entropy

Entropy measures the amount of disorder or uncertainty.

Higher entropy means the data is more mixed.

Lower entropy means the data is more organized.

Formula:

```
Entropy = -Σ p log₂(p)
```

Goal:

Reduce entropy after every split.

---

## 2️⃣ Information Gain

Information Gain measures how much uncertainty decreases after splitting.

Higher Information Gain means a better split.

Formula:

```
Information Gain

= Parent Entropy

− Weighted Child Entropies
```

The algorithm always chooses the split with the highest Information Gain.

---

## 3️⃣ Gini Index

Gini measures impurity.

Formula:

```
Gini = 1 − Σ(p²)
```

Lower Gini means a purer node.

The Decision Tree chooses the split with the lowest Gini impurity.

---

# 📈 Model Training

Two Decision Tree models were trained.

### Model 1

* Criterion: Entropy
* Max Depth: 4

Accuracy:

```
66.67%
```

---

### Model 2

* Criterion: Gini
* Max Depth: 3

Accuracy:

```
76.67%
```

The Gini model achieved better performance on this train-test split.

---

# 📊 Model Evaluation

The project evaluates the model using:

* Accuracy Score
* Classification Predictions
* Decision Boundary
* Decision Tree Visualization

---

# 📉 Decision Boundary Visualization

The decision boundary shows how the model divides the feature space.

Each colored region represents the class predicted by the Decision Tree.

Straight horizontal and vertical boundaries appear because Decision Trees create **axis-parallel splits**.

---

# 🌲 Decision Tree Visualization

The tree diagram displays:

* Decision rules
* Split feature
* Threshold values
* Gini/Entropy values
* Number of samples
* Predicted class

This makes the model highly interpretable.

---

# 📁 Project Structure

```
Decision-Tree-Iris/
│
├── decision_tree.ipynb
├── README.md
└── images/
    ├── pairplot.png
    ├── entropy_boundary.png
    ├── entropy_tree.png
    ├── gini_boundary.png
    └── gini_tree.png
```

---

# 🚀 Future Improvements

* Use all four Iris features
* Perform feature importance analysis
* Apply GridSearchCV for hyperparameter tuning
* Compare Decision Tree with Random Forest
* Add cross-validation
* Evaluate Precision, Recall, and F1-Score
* Export the trained model using Joblib

---

# 🎯 Key Learning Outcomes

After completing this project, I learned:

* How Decision Trees perform classification
* How recursive splitting builds a tree
* Difference between Entropy and Gini Index
* Information Gain concept
* Model training and evaluation
* Decision boundary visualization
* Decision Tree structure interpretation
* Basic Machine Learning workflow using Scikit-learn

---

# 👩‍💻 Author

**Manahilch18**

Machine Learning & Generative AI Learner

"The best way to understand a machine learning algorithm is to build it yourself."

⭐ If this helped you, consider giving it a star — it means a lot!
