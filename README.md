# PredictHer AI – Proactive Women Safety System

Proactive Women Safety System using AI – Predicts unsafe situations and provides recommendations
**Software Requirements Specification (SRS) | v1.0 | 2026**

---

## 1. Project Name

PredictHer AI – Proactive Women Safety System

---

## 2. Background

**Purpose:**
An AI-based safety system that predicts unsafe situations before they occur and provides timely alerts.

**Problem Statement:**
Existing safety apps react after incidents. PredictHer AI predicts risk in advance using contextual data, helping users proactively avoid unsafe situations.

---

## 3. Objectives

* Predict unsafe situations using time, location, and movement.
* Provide real-time risk levels.
* Generate safety recommendations.
* Assist proactive decision-making.
* Provide an interactive dashboard for visualization.

---

## 4. Project Scope

**Included:**

* AI-based model predicting safety risk.
* Input features: time, location type, crowd level, movement.
* Preventive recommendations via Streamlit dashboard deployed on cloud.

**Excluded:**

* Real-time GPS tracking.
* Emergency service integration.
* Mobile or hardware implementation.

**Constraints:**

* Limited availability of real-world data.
* Reliance on simulated datasets.
* Model accuracy depends on input quality.

---

## 5. Proposed Solution

| Component             | Technology / Approach                              | Description                                                     |
| --------------------- | -------------------------------------------------- | --------------------------------------------------------------- |
| Risk Prediction Model | Scikit-learn (Random Forest / Logistic Regression) | Predicts risk level (Low, Medium, High) based on input features |
| Recommendation Model  | Rule-based suggestions                             | Generates preventive actions for users                          |
| Frontend              | Streamlit dashboard                                | Interactive web-based interface                                 |
| Deployment            | Pickle + Streamlit Cloud                           | Saves model and runs dashboard online                           |

---

## 6. Comparison with Existing Projects

| Project / App    | Focus                  | Difference with PredictHer AI                       |
| ---------------- | ---------------------- | --------------------------------------------------- |
| bSafe            | Emergency alerts       | Reactive, PredictHer AI is predictive               |
| Noonlight        | Personal safety        | Reactive, Predictive risk scoring not included      |
| Google Maps      | Location & safety info | Only provides info, not risk prediction             |
| Red Panic Button | Panic alerts           | Works after incident, PredictHer AI predicts before |

PredictHer AI is focused on proactive safety prediction.

---

## 7. Datasets

* [Women Harassment Dataset – Kaggle](https://www.kaggle.com/datasets/thevincida/women-harassment-dataset)
* [Crime Data – Kaggle](https://www.kaggle.com/datasets/fatmanur12/crime-data)

Raw datasets will be stored in `data/raw/` and processed datasets in `data/processed/`.

---

## 8. Resources

* [Scikit-learn](https://scikit-learn.org/)
* [Streamlit](https://streamlit.io/)
* [Kaggle Datasets](https://www.kaggle.com)
* [GitHub](https://github.com/)

---

## 9. System Architecture

1. **Data Collection & Preprocessing**

   * Load and clean datasets
   * Encode categorical variables
   * Normalize features

2. **Risk Prediction Model**

   * Algorithms: Random Forest / Logistic Regression
   * Output: Risk levels (Low, Medium, High)

3. **Recommendation Engine**

   * Rule-based system to generate preventive suggestions

4. **Interactive Dashboard**

   * Input: time, location, crowd level, movement
   * Output: predicted risk & safety recommendations
   * Visualization with Streamlit

---

## 10. Technology Stack

* Programming Language: Python 3.x
* Machine Learning: Scikit-learn
* Data Processing: Pandas, NumPy
* Visualization: Matplotlib, Seaborn
* Web Dashboard: Streamlit
* Model Persistence: Pickle
* Deployment: Streamlit Cloud

---

## 11. Installation & Usage

**Clone repository**

```bash
git clone https://github.com/<username>/PredictHer-AI.git
cd PredictHer-AI
```

**Create virtual environment (optional)**

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
```

**Install dependencies**

```bash
pip install -r requirements.txt
```

**Run Streamlit dashboard**

```bash
streamlit run src/dashboard.py
```

**Dashboard Interaction:**

* Enter time, location type, crowd level, movement
* View predicted risk level
* Get recommended actions

---

## 12. Project Structure

```
PredictHer-AI/
│
├── README.md
├── LICENSE
├── requirements.txt
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── data_exploration.ipynb
│   └── model_training.ipynb
├── src/
│   ├── data_preprocessing.py
│   ├── model_training.py
│   ├── recommendation.py
│   └── dashboard.py
├── models/
│   └── risk_model.pkl
├── tests/
│   └── test_model.py
└── .gitignore
```

---

## 13. Future Work

* Real-time GPS tracking integration
* Mobile application for instant alerts
* Expand datasets for improved model accuracy
* Integration with emergency response services
* Personalized recommendations using user profiles

---

## 14. References

* [Scikit-learn Documentation](https://scikit-learn.org/)
* [Streamlit Documentation](https://streamlit.io/)
* [bSafe – Safety App](https://www.bsafe.com/)
* [Noonlight – Safety App](https://www.noonlight.com/)
* [Red Panic Button](https://www.redpanicbutton.com/)
* [Google Maps](https://maps.google.com/)


