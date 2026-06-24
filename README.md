# 🛡️ Fake Internship & Scam Job Detection System

### An AI-powered tool to protect students from fraudulent job postings.

![Python](https://img.shields.io/badge/Python-3.11-blue) ![Framework](https://img.shields.io/badge/Framework-Flask-green) ![ML](https://img.shields.io/badge/Library-TensorFlow%20%2F%20Keras-orange) ![Status](https://img.shields.io/badge/Status-Active-success)

## 📌 Project Overview
In the current job market, scam job postings and fake internships are a growing threat, particularly for students and fresh graduates. These fraudulent listings often aim to steal personal data or demand money for "training" or "security deposits."

This project is a **Deep Learning-based Web Application** that analyzes job descriptions and predicts whether they are **Legitimate** or **Fraudulent**. It uses Natural Language Processing (NLP) techniques and a trained LSTM (Long Short-Term Memory) neural network to detect patterns common in scam listings.


## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3, JavaScript
* **Backend:** Flask (Python)
* **Machine Learning:** TensorFlow, Keras
* **Data Processing:** NumPy, Pickle
* **Deployment:** Render / Gunicorn

## 📂 Project Structure
```bash
Fake-Internship-Scam-Detection/
│
├── app.py                   # Main Flask application
├── EDA_job_data.ipynb       # complete analysis of the data
├── fake_job_detection.h5    # Trained Keras Model (LSTM)
├── tokenizer.pkl            # Tokenizer for text preprocessing
├── requirements.txt         # List of dependencies
├── fake_job_postings.csv    # Data used for training the model
├── Procfile                 # Deployment configuration for Render
│── style.css            # Styling for the web interface
│
|── index.html           # Frontend user interface
```

### Model Architecture & Workflow


* Input: The user pastes a job description (Title, Company, Description, Requirements) into the web interface.

### Preprocessing:

* The text is cleaned and converted into a sequence of integers using a pre-fitted Tokenizer.

* The sequence is padded to a length of 200 to match the model's input layer.

### Inference:

* The processed data is fed into the loaded Keras (.h5) model.

* The model is trained on the EMSCAD and outputs a probability score between 0 and 1.

### Output:

* Score > 0.7: Classified as Fraudulent.

* Score <= 0.7: Classified as Legitimate.


# 🔮 Future Scope
Chrome Extension: Integrate the model directly into job portals like LinkedIn or Internshala.

Explainable AI: Highlights specific words (e.g., "fast cash," "no experience") that triggered the fraud detection.

Real-time Scraping: Automatically fetch and verify latest job posts.


