# ML Model Prediction API

A simple and smart Flask-based API that serves a pre-trained logistic regression model for making predictions. The API encodes categorical data before feeding it into the model and returns the result in JSON format.

## Features

- **JSON Input**: Accepts input via POST requests.
- **Categorical Encoding**: Converts categorical strings into numerical codes.
- **JSON Response**: Returns predictions as JSON.

## Requirements

- Python 3.x
- Flask
- joblib
- scikit-learn

Install the dependencies using:

```sh
pip install flask joblib scikit-learn


File Structur
.
├── Logistic-Regression.joblib  # Pre-trained ML model
└── app.py             # Flask API


API Endpoint
POST /predict

Description: Predicts the output based on the provided input data.
Request Body (JSON):

{
  "age": 35,
  "job": "technician",
  "marital": "married",
  "education": "secondary",
  "default": "no",
  "housing": "yes",
  "loan": "no"
}

Response Example:

{
  "prediction": ["yes|no"]
}