# Machine Learning Projects: Home Price Prediction and Spam Detection

This repository contains two beginner-to-intermediate level machine learning projects implemented in Python. Both projects demonstrate core machine learning concepts step by step with reproducible code.

---

## Project 1: Linear Regression (Mini Home Prices)

### Overview
A simple linear regression model is built from scratch using gradient descent and compared with scikit-learn.  
The dataset (`minihomeprices.csv`) contains housing features such as area, bedrooms, and age, with the target variable `price`.

### Steps
- Load and explore the dataset
- Normalize features for stability
- Implement gradient descent manually
- Track and plot cost convergence
- Visualize the regression line
- Compare predictions with scikit-learn implementation

### Results
- Final parameters (`theta0`, `theta1`) learned through gradient descent  
- Cost function decreases smoothly across iterations  
- Predicted price for a new house size (e.g., 1800 sqft)  

**Example Output:**
Final Parameters:
theta0 (intercept): 648305.34
theta1 (slope): 89792.51
Final Cost: 929416181.92
### Predicted Price for 1800 sqft (scratch model): 377833.25 
Accuracy: 0.9883
Precision: 0.9928
Recall: 0.9195
F1-score: 0.9547
ROC AUC: 0.9957


Confusion matrix and ROC curve visualizations are included.  

Top indicators for spam: digits, "ringtone", "mobile", "sms", "reply"  
Top indicators for ham: "gt", "got", "say", "hey", "sorry"

### Model Saving
The trained model and preprocessing steps are saved with joblib:
- `spam_logreg_model.joblib`
- `vectorizer.joblib`
- `scaler.joblib`
- `hand_columns.joblib`

---

## How to Run

1. Clone the repository:
   
   git clone https://github.com/UrwahRasheed80/Buildables_tasks/Week_03/Urwah
   cd Week_03/Urwah



---

## Project 2: Spam Detection with Logistic Regression

### Overview
A text classification model that detects spam SMS messages using Logistic Regression with both Bag-of-Words features and handcrafted features.

Dataset: [UCI SMS Spam Collection](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection) (provided as `spam.csv`).

### Preprocessing
- Cleaned text (lowercasing, removing punctuation, replacing URLs and digits)
- Extracted Bag-of-Words features with `CountVectorizer`
- Added handcrafted features:
  - Message length
  - Number of words, digits, exclamation marks
  - Presence of URL, "free", uppercase words

### Training
- Split dataset into train/test (80/20)
- Trained Logistic Regression with `liblinear` solver
- Evaluated with Accuracy, Precision, Recall, F1-score, and ROC AUC

### Results
Accuracy: 0.9883
Precision: 0.9928
Recall: 0.9195
F1-score: 0.9547
ROC AUC: 0.9957


Confusion matrix and ROC curve visualizations are included.  

Top indicators for spam: digits, "ringtone", "mobile", "sms", "reply"  
Top indicators for ham: "gt", "got", "say", "hey", "sorry"

### Model Saving
The trained model and preprocessing steps are saved with joblib:
- `spam_logreg_model.joblib`
- `vectorizer.joblib`
- `scaler.joblib`
- `hand_columns.joblib`

---

## How to Run

1. Clone the repository:
   
  git clone https://github.com/UrwahRasheed80/Buildables_tasks/Week_03/Urwah
   cd Week_03/Urwah




