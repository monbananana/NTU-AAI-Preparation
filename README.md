# NTU-AAI-Preparation
I'm a student from SCU, and I'm going to NTU for my master's degree. This README is to document my preparation for the AAI program.


## Day 1: Supply Chain Analysis - Exploratory Data Analysis (EDA)

**Dataset**: [Supply Chain Analysis Dataset](https://www.kaggle.com/datasets/aminasalamt/supply-chain-analysis-dataset)  
(Fashion & Beauty startup makeup products supply chain data)

### Work Completed:
- Loaded and inspected the dataset (shape, data types, summary statistics)
- **Data Cleaning**:
  - Checked and handled missing values
  - Removed/handled duplicates if any
  - Corrected data types where necessary
- **Exploratory Data Analysis & Visualization**:
  - Distribution analysis: Histplots for key numerical variables (Price, Revenue Generated, Stock Levels, etc.)
  - Outlier detection: Boxplots for Price, Order Quantities, Lead Time
  - Correlation analysis: Heatmap to identify relationships between variables (e.g., Price vs Revenue, Stock Levels vs Sales)
  - Categorical analysis: Countplots for Product Type, Customer Demographics, Shipping Carriers
- Initial business insights extracted (e.g., most popular product types, revenue distribution)

**Tools**: Python, Pandas, NumPy, Matplotlib, Seaborn

**Next Step (Day 2)**: Build predictive models (e.g., predict Revenue Generated or Number of Products Sold) using Scikit-Learn.


## Day 2: Baseline Prediction Models for Revenue Generated

**Dataset**: [Supply Chain Analysis Dataset](https://www.kaggle.com/datasets/aminasalamt/supply-chain-analysis-dataset)  
(Fashion & Beauty startup makeup products supply chain data)

### Work Completed:
- Defined target variable: `Revenue Generated`
- Feature selection: Numerical features + Categorical features
- Built preprocessing pipeline using `ColumnTransformer` (StandardScaler + OneHotEncoder)
- Trained two baseline models:
  - Linear Regression
  - Random Forest Regressor (n_estimators=200, max_depth=10)
- Performed train-test split (80/20) and model evaluation

### Model Results:
- Both Linear Regression and Random Forest produced **negative R² scores**
- Model performance was worse than simply predicting the mean value

**Tools**: Python, Pandas, Scikit-Learn, Matplotlib, Seaborn

### Problem Analysis:
- Dataset has limited number of samples
- High feature dimensionality after One-Hot Encoding
- Strong non-linear relationships between features and target variable
- Curse of dimensionality issue

**Model Plan (Next Step)**: Build baseline classification models (Logistic Regression, Random Forest, XGBoost) and evaluate using Accuracy, Precision, Recall, F1-score, ROC-AUC.


## Day 3 & Day 4: Customer Churn Prediction - Full ML Pipeline

**Dataset**: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
(Telecom company customer churn data)

### Work Completed:
- Loaded and inspected the dataset (shape, data types, summary statistics)
- **Data Cleaning**:
  - Handled missing values in `TotalCharges`
  - Converted data types and removed unnecessary columns (`customerID`)
- **Exploratory Data Analysis & Visualization**:
  - Distribution analysis: Histplots and Boxplots for numerical features (tenure, MonthlyCharges, TotalCharges)
  - Categorical analysis: Countplots showing churn rate by Contract, InternetService, PaymentMethod, etc.
  - Analyzed overall churn rate and relationships between features and target variable
- **Feature Engineering**:
  - Created new features (e.g., Tenure groups)
  - Applied One-Hot Encoding for categorical variables
  - Standardized numerical features
- **Modeling & Evaluation**:
  - Built preprocessing Pipeline using ColumnTransformer
  - Trained baseline models: Logistic Regression and Random Forest Classifier
  - Evaluated models using Accuracy, Precision, Recall, F1-score, and ROC-AUC
- **Feature Importance**:
  - Analyzed and visualized feature importance using Random Forest

**Tools**: Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn




