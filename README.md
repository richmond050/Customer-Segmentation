# Customer Segmentation Using K-Means Clustering

This project applies **Unsupervised Machine Learning (Clustering)** to group retail customers based on demographic and behavioral data. The goal is to help the marketing and business teams personalize campaigns, improve targeting strategies, and understand key customer personas.

---

## 📂 Dataset

**Source:** [Kaggle - Customer Personality Analysis](https://www.kaggle.com/datasets/vishakhdapat/customer-segmentation-clustering/data)

The dataset contains information on:
- Demographics (age, education, marital status, etc.)
- Spending on product categories
- Response to marketing campaigns
- Number of purchases through different channels

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Scikit-learn** for clustering & preprocessing
- **Jupyter Notebook** for exploration

---

## 📊 Project Workflow

### 1. 📥 Data Loading
- Loaded the dataset from CSV
- Checked data types, nulls, and dataset dimensions

### 2. 🧹 Data Cleaning
- Dropped irrelevant columns like `ID` and constant features
- Parsed `Dt_Customer` to datetime
- Removed outliers and unrealistic values (e.g., birth year before 1900)
- Filled or removed missing values appropriately

### 3. 📈 Exploratory Data Analysis (EDA)
- Categorical Distribution:
  - Visualized counts of `Education`, `Marital_Status`, and campaign responses
- Numerical Distribution:
  - Used histograms to inspect distribution shapes
  - Box plots to detect outliers
- Correlation Analysis:
  - Heatmap to explore relationships among variables

### 4. 🧽 Feature Engineering & Data Preprocessing
- Created new features like `Customer_Tenure`
- Removed `Response` column since clustering is unsupervised
- Label encoded categorical features (`Education`, `Marital_Status`)
- Scaled all numeric features using `StandardScaler`
- Final clean, encoded, and scaled dataset was stored in `encoded_data`

---

## 🤖 Clustering

### 5. 📍 Elbow Method
- Ran KMeans clustering for K=1 to K=10
- Plotted inertia vs. number of clusters
- **Elbow observed at K=4 and K=5**, both tested

### 6. 🚨 Model Training
- Fit KMeans for K=4 and K=5
- Added `Cluster_4` and `Cluster_5` labels to the dataset

### 7. 📐 Cluster Analysis
- Grouped data by `Cluster_4` and `Cluster_5`
- Computed summary statistics (means) for each cluster
- Interpreted patterns in income, product spending, engagement, and demographics

---

## 👥 Customer Segments (K=4)

| Cluster | Description                           |
|---------|---------------------------------------|
| 0       | Budget-Conscious Families             |
| 1       | Moderate Income, Active Shoppers      |
| 2       | Affluent and Highly Engaged Customers |
| 3       | Low Income, Low Engagement            |

> Each profile includes unique traits in income, product spending, campaign response, and digital activity.

---

## 📌 Final Decision

After comparing both clusterings, **K=4** was selected for clarity, interpretability, and actionable marketing insights.

---


