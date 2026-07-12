# 🛍️ Customer Segmentation using K-Means & DBSCAN

> **Machine Learning Internship Project – Elevvo (Task 02)**

Customer segmentation is one of the most important applications of **Unsupervised Machine Learning** in retail analytics. This project applies **K-Means Clustering** to segment mall customers based on their purchasing behavior using **Annual Income** and **Spending Score**. The optimal number of clusters is determined using both the **Elbow Method** and **Silhouette Score Analysis**.

As a bonus, **DBSCAN** is implemented and compared with K-Means to evaluate the strengths and limitations of different clustering algorithms.

---

# 📌 Project Objectives

- Perform customer segmentation using **Unsupervised Learning**
- Analyze customer behavior through **Exploratory Data Analysis (EDA)**
- Select meaningful features for clustering
- Apply **Feature Scaling** for distance-based learning
- Determine the optimal number of clusters using:
  - Elbow Method
  - Silhouette Score
- Train the **K-Means** clustering model
- Visualize customer segments
- Generate actionable business insights
- Compare **K-Means** with **DBSCAN**

---

# 📂 Dataset Information

**Dataset:** Mall Customers Dataset

| Property | Value |
|----------|-------|
| Total Samples | 200 |
| Total Features | 5 |
| Learning Type | Unsupervised Learning |
| Missing Values | None |
| Duplicate Rows | None |
| Target Variable | None |

### Features

- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

---

# ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 🔄 Project Workflow

```text
Mall Customer Dataset
        │
        ▼
Data Quality Assessment
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Feature Scaling
        │
        ▼
Optimal K Selection
(Elbow + Silhouette)
        │
        ▼
K-Means Clustering
        │
        ▼
Cluster Visualization
        │
        ▼
Business Insights
        │
        ▼
Model Evaluation
        │
        ▼
DBSCAN Comparison
```

---

# 📊 Exploratory Data Analysis (EDA)

The dataset was explored through multiple analytical perspectives:

### ✔ Univariate Analysis

- Customer Distribution
- Gender Distribution
- Age Distribution
- Annual Income Distribution
- Spending Score Distribution

### ✔ Bivariate Analysis

- Age vs Spending Score
- Age vs Annual Income
- Annual Income vs Spending Score
- Gender vs Spending Score
- Gender vs Annual Income
- Gender vs Age

### ✔ Multivariate Analysis

- Pair Plot
- Customer Relationship Analysis

### ✔ Correlation Analysis

- Correlation Matrix
- Heatmap

### ✔ Outlier Analysis

- Age
- Annual Income
- Spending Score

---

# 🛠 Feature Engineering

Feature evaluation was performed before clustering.

### Selected Features

- Annual Income (k$)
- Spending Score (1-100)

### Excluded Features

- CustomerID (Identifier)
- Gender (Categorical)
- Age (Used for exploratory analysis but excluded from the baseline clustering model)

---

# 📈 Feature Scaling

Since K-Means relies on **Euclidean Distance**, feature scaling was performed using **StandardScaler**.

Benefits:

- Equal contribution of all features
- Improved centroid estimation
- Better clustering performance

---

# 📉 Choosing the Optimal Number of Clusters

Two evaluation techniques were used:

### ✔ Elbow Method

Used to identify the point where additional clusters provide diminishing improvements in WCSS.

### ✔ Silhouette Score

Used to evaluate:

- Cluster Cohesion
- Cluster Separation

---

# 🤖 K-Means Clustering

The final K-Means model was trained using:

- Number of Clusters = **5**
- Initialization = **k-means++**
- Random State = **42**
- n_init = **10**

---

# 📊 Model Performance

| Metric | Result |
|---------|---------|
| Algorithm | K-Means |
| Optimal K | **5** |
| Silhouette Score | **0.5547** |
| WCSS (Inertia) | **65.568** |
| Number of Features | **2** |
| Training Samples | **200** |
| Iterations to Converge | **4** |

---

