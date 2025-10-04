
Visa Eligibility Screening System (AI-Based)

Project Overview

This project is an AI-based Visa Eligibility Screening System that automatically evaluates visa applicants based on personal, financial, and background information. The system uses a Random Forest machine learning model to predict eligibility and provides probabilities for each decision.



Features

Predicts visa eligibility based on applicant data

Uses a combination of categorical and numerical features

Includes a simple web-based frontend to submit applications

Provides feature importance for explainability

Fast, consistent, and automated screening process



Dataset

Synthetic dataset generated using generate_dataset.py

Features include:

age, nationality, purpose, education, employment_years

criminal_record, previous_visas, bank_balance_k, sponsor_letter

language_score, intended_stay_months


Label: eligible (0 = Not Eligible, 1 = Eligible)




Installation

1. Create a virtual environment:



python -m venv venv

2. Activate the environment:



# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate

3. Install dependencies:



pip install -r requirements.txt



Usage

1. Generate Dataset

python generate_dataset.py

Generates visa_dataset.csv with 10,000 synthetic applicant records.

2. Train Model

python train_model.py

Trains a Random Forest classifier and saves the pipeline as visa_model.joblib.

3. Run API

python inference_api.py

Starts a Flask API at http://0.0.0.0:5000

Endpoints:

GET / → Returns API info

POST /predict → Accepts JSON input for applicant data and returns eligibility prediction



4. Frontend

Open frontend.html in a browser

Fill in applicant details and click Check Eligibility

Displays eligibility result with probability


5. Feature Importance

python explain.py

Shows top features influencing eligibility predictions



Requirements

Python 3.8+

Packages:

flask
pandas
numpy
scikit-learn
joblib




Notes

This is a demo system using synthetic data.

Do not use for real visa decisions without proper legal and ethical review.

Extendable with real data, additional features, and advanced ML models.




Author

Name: Sai Kumar Nethi
Course: AI
Institution: Anurag University



