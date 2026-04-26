# Heart Attack Prediction

An end-to-end machine learning project that predicts the risk of a heart attack based on clinical parameters — from exploratory data analysis to a deployed Streamlit web application backed by a FastAPI model server.

## Project Structure

```
heart-attack-prediction/
├── app/                  # FastAPI backend application
├── model/                # Trained ML model files
├── streamlit_app.py      # Streamlit frontend app
├── Dockerfile            # Docker configuration for deployment
└── requirements.txt      # Python dependencies
```

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## Features

- **Clinical Input Form** — Users enter patient details (age, sex, chest pain type, cholesterol, blood pressure, etc.)
- **ML Prediction** — Trained classification model predicts heart attack risk with a probability score
- **FastAPI Backend** — Model served via a REST API deployed on Render
- **Streamlit Frontend** — Interactive web interface for real-time predictions
- **Dockerized** — Fully containerized for easy deployment

## How It Works

1. User inputs clinical parameters via the Streamlit app
2. The app sends a POST request to the FastAPI backend at `/predict/`
3. The backend runs the trained model and returns a prediction + probability
4. The result is displayed as **Heart Attack Risk** or **No Risk**

## Input Parameters

| Parameter | Description |
|---|---|
| Age | Patient age in years |
| Sex | Male / Female |
| CP | Chest pain type (Typical Angina, Atypical Angina, Non-Anginal, Asymptomatic) |
| Trestbps | Resting blood pressure (mm Hg) |
| Chol | Serum cholesterol (mg/dl) |
| FBS | Fasting blood sugar > 120 mg/dl |
| Restecg | Resting electrocardiographic results |
| Thalach | Maximum heart rate achieved |
| Exang | Exercise induced angina |
| Oldpeak | ST depression induced by exercise |
| Slope | Slope of peak exercise ST segment |
| CA | Number of major vessels (0–4) |
| Thal | Thalassemia type |

## Running Locally

```bash
# Install dependencies
pip install -r requirements.txt

# Run the Streamlit app
streamlit run streamlit_app.py
```

## Running with Docker

```bash
docker build -t heart-attack-prediction .
docker run -p 8000:8000 heart-attack-prediction
```

## Dataset

Based on the classic Heart Disease dataset — 13 clinical features used to predict the presence of heart disease.

---

*Built by [Monish Mithra Kadiyala](https://linkedin.com/in/monishmithra) · MS Data Science @ University at Buffalo*
