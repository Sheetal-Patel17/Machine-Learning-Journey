# Heart Stroke Prediction

A Machine Learning web application that predicts the risk of heart disease using a trained **K-Nearest Neighbors (KNN)** model.

## Features

* User-friendly Streamlit interface
* KNN-based heart disease prediction
* Data preprocessing and feature scaling
* One-hot encoded categorical features
* Risk prediction with clear results

## Tech Stack

* Python
* Streamlit
* Pandas
* Scikit-learn
* Joblib
* Jupyter Notebook

## Project Files

* `app.py` — Streamlit web application
* `HeartdiseaseFinal.ipynb` — Model development and training
* `knn_heart_model.pkl` — Trained KNN model
* `heart_scaler.pkl` — Feature scaler
* `heart_columns.pkl` — Expected feature columns
* `requirements.txt` — Required Python libraries

## Run Locally

```bash
pip install -r requirements.txt
python -m streamlit run app.py
```

## Disclaimer

This project is developed for **educational and research purposes only** and is not a substitute for professional medical advice.

**Developed by Sheetal Patel**
