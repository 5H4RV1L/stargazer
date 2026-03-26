# 🌌 Stargazer AI — Exoplanet Classifier

A full-stack machine learning web application that allows users to train and deploy an **XGBoost-based classifier** for predicting exoplanet dispositions from tabular data.

Built with a complete pipeline: **data upload → preprocessing → training → evaluation → prediction**, all through an interactive UI.

---

## 🚀 Features

- 📊 Upload labelled datasets (CSV)
- 🧠 Train ML model with:
  - XGBoost classifier
  - SMOTE for class balancing
  - 5-fold Stratified Cross Validation
- 📈 Model evaluation:
  - Accuracy, Precision, Recall, F1-score
  - Confusion Matrix
- 💾 Model persistence (saved & auto-loaded)
- 🔮 Predict on new/unlabelled datasets
- 🔍 Row-wise prediction viewer
- 🎨 Modern glassmorphism UI with animated starfield

---

## 🧠 ML Pipeline Overview

1. **Data Upload**
2. **Preprocessing**
   - Missing value handling (median/mode)
   - Label encoding for categorical data
   - Feature scaling (StandardScaler)
3. **Feature Engineering**
   - Radius ratio
   - Log transformations
   - Derived relationships
4. **Class Balancing**
   - SMOTE (Synthetic Minority Oversampling)
5. **Model Training**
   - XGBoost with cross-validation
6. **Evaluation**
   - Multiple metrics + confusion matrix
7. **Prediction**
   - Automatic preprocessing + inference

---

## 🖥️ Tech Stack

### Backend
- Python
- Flask
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)

### Frontend
- HTML, CSS, JavaScript
- Custom glassmorphism UI

---

## 📂 Project Structure

    ├── app.py
    ├── templates/
    │   ├── index.html
    │   └── guide.html
    ├── static/
    │   ├── styles.css
    │   └── model_cache/
    ├── demo/
    │   ├── train.csv
    │   └── test.csv

---

## ⚙️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/stargazer-ai.git
cd stargazer-ai
```

### 2. Install dependencies
```bash
pip install flask pandas numpy scikit-learn xgboost imbalanced-learn joblib
```

### 3. Run the app
```bash
python app.py
```

### 4. Open in browser
```
http://127.0.0.1:5000/
```

---

## 📊 Dataset Requirements

- Must be a **CSV file**
- Must include target column:

```
koi_disposition
```

### Example features:
- koi_period
- koi_depth
- koi_duration
- koi_prad
- koi_srad

---

## 📸 Workflow

1. Upload labelled dataset  
2. Train model  
3. Upload test dataset  
4. Run predictions  

---

## 💾 Model Persistence

- Models are saved using `joblib`
- Automatically reloaded on server restart
- No retraining required unless data changes

---

## 🎯 Use Cases

- Exoplanet classification (Kepler dataset)
- Tabular ML experimentation
- ML pipeline demos
- Educational projects

---

## 🔧 Future Improvements

- Hyperparameter tuning UI
- Model comparison (RF, SVM, etc.)
- Data visualization dashboard
- Export predictions as CSV
- Authentication & multi-user support

---

## 👨‍💻 Author

**Sharvil Sagalgile**  
GitHub: https://github.com/5H4RV1L

---

## ⭐ Acknowledgements

- NASA Kepler dataset (KOI)
- Scikit-learn ecosystem
- XGBoost
