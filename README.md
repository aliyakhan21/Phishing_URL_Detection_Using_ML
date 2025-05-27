# 🛡️ Phishing URL Detection System

This is a Flask-based web application that detects whether a given URL is **phishing** or **legitimate** using a trained Random Forest machine learning model.

## 📌 Architecture Overview

```
User → Web Interface → Flask Backend → ML Model → Response
```

1. Users enter a URL via a web form.
2. The Flask backend extracts features from the URL.
3. These features are passed to a pre-trained ML model (`final_model.pkl`).
4. The model returns a prediction:  
   - `1` = Phishing  
   - `0` = Legitimate
5. The result is shown on the webpage.

---

## 🛠️ Setup Instructions

### ✅ Requirements

- Python 3.9 or higher  
- Install dependencies:

```bash
pip install -r requirements.txt
```

### 📁 Project Structure

```
ML_Flask_App/
├── Dockerfile                     # For containerization
├── app.py                         # Main Flask app
├── test_prediction.py             # Optional testing script
├── final_model.pkl                # Pre-trained ML model
├── requirements.txt               # Python dependencies
├── deployment_documentation.docx # Deployment instructions
└── templates/
    └── index.html                 # Web UI
```

### ▶️ Running the App

1. Open terminal and navigate to the project directory:

```bash
cd ML_Flask_App/
```

2. (Optional) Activate your Python virtual environment.

3. Start the Flask server:

```bash
python app.py
```

4. Visit the app at: [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

---

## 📊 Monitoring & Maintenance

- **Model Accuracy**  
  - Regularly evaluate using updated phishing datasets.  
  - Retrain and replace `final_model.pkl` as needed.

- **Logging**  
  - Add logs to track predictions, errors, and API calls.

- **Security**  
  - Sanitize user inputs.  
  - Use HTTPS in production.

- **Performance**  
  - Monitor app response time and user load, especially if hosted online.

---

## 📦 Docker (Optional)

To run in a Docker container:

```bash
docker build -t phishing-detector .
docker run -p 5000:5000 phishing-detector
```

---

## 🧠 Author & License

Developed as part of an internship project for phishing detection using machine learning.




