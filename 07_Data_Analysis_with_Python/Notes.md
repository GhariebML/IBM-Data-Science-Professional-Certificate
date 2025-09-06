# 📝 Notes – Data Analysis with Python

## 📄 Overview
This course focuses on analyzing data with Python.  
We cover **data wrangling**, **exploratory data analysis (EDA)**, **statistical analysis**, and **building regression models**.

---

## 1️⃣ Data Wrangling
**Purpose**: Clean and prepare raw data for analysis.

**Key Functions (Pandas):**
```python
import pandas as pd

# Read data
df = pd.read_csv("dataset.csv")

# Check data info
df.info()

# Handle missing values
df.dropna(inplace=True)  # remove missing rows
df.fillna(value=0, inplace=True)  # replace missing with 0

# Convert data types
df['date'] = pd.to_datetime(df['date'])

# Remove duplicates
df.drop_duplicates(inplace=True)
````

---

## 2️⃣ Exploratory Data Analysis (EDA)

**Purpose**: Understand dataset structure and find patterns.

**Descriptive statistics:**

```python
# Summary statistics
df.describe()

# Unique values in a column
df['category'].value_counts()
```

**Visualization:**

```python
import matplotlib.pyplot as plt
import seaborn as sns

# Histogram
sns.histplot(df['price'], bins=20)
plt.show()

# Correlation heatmap
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.show()
```

---

## 3️⃣ Statistical Analysis

**Hypothesis Testing** – t-test example:

```python
from scipy import stats

group1 = df[df['category'] == 'A']['sales']
group2 = df[df['category'] == 'B']['sales']

t_stat, p_value = stats.ttest_ind(group1, group2)
print("T-statistic:", t_stat, "P-value:", p_value)
```

---

## 4️⃣ Model Development

**Linear Regression Example:**

```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split

X = df[['feature1', 'feature2']]
y = df['target']

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Model
model = LinearRegression()
model.fit(X_train, y_train)

# Predictions
y_pred = model.predict(X_test)
```

---

## 5️⃣ Model Evaluation

**Metrics for Regression:**

```python
from sklearn.metrics import mean_squared_error, r2_score

mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print("MSE:", mse)
print("R²:", r2)
```

---

## 6️⃣ Practical Tips

* Always check for **missing data** before starting analysis.
* Visualizations help uncover **outliers** and **relationships**.
* Feature engineering can significantly improve model performance.
* Keep your code clean with comments and section titles.

---
