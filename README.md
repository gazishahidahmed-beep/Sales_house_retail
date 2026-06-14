# Retail_Sales_Data_Analysis

Welcome to the **Retail Sales Data Analysis** project repository. This project was developed as part of the **IDEAS (Institute of Data Engineering, Analytics and Science Foundation) Summer Internship Program 2026**. 

The primary objective of this project is to perform comprehensive exploratory data analysis (EDA), extract meaningful time-series revenue metrics, and apply machine learning clustering algorithms to discover underlying patterns in complex data structures.

## 👤 Author Details
- **Developer:** Samyabrata Roy
- **Designation:** Associate Software Developer
- **Program:** Summer Internship Program 2026
- **Organization:** IDEAS Foundation

---

## 🚀 Project Overview

This repository features an end-to-end data pipeline built inside a Jupyter Notebook that tackles data preprocessing, chronological sales aggregations, advanced data pivoting, and unsupervised learning evaluations. 

### Key Highlights & Technical Tasks:
1. **Data Preprocessing & Cleaning:** Handling custom datetime formatting (including Excel date serializations) and structural anomaly detection.
2. **Time-Series Revenue Analysis:** Calculating total monthly, weekly, and cumulative revenue benchmarks to evaluate overall business growth.
3. **Customer & Product Intelligence:** Grouping sales metrics to pinpoint top-spending customers, determine Average Order Value (AOV), and establish best-selling product categories.
4. **Unsupervised Machine Learning:** Implementing **K-Means Clustering** on dimensional features (using the MNIST handwritten digit benchmark) to categorize data distributions.
5. **Advanced Model Evaluation:** Mapping arbitrary cluster labels to true categorical modes and assessing performance using **Macro-Averaged F1-Scores**.

---

## 🛠️ Tech Stack & Libraries Used

The core analysis is performed using Python and standard scientific computing libraries:
* **Data Manipulation:** `pandas`, `numpy`
* **Mathematical Operations:** `scipy` (Statistical Modes)
* **Machine Learning:** `scikit-learn` (KMeans, load_digits)
* **Model Assessment:** `sklearn.metrics` (f1_score)

---

## 📁 Repository Structure

```text
├── Retail_Sales_Data_Analysis_Summer_2026.ipynb   # Main Project Notebook with solutions
├── README.md                                      # Project documentation (This file)
└── retail_sales_dataset.csv                       # Project Source Dataset (External link provided)

Summary of Key Implementations
1. Chronological Aggregations
The project isolates time-stamped transactions into discrete periods (W-SUN for weekly, M for monthly) using Pandas grouping techniques to observe real-time business momentum and patterns:
# Monthly and Weekly aggregations example
df['Month'] = df['Date'].dt.to_period('M')
monthly_revenue = df.groupby('Month')['Price'].sum()

K-Means Clustering Configuration
A K-Means algorithm is deployed to segment features into 10 target boundaries representing structured mathematical clusters:
from sklearn.cluster import KMeans
kmeans = KMeans(n_clusters=10, random_state=42)
kmeans_labels = kmeans.fit_predict(X)

from sklearn.cluster import KMeans
kmeans = KMeans(n_clusters=10, random_state=42)
kmeans_labels = kmeans.fit_predict(X)

Clone the Repository-
git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
cd YOUR_REPOSITORY_NAME

Set Up Your Environment
Ensure you have Python 3.8+ installed along with the required dependencies:
pip install pandas numpy scipy scikit-learn notebook

Run the Notebook
Launch Jupyter Notebook or JupyterLab to execute the pipeline cells sequentially:
jupyter notebook Retail_Sales_Data_Analysis_Summer_2026.ipynb


