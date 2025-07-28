# Customer Segmentation & Campaign Response Analysis

This project combines customer segmentation with predictive modeling to help marketers personalize campaigns and improve response rates. It explores unsupervised learning techniques for clustering, followed by supervised classification and visualizations to interpret customer behavior and campaign success.

---

## Problem Statement

Businesses often struggle to personalize marketing campaigns due to a lack of understanding of customer segments and response behavior. This project addresses two key problems:

1. **Segmentation**: Grouping customers based on demographics and behavior to enable tailored marketing.
2. **Campaign Targeting**: Predicting which customers are likely to respond to campaigns for efficient resource allocation.

---

## 📂 Dataset

- **Source**: A marketing campaign dataset from a Portuguese retail company
- **Format**: CSV (semicolon-separated)
- **Key Features**:
  - Demographics: Age, Education, Income, Marital Status, Children, Family Size
  - Customer behavior: Spending across product categories, Web/Catalog/Store Purchases, Tenure
  - Campaign response: Accepted or not (binary)
  - Other: Complaints, Number of promotions accepted, RFM Score

---

## Techniques & Models Used

- **Preprocessing**
  - Handling missing values (`Income`)
  - Feature engineering (e.g., `Family_Size`, `Is_Parent`)
  - Label Encoding, Feature Scaling

- **Unsupervised Learning**
  - PCA for dimensionality reduction
  - K-Means (via Elbow Method)
  - Agglomerative Hierarchical Clustering

- **Supervised Learning**
  - Logistic Regression
  - Random Forest Classifier with class balancing
  - Evaluation via Classification Report, Confusion Matrix, and ROC-AUC

- **Visualization**
  - Campaign Funnel Analysis
  - PCA scatter plots
  - Feature Importance chart
  - Correlation heatmap

---

## 📊 Visual Insights

### 1. Campaign Funnel
Only **15%** of customers accepted the campaign. This highlights the need for better targeting to reduce wasted effort on unlikely responders.

### 2. PCA Scatterplot
PCA shows poor separability between responders and non-responders. Most responding customers are clustered closely with non-responders, indicating limited feature power or subtle behavioral differences.

### 3. Feature Importance (Logistic Regression)
Top features influencing campaign response:
- `Children` and `Family_Size` (negative impact)
- `NumWebPurchases` and `NumCatalogPurchases` (positive impact)

This suggests family structure inversely correlates with response, while digital engagement is a strong positive indicator.

### 4. Correlation Heatmap (Top Features)
- `Income` and `Spent` show high correlation (r = 0.79)
- `Family_Size` and `Children` (r = 0.85)
- `Response` is moderately correlated with digital engagement features and RFM score.

---

## Classification Results

| Model                  | Accuracy | Precision (1) | Recall (1) | F1-score (1) | AUC   |
|------------------------|----------|----------------|-------------|--------------|-------|
| Logistic Regression    | 85%      | 0.67           | 0.22        | 0.33         | ~0.60 |
| Random Forest (Balanced)| 84%     | 0.61           | 0.20        | 0.30         | ~0.59 |

- Models predict non-responders well but struggle to capture the minority class (responders).
- Future improvements could involve SMOTE, cost-sensitive training, or deeper feature engineering.

---

## Customer Segmentation – 4 Clusters Identified

### Cluster 0
- Parents with teenagers
- Family size: 2–4
- Older demographic

### Cluster 1
- Non-parents
- Small households (1–2)
- High-income, varied ages

### Cluster 2
- Young parents with small families
- Likely to have young children

### Cluster 3
- Parents with large families (up to 5)
- Lower income group

---

## 💡 Business Recommendations

- **📣 Digital Channels Drive Response**: Invest more in online/catalog campaigns — top predictors of response.
- **👨‍👩‍👧 Segment by Family Structure**: Parents, especially those with larger families, show lower response. Use tailored messaging or exclude where ROI is low.
- **🎁 Personalize Offers by Cluster**: Luxury for Cluster 1, family bundles for Clusters 0 and 3, educational toys for Cluster 2.
- **📊 Use RFM and Purchase History**: Prioritize customers with higher RFM scores and web/catalog activity.
- **⚖️ Class Imbalance Needs Attention**: Improve predictive models through oversampling or weighting to better capture likely responders.

---

## Project Structure

customer_segmentation_marketing_campaign/
│
├── customer_segmentation_marketing_campaign.ipynb # Main notebook
├── marketing_campaign.csv # Dataset
├── README.md # Project overview
├── requirements.txt # Python dependencies
├── .gitignore # Ignore rules
└── LICENSE # MIT License


---

## Conclusion

This end-to-end marketing analytics project blends clustering, dimensionality reduction, supervised learning, and business insights. It not only segments customers for strategic planning but also identifies key drivers of campaign response, allowing marketers to optimize targeting and ROI.



