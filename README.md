# 🧠 Mental Health Signal

Mental Health Signal is a full-stack AI/ML web application that predicts a student's mental health score from their daily digital habits — screen time, sleep, stress, study hours, and platform use. Built with a **FastAPI** backend serving a **scikit-learn** regression pipeline, and a vanilla HTML/CSS/JS frontend with an animated result gauge.

---

## ✨ Features

* 🧮 AI Score Prediction

  * Predicts a 0–10 mental health score from 12 lifestyle and digital-habit inputs.

* ⚡ RESTful API

  * Clean, Pydantic-validated `/predict` endpoint built with FastAPI.

* 🌲 Trained ML Pipeline

  * Random Forest Regressor, tuned via `RandomizedSearchCV`, packaged as a single `sklearn` pipeline.

* 🎛️ Interactive Frontend

  * Animated gauge UI with live validation and a segmented stress-level selector.

* 🗄️ Reproducible Notebook

  * Full EDA, cleaning, feature engineering, and model comparison in one notebook.

---

## 🛠️ Tech Stack

### Backend

* Python 3.10+
* FastAPI
* Pydantic
* Uvicorn
* Joblib

### Machine Learning

* scikit-learn
* pandas
* numpy
* matplotlib / seaborn

### Frontend

* HTML5
* CSS3
* Vanilla JavaScript

---

## 📁 Project Structure

```text
.
├── ML_Project_details.ipynb    # EDA, cleaning, feature engineering, model training
├── Mental_Health_Model.pkl     # Saved sklearn pipeline (preprocessing + model)
├── main.py                     # FastAPI app — /predict endpoint
├── requirements.txt            # Backend dependencies
├── index.html                  # Form + result UI
├── style.css                   # Styling for the form and animated gauge
├── script.js                   # Validation, API calls, gauge animation
└── README.md
```

---

## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/mental-health-score-predictor.git
```

### Navigate to the Project

```bash
cd mental-health-score-predictor
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Application

```bash
uvicorn main:app --reload --port 2200
```

The server will start on:

```
http://localhost:2200
```

Then open `index.html` in your browser (make sure `API_BASE` in `script.js` points to `http://127.0.0.1:2200`).

---

## 📡 API Overview

### Predict Mental Health Score

```http
POST /predict
```

**Request**

```json
{
  "age": 21,
  "gender": "Male",
  "country": "India",
  "academic_level": "Undergraduate",
  "most_used_platform": "Instagram",
  "purpose_of_use": "Entertainment",
  "avg_daily_usage_hours": 4.5,
  "daily_unlocks": 90,
  "study_hours": 3.5,
  "physical_activity_hours": 1.0,
  "sleep_hours_per_night": 6.5,
  "stress_level": "High"
}
```

**Response**

```json
{
  "predicted_mental_health_score": 6.42
}
```

---

## 📌 Upcoming Features

* 📊 Prediction Confidence Intervals
* 🧩 Feature-Importance Breakdown
* ☁️ Always-On Hosted Backend
* ✅ Automated API Tests
* 🌙 Dark Mode
* 📱 Responsive Layout Polish

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository, create a new branch, and submit a pull request. If you change the model, please regenerate `Mental_Health_Model.pkl` from the notebook rather than hand-editing the pickle.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Dev Singh**

If you found this project helpful, consider giving it a ⭐ on GitHub.
