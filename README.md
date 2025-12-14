# Airline Customer Experience Analysis & Satisfaction Prediction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L8WdPQs1E89qOJOIbg4bA0PoL2HMdoYf?usp=sharing)

## Quick Access
- [Open in Google Colab](https://colab.research.google.com/drive/1L8WdPQs1E89qOJOIbg4bA0PoL2HMdoYf?usp=sharing)

## Project Overview
This project analyzes airline customer experience data to predict customer satisfaction and identify distinct customer segments. The analysis is conducted using Python in a Jupyter Notebook, leveraging machine learning for both predictive modeling and customer segmentation.

## Dataset
- **Source**: OpenML (Dataset ID: 46920)
- **Size**: 129,880 rows × 22 columns
- **Target Variable**: `satisfaction` (binary)
- **Features**:
  - Customer attributes: `Age`, `CustomerType`, `TypeofTravel`, `Class`
  - Service ratings: `Inflightentertainment`, `Seatcomfort`, `Onboardservice`, etc.
  - Flight details: `FlightDistance`, `DepartureDelay`, `ArrivalDelay`

## Notebook Structure

### 1. Exploratory Data Analysis (EDA)
- Data structure and quality assessment
- Univariate and bivariate analysis
- Correlation analysis
- Missing value treatment
- Feature engineering

### 2. Predictive Modeling
- Binary classification of customer satisfaction
- Model training and evaluation:
  - Linear models (Logistic Regression)
  - Tree-based models (Random Forest, XGBoost)
  - Performance metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
- Feature importance analysis

### 3. Customer Segmentation
- Dimensionality reduction (PCA, t-SNE)
- Clustering techniques:
  - K-means
  - Hierarchical clustering
  - DBSCAN
- Cluster profiling and interpretation
- Business insights and recommendations

## Technical Requirements
- Python 3.8+
- Key Libraries:
  - pandas, numpy, matplotlib, seaborn
  - scikit-learn
  - xgboost
  - tqdm (for progress tracking)

## Performance Note
The notebook includes progress bars using `tqdm` to track execution progress, especially useful for longer-running operations.

## Key Insights
- Identification of critical service factors impacting satisfaction
- Customer segments with distinct service expectations
- Actionable recommendations for improving customer experience

## How to Use
1. Clone the repository
2. Install required packages: `pip install -r requirements.txt`
3. Open and run the Jupyter notebook
4. Follow the step-by-step analysis
