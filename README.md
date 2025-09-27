🩺 Chronic Kidney Disease (CKD) Detection with Machine Learning
📌 Overview

This repository provides a machine learning pipeline for detecting Chronic Kidney Disease (CKD) from clinical data. The model uses patient health indicators (age, blood pressure, blood glucose, hemoglobin, etc.) to classify whether a patient is likely to have CKD.

The implementation is built with Python (scikit-learn, pandas, numpy) and follows these steps:

Load and preprocess the dataset

Handle missing values

Encode categorical variables

Scale numerical features

Train a Random Forest Classifier

Evaluate model performance

Identify important features

Provide a manual prediction function for new patient data

⚙️ Features

Automatic detection of target column (class / classification)

Preprocessing pipeline for missing values and encoding

Train/test split with stratification

Random Forest model for robust performance

Feature importance ranking

Manual prediction API for custom inputs

📂 Repository Structure
├── kidney_disease.csv       # Dataset (or instructions to download)
├── chronic_kidney.py        # Main pipeline script
├── requirements.txt         # Dependencies
└── README.md                # Documentation

🚀 How to Run

Clone the repo:

git clone https://github.com/your-username/chronic-kidney-disease.git
cd chronic-kidney-disease


Install dependencies:

pip install -r requirements.txt


Run the script:

python chronic_kidney.py

📊 Model Evaluation

Algorithm: Random Forest Classifier

Metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix

The script automatically prints:

Overall accuracy

Confusion matrix

Classification report

Top 10 most important features

🔮 Example Usage
Sample Predictions

The script outputs predictions for the first 20 test cases:

True: 1 → Predicted: CKD (Disease)
True: 0 → Predicted: Not CKD
...

Manual Prediction
example_patient = {
    "age": 40, "bp": 80, "sg": 1.02, "al": 1, "su": 0, "rbc": 1, "pc": 1,
    "pcc": 0, "ba": 0, "bgr": 120, "bu": 36, "sc": 1.2, "sod": 138, "pot": 4.5,
    "hemo": 15, "pcv": 44, "wc": 6700, "rc": 5.2, "htn": 1, "dm": 0, "cad": 0,
    "appet": 1, "pe": 0, "ane": 0
}
print(predict_new(example_patient))


Output:

CKD (Disease)

📈 Future Enhancements

Add hyperparameter tuning with GridSearchCV / Optuna

Test deep learning models for improved performance

Build a Flask/Streamlit web app for real-time predictions

📜 License

This project is licensed under the MIT License.
