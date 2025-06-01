# 🧪 Notes – Python Project for Data Science

This project-based course provided a hands-on opportunity to apply Python skills to a real-world dataset involving SpaceX Falcon 9 launches.

---

## 🔍 1. Project Overview

- **Objective**: Analyze Falcon 9 launch data and predict the likelihood of a successful first-stage landing using classification models.
- **Tools**: Python, Jupyter Notebook, Pandas, NumPy, Plotly, BeautifulSoup, Folium, Scikit-learn.

---

## 🌐 2. Data Collection

### ✅ Web Scraping
- Used `BeautifulSoup` to scrape SpaceX launch data from [Wikipedia](https://en.wikipedia.org/wiki/Falcon_9).
- Extracted relevant columns: Launch date, Site, Payload mass, Orbit, Launch outcome.

### ✅ SpaceX API
- Accessed LaunchPad location data via the SpaceX REST API.
- Mapped launch locations using `Folium`.

---

## 🧹 3. Data Wrangling

### ✅ Cleaning Tasks
- Replaced "NaN" and empty cells
- Converted data types (e.g., payload mass to float)
- Encoded categorical variables (e.g., Launch Site)

---

## 📊 4. Data Analysis & Visualization

### ✅ Visual Tools Used
- `Plotly` for bar charts, pie charts, scatter plots
- `Folium` for geographic launch site visualization

### 📈 Insights Gained
- Launch success rates by site
- Correlation between payload mass and success
- Launch outcome distribution across time and orbit types

---

## 🧠 5. Machine Learning – Classification Model

### ✅ Features Used
- Payload mass
- Launch site (one-hot encoded)
- Orbit type
- Flight number

### ✅ Model Applied
- Logistic Regression via `Scikit-learn`
- Train-test split and model evaluation using accuracy score and confusion matrix

---

## 📌 6. Summary & Takeaways

- First real end-to-end data science project experience
- Scraping and cleaning data manually improved my understanding of real-world data issues
- Visualization tools helped uncover meaningful patterns
- Built and interpreted a basic classification model
- Strengthened workflow skills using Jupyter Notebooks

---

## 📁 Project Structure

