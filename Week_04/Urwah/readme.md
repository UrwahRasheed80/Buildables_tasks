Banknote Authentication System
Project Overview
This project implements a machine learning system that can authenticate banknotes as real or fake based on image analysis. The system automatically extracts statistical features from uploaded banknote images and uses a trained machine learning model to make predictions with high accuracy.

Features
Image-based Authentication: Upload banknote images for instant analysis

Feature Extraction: Automatically calculates variance, skewness, kurtosis, and entropy from images

Multiple ML Algorithms: Implements Decision Tree, Random Forest, and SVM classifiers

Web Interface: User-friendly Gradio interface for easy interaction

Detailed Reports: Provides feature analysis and confidence scores

Dataset
The system was trained on the Banknote Authentication Dataset from the UCI Machine Learning Repository. The dataset contains 1,372 samples with four features extracted from banknote images:

Variance: Measures the spread of pixel values in the image

Skewness: Measures the asymmetry of the pixel distribution

Kurtosis: Measures the peakedness of the pixel distribution

Entropy: Measures the randomness or disorder in the image

The target variable indicates whether the banknote is authentic (0) or counterfeit (1).

Model Performance
Three machine learning algorithms were implemented and evaluated:

Decision Tree Classifier: 98.55% accuracy

Random Forest Classifier: 100% accuracy

Support Vector Machine: 100% accuracy

The best performing model (Random Forest or SVM) was selected for deployment.

Installation
To run this project locally, install the required dependencies:

bash
pip install scikit-learn pandas numpy matplotlib seaborn opencv-python pillow gradio
Usage
Run the main script to launch the web interface

Upload a banknote image through the interface

Click "Analyze Banknote" to get results

Review the authentication report with feature analysis

How It Works
1. Image Processing
Converts uploaded images to grayscale

Resizes images to standard dimensions (200x100 pixels)

Flattens image pixels for statistical analysis

2. Feature Extraction
The system extracts four statistical features from each image:

Variance: Measures how spread out the pixel values are

Skewness: Measures the asymmetry of the pixel distribution

Kurtosis: Measures how peaked or flat the distribution is

Entropy: Calculates the randomness or information content

3. Machine Learning
Features are scaled using StandardScaler

Pre-trained Random Forest model makes predictions

Confidence scores are calculated from probability estimates

4. Results Display
Prediction (Real/Fake) with confidence percentage

Extracted feature values for transparency

Error handling for invalid images

File Structure
text
banknote-authentication/
├── main.ipynb              # Main implementation notebook
├── banknote_model.pkl      # Trained machine learning model
├── scaler.pkl              # Feature scaling parameters
└── README.md               # Project documentation
Technical Details
Programming Language: Python 3

ML Framework: Scikit-learn

Image Processing: OpenCV, PIL

Web Interface: Gradio

Data Persistence: Joblib for model serialization

Model Training
The training process includes:

Data loading from UCI Machine Learning Repository

Train-test split (80-20) with stratified sampling

Feature scaling using StandardScaler

Cross-validation for model evaluation

Model selection based on test accuracy

Web Interface
The Gradio web interface provides:

Image upload functionality (file upload or webcam)

Real-time processing and prediction

Detailed results display

User-friendly design

Limitations
This is a demonstration system for educational purposes

Performance depends on image quality and lighting conditions

Feature extraction may not match the original wavelet-based features exactly

Always verify important transactions with official methods

Contributing
This project is open for educational purposes. To contribute:

Fork the repository

Create a feature branch

Make your changes

Submit a pull request

License
This project is intended for educational use only. Please comply with all applicable laws and regulations regarding currency verification.

Acknowledgments
UCI Machine Learning Repository for the Banknote Authentication Dataset

Scikit-learn team for machine learning tools

Gradio team for the web interface framework

Support
For questions or issues with this project, please check the documentation above or create an issue in the GitHub repository.