# 👥 Customer Segments

| Cluster | Business Segment | Characteristics |
|----------|------------------|-----------------|
| 0 | Regular Customers | Moderate Income • Moderate Spending |
| 1 | Premium Customers | High Income • High Spending |
| 2 | Enthusiastic Shoppers | Low Income • High Spending |
| 3 | Careful Wealthy Customers | High Income • Low Spending |
| 4 | Budget Customers | Low Income • Low Spending |

---

# 💼 Business Insights

### 🟢 Regular Customers

- Stable purchasing behavior
- Ideal for loyalty programs

### 🟣 Premium Customers

- Highest-value customers
- VIP services and exclusive offers

### 🟡 Enthusiastic Shoppers

- High spending despite lower income
- Reward programs and cashback campaigns

### 🔴 Careful Wealthy Customers

- High purchasing power but low spending
- Personalized marketing opportunities

### 🔵 Budget Customers

- Cost-conscious customers
- Discount-based promotional campaigns

---

# 📊 Model Evaluation

The clustering model was evaluated using multiple perspectives.

### Internal Evaluation

- Silhouette Score
- WCSS (Inertia)
- Cluster Compactness
- Cluster Separation

### Business Evaluation

The resulting clusters are:

- Well separated
- Interpretable
- Actionable
- Suitable for targeted marketing

---

# ⭐ Bonus: DBSCAN Comparison

To compare clustering algorithms, **DBSCAN** was implemented.

| Criteria | K-Means | DBSCAN |
|----------|----------|----------|
| Algorithm | Centroid Based | Density Based |
| Number of Clusters | **5** | **6** |
| Silhouette Score | **0.5547** | **0.4368** |
| Requires K | Yes | No |
| Detects Noise | No | Yes |

### Conclusion

Although DBSCAN successfully detected noise and identified dense regions, **K-Means achieved a higher Silhouette Score and produced more interpretable customer segments**, making it the preferred clustering algorithm for this dataset.

---

# 📁 Repository Structure

```text
elevvo-internship-task02-customer-segmentation/
│
├── data/
│   └── Mall_Customers.csv
│
├── notebook/
│   └── Customer_Segmentation.ipynb
│
├── images/
│   ├── Correlation Heatmap.png
│   ├── Customer Distribution Across Clusters.png
│   ├── Customer Segmentation using DBSCAN.png
│   ├── Customer Segmentation using K-Means.png
│   └── Elbow Method.png
│   └── Silhouette Score Analysis.png
├── README.md
├── requirements.txt
└── LICENSE
```

---

# ▶️ How to Run

### Clone the repository

```bash
git clone https:[//github.com/Delwar2004/elevvo-internship-task02-customer-segmentation.git](https://github.com/Delwar2004/elevvo-internship-task02-customer-segmentation)
```

### Navigate to the project

```bash
cd elevvo-internship-task02-customer-segmentation
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```
Customer_Segmentation.ipynb
```

---

# 🚀 Future Improvements

- Compare with Hierarchical Clustering
- Hyperparameter tuning for DBSCAN
- Evaluate using Calinski–Harabasz Index
- Evaluate using Davies–Bouldin Index
- Deploy an interactive customer segmentation dashboard
- Build a real-time customer recommendation system

---

# 🎯 Key Takeaways

- Successfully segmented customers into **five meaningful groups**
- Achieved a **Silhouette Score of 0.5547**
- Identified actionable customer segments for targeted marketing
- Demonstrated the complete **Machine Learning pipeline** for an unsupervised learning problem
- Compared **K-Means** with **DBSCAN** to validate algorithm selection

---

# 👨‍💻 Author

**Md Delwar Husen**

Machine Learning Intern @ Elevvo
Dept of Information & Communication Engineering(ICE)
Bangladesh University Of Professionals(BUP)

GitHub: https:[//github.com/Delwar2004](https://github.com/Delwar2004)

---

## ⭐ If you found this project helpful, consider giving it a star!
