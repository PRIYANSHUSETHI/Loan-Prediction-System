# Loan Prediction System

## Overview
The **Loan Prediction System** is a machine learning project that helps predict whether a loan will be approved or not based on applicant details. The project uses various machine learning classifiers to analyze historical loan application data and make predictions.

## Features
- Reads and processes loan applicant data from an Excel file.
- Handles missing values through imputation techniques.
- Performs feature engineering (log transformation, income calculation).
- Visualizes applicant data using Seaborn and Matplotlib.
- Trains multiple machine learning classifiers to predict loan approval.
- Compares model performance based on accuracy.

## Dataset
The dataset contains various features related to loan applicants, such as:
- **Applicant Income**
- **Co-applicant Income**
- **Loan Amount**
- **Credit History**
- **Marital Status**
- **Employment Status**
- **Number of Dependents**
- **Loan Amount Term**

## Data Preprocessing
- **Handling Missing Values**: Categorical values are filled using the most frequent value (mode), while numerical values are filled using the mean.
- **Feature Engineering**:
  - `totalincome` = `ApplicantIncome` + `CoapplicantIncome`
  - Log transformation applied to `LoanAmount` and `totalincome` to normalize skewed distributions.
- **Encoding Categorical Features**: Using `LabelEncoder` to convert categorical variables into numerical format.
- **Standardization**: Feature values are normalized using `StandardScaler`.

## Machine Learning Models Used
The following classifiers were trained and evaluated:
1. **Random Forest Classifier**
2. **Naive Bayes (GaussianNB)**
3. **Decision Tree Classifier**
4. **K-Nearest Neighbors (KNN) Classifier**

## Model Evaluation
The models were trained on an 80-20 train-test split. The **accuracy score** was used to evaluate the performance of each classifier.

## Dependencies
Ensure you have the following Python libraries installed:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/loan-prediction-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd loan-prediction-system
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the script:
   ```bash
   python loan_prediction_system.py
   ```

## Results
After training, the script prints the accuracy of each model, helping determine the best classifier for loan prediction.

## Future Enhancements
- Improve feature selection using advanced techniques.
- Implement hyperparameter tuning for better model accuracy.
- Deploy the model using a web interface.
