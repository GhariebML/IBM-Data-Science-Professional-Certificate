# Machine Learning with Python — Notes

Part of the **IBM Data Science Professional Certificate**.

---

## 1️⃣ Introduction to Machine Learning
- **Definition:** Field of AI that enables computers to learn patterns from data and make predictions.
- **Types of Machine Learning:**
  - **Supervised Learning:** Labeled data, prediction tasks (e.g., regression, classification).
  - **Unsupervised Learning:** Unlabeled data, pattern finding (e.g., clustering).
  - **Reinforcement Learning:** Agents learn by interacting with an environment and receiving rewards/punishments.

---

## 2️⃣ Supervised Learning

### 🔹 Regression
- Predicts continuous values.
- **Example algorithms:**
  - Linear Regression
  - Polynomial Regression
- **Code Example:**
```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
````

### 🔹 Classification

* Predicts discrete categories.
* **Example algorithms:**

  * Logistic Regression
  * Decision Trees
  * K-Nearest Neighbors (KNN)
  * Support Vector Machines (SVM)
* **Code Example:**

```python
from sklearn.neighbors import KNeighborsClassifier

knn = KNeighborsClassifier(n_neighbors=3)
knn.fit(X_train, y_train)
y_pred = knn.predict(X_test)
```

---

## 3️⃣ Unsupervised Learning

### 🔹 Clustering

* Groups similar data points together.
* **Example algorithms:**

  * K-Means
  * Hierarchical Clustering
* **Code Example:**

```python
from sklearn.cluster import KMeans

kmeans = KMeans(n_clusters=3)
kmeans.fit(X)
labels = kmeans.labels_
```

---

## 4️⃣ Model Evaluation

* **Regression metrics:** Mean Squared Error (MSE), R² Score
* **Classification metrics:** Accuracy, Precision, Recall, F1-score
* **Cross-validation:** Splits data into multiple folds to improve generalization.

```python
from sklearn.metrics import accuracy_score, confusion_matrix

print("Accuracy:", accuracy_score(y_test, y_pred))
print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
```

---

## 5️⃣ Recommender Systems

* **Content-based filtering:** Recommends items similar to those a user liked.
* **Collaborative filtering:** Recommends items based on user similarity.
* Implemented using similarity measures like cosine similarity.

---

## 6️⃣ Libraries Used

* **Pandas:** Data manipulation
* **NumPy:** Numerical computing
* **Matplotlib & Seaborn:** Data visualization
* **Scikit-learn:** ML algorithms and tools

---

## 7️⃣ Final Project

* Built a machine learning model using real-world dataset.
* Applied:

  * Data cleaning and preprocessing
  * Feature selection
  * Model training and tuning
  * Performance evaluation

---

## 📜 Certificate

🔗 [Verify Certificate](https://www.coursera.org/account/accomplishments/specialization/certificate/9JPL43YELY5B)

```
