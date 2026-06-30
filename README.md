# 📊 EY-GDS Edunet Customer Segmentation Project

[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-notebook-orange)](https://jupyter.org/)
[![Dependencies](https://img.shields.io/badge/dependencies-%E2%89%A4-9-brightgreen)](requirements.txt)
[![Data Rows](https://img.shields.io/badge/data-541909%20rows-lightgrey)](#dataset)

## ✨ Overview

This project performs customer segmentation and behavioral profiling using the `EY_GDS_Edunet_P8_final.ipynb` notebook.
The notebook ingests transactional customer data, performs data cleaning and feature engineering, builds RFM-style and behavioral customer features, and applies K-Means clustering.
It also evaluates clustering quality, visualizes the resulting segments, and extracts actionable customer insights.

## 🎯 Key Objectives

- 🧼 Clean and preprocess transactional customer data
- ⚙️ Engineer customer-level features including RFM, product diversity, seasonality, and cancellation behavior
- 🚨 Detect and treat outliers and anomalies
- 📏 Scale features and reduce dimensionality via PCA
- 🔍 Determine the optimal number of clusters using elbow and silhouette methods
- 🧩 Segment customers using K-Means clustering
- ✅ Evaluate cluster quality with silhouette, Calinski-Harabasz, and Davies-Bouldin metrics
- 📊 Profile clusters and surface recommendations

## 🧠 Core Concepts Covered

- 🧼 Data cleaning
  - missing values handling
  - duplicate removal
  - cancelled transaction treatment
  - stock code anomalies
  - description normalization
  - zero price handling
- ⚙️ Feature engineering
  - Recency, Frequency, Monetary (RFM)
  - product diversity and category counts
  - behavioral features such as purchase day/hour and inter-purchase interval
  - geographic segmentation and country-level behavior
  - cancellation insights and transaction status
  - seasonality and spending trend extraction
- 🚨 Outlier detection
  - anomaly detection using Isolation Forest
  - removal of outlier customers and transactions
- 📏 Scaling and transformation
  - StandardScaler for numeric feature scaling
  - PCA for dimensionality reduction and cluster visualization
- 🤖 Unsupervised machine learning
  - K-Means clustering
  - cluster validation via elbow and silhouette analysis
- 📈 Visualization
  - scatter plots, bar plots, histograms
  - 3D cluster visualization with Plotly
  - cluster distribution and feature-level profiling

## 🧭 Notebook Structure

The main notebook is organized into the following stages:

1. **Setup and Initialization**
   - import libraries
   - load customer transaction dataset
2. **Initial Data Analysis**
   - dataset overview and descriptive statistics
3. **Data Cleaning and Transformation**
   - handle missing values, duplicates, cancellations, stock code issues, and invalid descriptions
4. **Feature Engineering**
   - build RFM and advanced customer-level features
   - compute product diversity, purchase behavior, and geographic features
5. **Outlier Detection and Treatment**
   - use Isolation Forest and business rules to remove extreme customers
6. **Correlation Analysis**
   - identify relationships in customer features before modeling
7. **Feature Scaling**
   - standardize numeric features for clustering
8. **Dimensionality Reduction**
   - apply PCA to support cluster visualization and noise reduction
9. **K-Means Clustering**
   - determine optimal cluster count using elbow and silhouette methods
   - fit the final K-Means clustering model
10. **Clustering Evaluation**
    - compute silhouette score, Calinski-Harabasz score, and Davies-Bouldin score
    - visualize cluster distributions and PCA component clusters
11. **Cluster Profiling and Recommendations**
    - analyze segment characteristics
    - generate customer cluster recommendations based on purchase and cancellation patterns

## 📦 Dataset

The project uses the provided dataset `customer_data_internship.csv`.

### Dataset Summary

- Rows: `541909`
- Columns:
  - `InvoiceNo`
  - `StockCode`
  - `Description`
  - `Quantity`
  - `InvoiceDate`
  - `UnitPrice`
  - `CustomerID`
  - `Country`

## 🧩 Dependencies

Install project dependencies from `requirements.txt`.

```bash
python -m venv venv
venv\Scripts\activate
python -m pip install -r requirements.txt
```

### Main Python libraries

- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `plotly`
- `scipy`
- `scikit-learn`
- `yellowbrick`
- `tabulate`

## 🚀 How to Run

1. Activate the virtual environment:

```bash
python -m venv venv
venv\Scripts\activate
```

2. Install dependencies:

```bash
python -m pip install -r requirements.txt
```

3. Open the main notebook:

```bash
jupyter notebook EY_GDS_Edunet_P8_final.ipynb
```

4. Run all cells sequentially from top to bottom.

## 📁 Files in this Repository

- `EY_GDS_Edunet_P8_final.ipynb` — main production notebook with full customer segmentation workflow
- `customer_data_internship.csv` — customer transaction dataset
- `customer_clusters_3d.html` — exported cluster visualization output
- `Output Shots/` — visual output artifacts and screenshots from the analysis
- `requirements.txt` — Python dependency list

## 🖼️ Output Artifacts

The `Output Shots` folder contains screenshots and visual artifacts showing the notebook execution, cluster visualizations, and key result panels.

These artifacts include:

- customer segment visualization screenshots
- cluster evaluation plots
- notebook run output captures

## 📈 Results and Insights

The main notebook builds customer segments that can be used for:

- identifying high-value repeat customers
- detecting customers with unstable or cancelling behavior
- understanding customer lifecycle through RFM analysis
- mapping purchase behavior by geography, frequency, and seasonality
- generating targeted recommendations per cluster

## 📝 Notes and Best Practices

- The notebook uses a relative dataset path, so keep `customer_data_internship.csv` in the same folder.
- For reproducible results, use the same random seed for K-Means clustering.
- The advanced feature engineering stage makes the final segmentation more robust than a simple RFM-only model.
- `EY_GDS_Edunet_P8_final.ipynb` is the primary deliverable and covers the complete analysis process.

## 🚀 Future Enhancements

Possible next steps:

- add time-series forecasting for customer spend
- apply hierarchical or density-based clustering methods
- incorporate text analysis on `Description`
- use customer lifetime value models
- export cluster assignments for downstream CRM or marketing use

## 📜 License

Add a license file if you want to make this project reusable by others.
