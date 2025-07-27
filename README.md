# 🧠 Customer Segmentation for Marketing Campaigns

This project explores unsupervised learning techniques to segment customers based on their behavior and demographics. The goal is to help businesses target specific customer groups with tailored marketing strategies, ultimately improving ROI and engagement.

---

## 🎯 Problem Statement

Businesses often struggle to personalize marketing campaigns due to a lack of understanding of customer segments. By analyzing customer data from a marketing campaign, this project aims to uncover distinct customer groups using clustering techniques, helping marketing teams make data-driven decisions.

---

## 📂 Dataset

- **Source**: A marketing campaign dataset
- **Format**: CSV (semicolon-separated)
- **Columns** include:
  - Demographics: Age, Education, Income, Marital Status
  - Spending behavior: Amount spent on various product categories
  - Campaign response: Acceptance of offers
  - Other: Tenure, Kids, Recency, etc.

---

## ⚙️ Algorithms and Models Used

- Data Preprocessing:
  - Handling missing values
  - Feature engineering (e.g., customer tenure)
  - Label Encoding, Scaling

- Dimensionality Reduction:
  - PCA (Principal Component Analysis)

- Clustering Techniques:
  - K-Means (with Elbow Method)
  - Agglomerative Hierarchical Clustering

---

## 📁 Project Structure
customer_segmentation_marketing_campaign/
│
├── customer_segmentation_marketing_campaign.ipynb # Jupyter Notebook
├── marketing_campaign.csv # Dataset (assumed, not included here)
├── README.md # Project Overview
├── requirements.txt # Dependencies
├── .gitignore # Files to ignore in Git
└── LICENSE # MIT License


---

## 🔍 Key Insights

After performing dimensionality reduction and clustering, customers were grouped into 4 clusters with distinct characteristics:

### Cluster 0
- Definitely parents
- Family size ranges from 2 to 4
- Many are single parents
- Most have teenagers at home
- Relatively older in age

### Cluster 1
- Definitely not parents
- Small households (1–2 members)
- Slight majority are couples
- High-income group
- Span a wide range of ages

### Cluster 2
- Majority are younger parents
- Family size mostly 3
- Often have young children (not teens)
- Relatively younger age group

### Cluster 3
- All are parents
- Family size ranges from 2 to 5
- Most have teenagers
- Relatively older
- Represent a lower-income group

---

## 📊 Evaluation Metrics

- Since it's an unsupervised problem:
  - **Silhouette Score** was used for evaluating cluster quality
  - **Elbow Method** guided the optimal number of clusters
  - PCA plots used for visual interpretation of cluster separation

---

## ✅ Conclusion

In this project, unsupervised clustering (using PCA followed by Agglomerative Clustering) revealed 4 customer segments based on demographics, family structure, and spending behavior. These segments can help marketing teams personalize campaigns, allocate resources more efficiently, and optimize customer targeting strategies.


