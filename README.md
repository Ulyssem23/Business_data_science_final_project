# Airline Customer Experience Analysis & Satisfaction Prediction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L8WdPQs1E89qOJOIbg4bA0PoL2HMdoYf?usp=sharing)

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Profiling](#data-profiling)
- [Notebook Structure](#notebook-structure)
- [Technical Requirements](#technical-requirements)
- [Key Insights](#key-insights)
- [How to Use](#how-to-use)

## Project Overview
This project provides a comprehensive analysis of airline customer experience data, focusing on predicting customer satisfaction and identifying distinct customer segments. The analysis is conducted using Python in a Jupyter Notebook, leveraging advanced machine learning techniques for both predictive modeling and customer segmentation.

## Dataset
- **Source**: [OpenML (Dataset ID: 46920)](https://www.openml.org/search?type=data&status=active&id=46920)
- **Size**: 129,880 rows × 22 columns
- **Target Variable**: `satisfaction` (binary: 0 = dissatisfied, 1 = satisfied)

### Key Features
- **Customer Attributes**:
  - `Age`, `CustomerType`, `TypeofTravel`, `Class`
  - `FlightDistance`, `DepartureDelay`, `ArrivalDelay`
- **Service Ratings (1-5 scale)**:
  - `SeatComfort`, `FoodAndDrink`, `InflightEntertainment`
  - `OnboardService`, `LegRoomService`, `BaggageHandling`
  - `CheckinService`, `InflightService`, `Cleanliness`
  - `OnlineBoarding`, `GateLocation`, `InflightWifi`

## Data Profiling
An automated data profiling report has been generated using `ydata-profiling`, providing comprehensive insights into:

### 1. Dataset Overview
- Basic statistics (missing values, duplicates, memory usage)
- Variable types and distributions
- Correlation analysis between variables

### 2. Key Findings
- **Data Quality**: Identification of missing values and potential data entry errors
- **Variable Distributions**: Analysis of numerical and categorical variable distributions
- **Correlations**: Heatmaps showing relationships between variables
- **Interactions**: Scatter plots for numerical variable pairs
- **Sample Records**: First and last rows of the dataset

### 3. Usage
```python
# To regenerate the profiling report:
from ydata_profiling import ProfileReport
profile = ProfileReport(df, title="Airline Customer Satisfaction Profiling Report")
profile.to_file("data_profile_report.html")
```

## Notebook Structure

### 1. Exploratory Data Analysis (EDA)
- Data loading and initial inspection
- Statistical summaries and visualizations
- Handling missing values and outliers
- Feature engineering and transformation

### 2. Predictive Modeling
- Data preprocessing and feature selection
- Model training with cross-validation:
  - Logistic Regression (baseline)
  - Random Forest Classifier
  - XGBoost Classifier
- Model evaluation using multiple metrics:
  - Accuracy, Precision, Recall, F1-score
  - ROC-AUC curves and confusion matrices
- Feature importance analysis

### 3. Customer Segmentation
- Dimensionality reduction techniques:
  - Principal Component Analysis (PCA)
  - t-Distributed Stochastic Neighbor Embedding (t-SNE)
- Clustering algorithms:
  - K-means
  - Hierarchical clustering
  - DBSCAN (Density-Based Spatial Clustering)
- Cluster interpretation and profiling
- Business recommendations based on segments

## Technical Requirements
- **Python**: 3.8+
- **Key Libraries**:
  - Core: `pandas`, `numpy`, `scipy`
  - Visualization: `matplotlib`, `seaborn`
  - Machine Learning: `scikit-learn`, `xgboost`
  - Data Profiling: `ydata-profiling`
  - Progress Tracking: `tqdm`

Install all dependencies using:
```bash
pip install -r requirements.txt
```

## Key Insights
1. **Critical Service Factors**:
   - In-flight entertainment and seat comfort are primary drivers of satisfaction
   - Onboard service quality significantly impacts overall experience

2. **Customer Segments**:
   - Business travelers vs. leisure travelers show distinct preferences
   - High-value customer segments identified for targeted improvements

3. **Operational Impact**:
   - Flight delays have less impact on satisfaction compared to service quality
   - Digital services (online boarding, check-in) are key satisfaction drivers

## How to Use
1. **Setup Environment**:
   ```bash
   git clone [repository-url]
   cd [repository-name]
   pip install -r requirements.txt
   ```

2. **Run the Analysis**:
   - Open `data_business_project_version_final.ipynb` in Jupyter Notebook/Lab
   - Execute cells sequentially or use the provided Colab link

3. **Explore Results**:
   - View all visualizations and model outputs in the notebook
   - Check the report
