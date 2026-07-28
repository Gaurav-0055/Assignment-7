
# 🛍️ Customer Segmentation using K-Means Clustering & PCA

> AI-ML Assignment 7 — Segmenting mall customers for targeted marketing using unsupervised learning.

---

## 👤 Student Details

| Field | Details |
|---|---|
| **Name** | Gaurav Gour |
| **Registration No.** | 23BSA10096 |
| **Application No.** | IN26011516 |
| **Batch No.** | 1A |
| **Assignment** | Assignment - 7 |

---

## 🎯 Objective

To segment mall customers into distinct groups based on their **annual income** and **spending behavior** using **K-Means Clustering**, and to apply **Principal Component Analysis (PCA)** to visualize these clusters in two dimensions. The resulting segments support data-driven, targeted marketing campaigns for the mall's management.

---

## 📊 Dataset

| Detail | Info |
|---|---|
| **Name** | Mall Customer Segmentation Dataset |
| **Source** | Kaggle |
| **Link** | [View Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customersegmentation-tutorial-in-python) |
| **Features** | CustomerID, Gender, Age, Annual Income (k$), Spending Score (1–100) |

> ⚠️ Dataset is **not included** in this repository — please download it directly from Kaggle using the link above.

---

## 🛠️ Libraries Used

| Library | Purpose |
|---|---|
| 🐼 `pandas` | Data loading and manipulation |
| 🔢 `numpy` | Numerical operations |
| 📈 `matplotlib` | Plotting (elbow curve, scatter plots) |
| 🎨 `seaborn` | Enhanced statistical visualizations |
| 🤖 `scikit-learn` | `StandardScaler`, `LabelEncoder`, `KMeans`, `PCA` |

---

## 🧭 Methodology

### 1️⃣ Data Understanding
- Loaded the dataset using Pandas
- Displayed the first five records
- Identified numerical (`Age`, `Annual Income`, `Spending Score`) and categorical (`Gender`) features
- Reviewed dataset info and summary statistics

### 2️⃣ Data Preprocessing
- ✅ Checked for missing values (none found)
- 🗑️ Dropped `CustomerID` (no analytical value)
- 🔤 Label-encoded the `Gender` column
- ⚖️ Standardized numerical features using `StandardScaler`

### 3️⃣ Model Development
- 📐 Used the **Elbow Method** (WCSS vs. K, for K = 1–10) to find the optimal cluster count
- 🎯 Trained a **K-Means** model with the selected K
- 🏷️ Assigned cluster labels to each customer
- 🔻 Applied **PCA** to reduce features to 2 principal components

### 4️⃣ Visualization & Evaluation
- 📉 Elbow Curve
- 🟢 Scatter plot: Annual Income vs. Spending Score, colored by cluster
- 🧩 PCA 2D visualization with cluster labels
- 📋 Cluster-wise summary of average feature values

---

## 📈 Results

| Metric | Outcome |
|---|---|
| **Optimal Clusters (K)** | 5 |
| **Method Used** | Elbow Method (WCSS) |
| **Dimensionality Reduction** | PCA → 2 components |
| **Segments Identified** | High income/high spend, low income/low spend, and 3 intermediate profiles |

**Key findings:**
- 🟦 The Elbow Curve showed a clear bend at **K = 5**
- 🟩 Clusters were visually well-separated in both the raw feature space and the PCA projection
- 🟨 The two PCA components retained a substantial share of total variance, confirming the 2D visualization is a reliable representation of the clustering structure
- 🟥 Distinct customer personas emerged — useful for tailoring marketing strategy per segment

---

## ✅ Conclusion

This project applied **K-Means Clustering** to segment mall customers based on age, annual income, and spending score. Using the Elbow Method, **five clusters** were identified as optimal, each representing a distinct customer profile — ranging from high-income high-spenders to budget-conscious shoppers. **PCA** was used to reduce the standardized features to two dimensions, enabling clear visualization of how well-separated these segments are.

From a business standpoint, this segmentation enables the mall's management to design **targeted marketing campaigns** — e.g., premium loyalty programs for high-value customers and discount-driven promotions for price-sensitive segments — improving marketing ROI and customer retention.

**⚠️ Limitation of K-Means:** Requires the number of clusters to be specified in advance and assumes roughly spherical, equally-sized clusters, which may not always reflect real customer behavior.

**💡 Advantage of PCA:** Simplifies high-dimensional data into interpretable components while preserving most of the variance, making pattern visualization and communication much easier.

---

## 📁 Repository Structure

```
├── Assignment-7.ipynb   # Full notebook: preprocessing, clustering, PCA, visualizations
└── README.md            # Project documentation (this file)
```

---

## 📬 Submission Info

| Field | Detail |
|---|---|
| **Deadline** | 29 July 2026, 11:59 PM IST |
| **Platform** | Google Colab |
| **Repo Visibility** | Public (until evaluation completed) |
