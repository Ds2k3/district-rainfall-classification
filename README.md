# District-wise Rainfall Classification Using Machine Learning

## Project Overview

This project uses machine learning to classify Indian districts into three rainfall categories: Low, Moderate, and High.

The classification is based on district-level monthly rainfall patterns and geographical information. The project includes data cleaning, exploratory data analysis, feature engineering, machine learning model development, hyperparameter tuning, and model evaluation.

The models used in this project are Decision Tree, Random Forest, and Support Vector Machine (SVM).

## Objective

The main objective of this project is to develop a machine learning classification system that categorizes districts based on their rainfall characteristics.

### Rainfall Categories

- Low Rainfall
- Moderate Rainfall
- High Rainfall

## Dataset

The dataset contains district-wise normal rainfall information for India.

### Dataset Details

- Records: 641
- States/UTs: 35
- Monthly rainfall attributes: January to December
- Annual rainfall: Available
- Geographical attributes: State and District
- Target: Rainfall Category

The original annual rainfall value was used to create the rainfall categories. Annual rainfall was excluded from the machine learning input features to avoid target leakage.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Google Colab
- GitHub

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded and inspected the dataset.
2. Checked for missing values.
3. Checked for duplicate records.
4. Converted rainfall columns to numeric format.
5. Verified annual rainfall calculations.
6. Renamed columns for easier analysis.
7. Created seasonal rainfall features.
8. Created rainfall variability features.
9. Created rainfall categories using annual rainfall distribution.
10. Split the dataset into training and testing sets.
11. Applied scaling to numerical features.
12. Applied one-hot encoding to the State feature.

## Feature Engineering

Additional features were created from the monthly rainfall data:

- Winter Rainfall
- Summer Rainfall
- Monsoon Rainfall
- Post-Monsoon Rainfall
- Maximum Monthly Rainfall
- Minimum Monthly Rainfall
- Rainfall Standard Deviation
- Monsoon Contribution

## Machine Learning Models

The following classification algorithms were implemented:

### 1. Decision Tree
Used as a tree-based classification model to identify rainfall category patterns.

### 2. Random Forest
An ensemble learning method combining multiple decision trees to improve classification performance.

### 3. Support Vector Machine (SVM)
Used to identify decision boundaries between the rainfall categories.

## Hyperparameter Tuning

GridSearchCV was used to systematically search for suitable hyperparameter combinations.

The tuning process used:

- Stratified 5-Fold Cross-Validation
- Weighted F1-score as the optimization metric
- Multiple hyperparameter combinations for each model

## Model Performance

|     Model     | Accuracy | Precision | Recall   | F1 Score |
| Decision Tree | 0.899225 | 0.904982  | 0.899225 | 0.900472 |
| Random Forest | 0.953488 | 0.954463  | 0.953488 | 0.953728 |
| SVM | XX.XX%  | 0.968992 | 0.969353  | 0.968992 | 0.969083 |

### Tuned Model Performance

|         Model       | Accuracy | Precision | Recall   | F1 Score |
| Tuned Decision Tree | 0.914729 | 0.916590  | 0.914729 | 0.915048 |
| Tuned Random Forest | 0.961240 | 0.961568	 | 0.961240 | 0.961318 |
| Tuned SVM           | 0.953488 | 0.954590  | 0.953488 | 0.952910 |

## Exploratory Data Analysis

### Annual Rainfall Distribution

![Annual Rainfall Distribution](visualizations/rainfall_distribution.png)

### Monthly Rainfall

![Monthly Rainfall](visualizations/monthly_rainfall.png)

### State-wise Rainfall

![State-wise Rainfall](visualizations/state_rainfall.png)

## Model Evaluation

### Model Comparison

![Model Comparison](visualizations/model_comparison.png)

### Confusion Matrix

![Confusion Matrix](visualizations/confusion_matrix.png)

## Project Workflow

Raw Rainfall Dataset
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Feature Engineering
        ↓
Rainfall Category Creation
        ↓
Train-Test Split
        ↓
Data Preprocessing
        ↓
Decision Tree / Random Forest / SVM
        ↓
Hyperparameter Tuning
        ↓
Model Evaluation
        ↓
Best Model Selection
        ↓
Rainfall Category Prediction

## Project Structure

district-rainfall-classification/
│
├── data/
│   └── district_rainfall_cleaned.csv
│
├── models/
│   └── rainfall_classifier.pkl
│
├── notebooks/
│   └── District_Wise_Rainfall_Classification.ipynb
│
├── visualizations/
│   ├── rainfall_distribution.png
│   ├── monthly_rainfall.png
│   ├── state_rainfall.png
│   ├── confusion_matrix.png
│   └── model_comparison.png
│
├── README.md
└── requirements.txt

## Future Improvements

- Develop a web-based rainfall prediction interface.
- Integrate real-time weather data.
- Explore advanced ensemble learning techniques.
- Compare classification with rainfall forecasting models.
- Develop an interactive Power BI dashboard.
- Deploy the trained model using Flask or Streamlit.

## Author

**Dheeran S**

B.E. Computer Science Engineering

Interested in Data Analytics, Machine Learning, and AI.

[GitHub](https://github.com/Ds2k3)

