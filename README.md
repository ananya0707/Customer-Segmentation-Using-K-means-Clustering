# Customer Segmentation using Unsupervised Machine Learning

## 📌 Project Overview
This project applies **unsupervised learning (KMeans clustering)** to segment customers based on demographic, behavioral, and marketing response data. The goal is to identify distinct customer groups and derive actionable business insights for targeted marketing strategies.

## 📂 Dataset
- Source: `customer_segmentation_data.csv`
- Shape: 2,240 rows × 29 columns
- Key features:
  - Demographics: `Year_Birth`, `Education`, `Marital_Status`, `Income`
  - Household: `Kidhome`, `Teenhome`
  - Purchase behavior: `MntWines`, `MntFruits`, `MntMeatProducts`, etc.
  - Campaign responses: `AcceptedCmp1–5`, `Response`
  - Other: `Recency`, `NumWebPurchases`, `NumStorePurchases`

## ⚙️ Steps Performed
1. **Import Libraries**  
   - `numpy`, `pandas`, `matplotlib`, `seaborn`, `sklearn`

2. **Data Preprocessing**  
   - Dropped null values in `Income` (24 rows removed)  
   - Extracted `day`, `month`, `year` from `Dt_Customer`  
   - Dropped irrelevant columns: `Z_CostContact`, `Z_Revenue`, `Dt_Customer`  
   - Label encoded categorical variables (`Education`, `Marital_Status`)  
   - Standardized numerical features using `StandardScaler`

3. **Exploratory Data Analysis (EDA)**  
   - Count plots for categorical features  
   - Campaign acceptance visualization  
   - Correlation heatmap (no strong correlations found)

4. **Dimensionality Reduction**  
   - Applied **t-SNE** for 2D visualization of high-dimensional data

5. **Clustering**  
   - Used **KMeans clustering**  
   - Optimal number of clusters determined via **Elbow Method**  
   - Final model trained with **4 clusters**

## 📊 Cluster Profiles
| Cluster | Profile Summary |
|---------|-----------------|
| **0** | Lower-income families with kids, low spending, low campaign response |
| **1** | Mid-income, more teens at home, moderate spending, moderate campaign response |
| **2** | Wealthy, child-free, very high spending (especially on wine), extremely responsive to campaigns |
| **3** | Upper-mid income, child-free, moderate-to-high spending, some campaign responsiveness |

## 🎯 Business Insights
- **Cluster 0** → Target with budget-friendly offers  
- **Cluster 1** → Family/teen-oriented promotions  
- **Cluster 2** → Premium, loyal, high-value customers; ideal for luxury campaigns  
- **Cluster 3** → Convertible into Cluster 2 with the right incentives  

## 🛠️ Technologies Used
- Python 3.x  
- Libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `sklearn`  

## 📈 Visualization
- t-SNE scatter plot for cluster visualization  
- Elbow method plot for optimal cluster selection  
- Campaign acceptance bar chart  

## ✅ Conclusion
This segmentation provides actionable insights for **personalized marketing strategies**. By tailoring offers to each cluster, businesses can improve customer engagement, loyalty, and revenue.
