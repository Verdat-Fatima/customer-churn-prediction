# Customer Churn Prediction

## Project Overview

Customer churn prediction is a machine learning classification project that aims to identify customers who are likely to leave a service. Understanding customer churn can help businesses identify patterns in customer behavior and make informed decisions to improve customer retention.

In this project, I performed exploratory data analysis (EDA), prepared the dataset for machine learning, and trained and evaluated five classification models to predict customer churn.

## Objectives

- Explore customer data and identify patterns related to churn.
- Perform data cleaning and preprocessing.
- Analyze customer characteristics and service charges.
- Train multiple machine learning classification models.
- Compare model performance using accuracy scores.

## Dataset

The project uses `customer_churn_data.csv`, which contains customer information and a target variable indicating whether a customer has churned.

The features selected for model training are:

| Feature | Description |
|---|---|
| `Age` | Customer's age |
| `Gender` | Customer's gender |
| `Tenure` | Length of time the customer has used the service |
| `MonthlyCharges` | Customer's monthly service charges |
| `Churn` | Target variable indicating whether the customer churned |

**Note:** The dataset file is not included in this repository unless uploaded separately.

## Technologies and Libraries

- **Python** — Programming language
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Scikit-learn** — Data preprocessing, model training, and evaluation
- **Google Colab** — Cloud-based notebook environment

## Project Workflow

### 1. Data Loading and Inspection
- Loaded the dataset using Pandas.
- Inspected the dataset's structure, dimensions, and data types.
- Checked for missing values and duplicate records.
- Examined descriptive statistics and correlations among numerical features.

### 2. Exploratory Data Analysis (EDA)
- Analyzed the distribution of churn.
- Compared average monthly charges between churn groups.
- Examined monthly charges by gender and churn status.
- Compared average customer tenure and age across churn groups.
- Analyzed monthly charges by contract type.
- Visualized the distributions of monthly charges and tenure.

### 3. Data Preprocessing
- Handled missing values in the `InternetService` column.
- Selected `Age`, `Gender`, `Tenure`, and `MonthlyCharges` as input features.
- Applied one-hot encoding to the `Gender` feature.
- Converted the target variable, `Churn`, into binary labels:
  - `Yes` → `1`
  - `No` → `0`
- Split the dataset into training and testing sets using an 80:20 ratio.
- Used stratified sampling to preserve the target class distribution.
- Standardized the features using `StandardScaler`.

### 4. Model Training

Five classification algorithms were implemented:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Support Vector Classifier (SVC)
4. Decision Tree Classifier
5. Random Forest Classifier

For KNN, SVC, Decision Tree, and Random Forest, `GridSearchCV` was used to search for suitable hyperparameter combinations with five-fold cross-validation.

### 5. Model Evaluation

The models were evaluated using **accuracy score** on the held-out test set. The evaluation allows their predictive performance to be compared on the same test data.

## How to Run the Project

### Prerequisites

Make sure Python is installed on your system.

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/customer-churn-prediction.git
```

### 2. Navigate to the project directory

```bash
cd customer-churn-prediction
```

### 3. Install the required libraries

```bash
pip install pandas matplotlib scikit-learn jupyter
```

### 4. Add the dataset

Place `customer_churn_data.csv` in the project directory, alongside the notebook.

### 5. Run the notebook

Open the notebook in Jupyter Notebook or VS Code and execute the cells in order.

## Key Learnings

Through this project, I gained practical experience with:

- Exploratory data analysis and data visualization.
- Handling missing values and categorical features.
- Train-test splitting and feature scaling.
- Implementing classification algorithms using Scikit-learn.
- Hyperparameter tuning with `GridSearchCV`.
- Evaluating machine learning models on unseen test data.

## Future Improvements

- Compare models using precision, recall, F1-score, and confusion matrices.
- Investigate class imbalance and evaluate how well the models identify customers who do not churn.
- Improve preprocessing by using Scikit-learn pipelines.
- Explore additional relevant features and assess their effect on model performance.

## Author

**Verdat Fatima**

- GitHub: [Verdat-Fatima](https://github.com/Verdat-Fatima)

---

