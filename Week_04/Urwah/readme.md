# Wine Classification with Machine Learning
## Project Overview
This project implements and compares three different machine learning algorithms to classify wine types based on their physicochemical properties. Using the classic Wine dataset from scikit-learn, we demonstrate how Decision Trees, Random Forests, and Support Vector Machines can be applied to a multiclass classification problem.

## Dataset
The Wine dataset contains 178 samples with 13 different chemical measurements for each wine:

Alcohol

Malic acid

Ash

Alcalinity of ash

Magnesium

Total phenols

Flavanoids

Nonflavanoid phenols

Proanthocyanins

Color intensity

Hue

OD280/OD315 of diluted wines

Proline

### These measurements are used to classify wines into three different categories (class_0, class_1, class_2).

## Algorithms Implemented
### 1. Decision Tree Classifier
A simple tree-based model that makes classification decisions by creating a series of if-then rules based on feature thresholds.

### 2. Random Forest Classifier
An ensemble method that combines multiple decision trees to improve predictive accuracy and control overfitting.

### 3. Support Vector Machine (SVM)
A powerful classifier that finds the optimal hyperplane to separate different classes in high-dimensional space.

## Project Structure
The implementation includes:

Data loading and exploratory analysis

Feature scaling (for SVM)

Model training and evaluation

Cross-validation for performance assessment

Hyperparameter tuning using GridSearchCV

Feature importance analysis

Comprehensive model comparison

## Key Results
After thorough evaluation, the models performed as follows:

Decision Tree: 89% accuracy

Random Forest: 97% accuracy

Support Vector Machine: 100% accuracy

### The SVM model achieved perfect classification on the test set, demonstrating the effectiveness of appropriate feature scaling for this algorithm.

## Technical Features
Data Preprocessing: Standard scaling applied for SVM

Model Evaluation: Accuracy, precision, recall, and F1-score metrics

Cross-Validation: 5-fold cross-validation to ensure robust performance estimates

Hyperparameter Tuning: Grid search optimization for Random Forest parameters

Feature Importance: Analysis of which chemical properties most influence classification

Visualization: Correlation matrices, feature importance plots, and confusion matrices

## How to Run
Open the Google Colab notebook

Run all cells sequentially

The code will automatically:

Load and analyze the dataset

Train and evaluate all three models

Perform cross-validation

Tune hyperparameters

Generate all visualizations

## Requirements
Python 3.x

scikit-learn

pandas

numpy

matplotlib

seaborn

## Conclusion
This project demonstrates that all three algorithms can effectively classify wine types based on chemical properties, with Support Vector Machines achieving perfect performance when properly configured. The analysis also reveals that proline content, flavanoids, and color intensity are the most important features for distinguishing between wine types.

The implementation follows machine learning best practices including proper train-test splitting, feature scaling, cross-validation, and comprehensive model evaluation.
