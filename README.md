# Customer Segmentation and Clustering

## 📊 Project Overview

This project focuses on understanding customer behavior through **data-driven segmentation** using clustering algorithms. The goal is to divide customers into distinct groups based on demographics, purchase behavior, and spending patterns. These insights help businesses design targeted marketing strategies, improve customer retention, and enhance profitability.

---

## 🎯 Objectives

* Perform **Exploratory Data Analysis (EDA)** to understand key customer attributes.
* Identify meaningful **customer segments** using clustering techniques.
* Derive actionable insights from data patterns for strategic business decisions.

---

## 🧰 Tools & Technologies

* **Programming Language:** Python
* **Libraries:** pandas, NumPy, matplotlib, seaborn, scikit-learn
* **Environment:** Jupyter Notebook / VS Code
* **Version Control:** Git & GitHub

---

## 🧩 Data Description

The dataset includes the following fields:

* **CustomerID:** Unique identifier for each customer
* **Gender:** Male/Female
* **Age:** Customer age
* **Annual Income (k$):** Annual income in thousands
* **Spending Score (1–100):** Score assigned by the store based on spending behavior

---

## 🔍 Data Analysis Steps

1. **Data Cleaning:**

   * Checked for null values, duplicates, and inconsistencies.
   * Standardized numerical values and formatted column names.

2. **Exploratory Data Analysis (EDA):**

   * Analyzed distributions and relationships between income, age, and spending score.
   * Visualized patterns using histograms, scatter plots, and correlation heatmaps.

3. **Clustering (K-Means & Hierarchical):**

   * Used the **Elbow Method** and **Silhouette Score** to determine optimal number of clusters.
   * Implemented K-Means and compared results with Hierarchical Clustering.

4. **Visualization:**

   * Created 2D and 3D cluster visualizations.
   * Highlighted distinct customer groups and their characteristics.

---

## 📈 Key Insights

* Identified 4–5 distinct customer segments based on income and spending score.
* High-income, high-spending customers form a premium segment ideal for loyalty programs.
* Low-income, low-spending customers require different engagement strategies.
* Middle-segment customers show potential for upselling through personalized marketing.

---

## 🧮 Sample Code Snippet

```python
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt

# Determine optimal clusters
wcss = []
for i in range(1, 11):
    kmeans = KMeans(n_clusters=i, random_state=42)
    kmeans.fit(X)
    wcss.append(kmeans.inertia_)

plt.plot(range(1, 11), wcss, marker='o')
plt.title('Elbow Method')
plt.xlabel('Number of clusters')
plt.ylabel('WCSS')
plt.show()
```




*This README was created for showcasing the Customer Segmentation and Clustering project on GitHub.*
