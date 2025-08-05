
# 🍽️ Mizban - Personalized Food Taste Prediction

**Mizban** is a machine learning application designed to predict a user's primary food taste based on lifestyle and background information. The ultimate goal is to provide highly personalized recipe recommendations using AI-driven classification and recommender systems.

---

## 📌 Project Overview

This project is a simplified prototype for the **Taste Prediction Pipeline** in Mizban. The system predicts a user's preferred taste category (e.g., sweet, sour, spicy, etc.) using their demographic and lifestyle data.

The pipeline consists of three core steps:

1. **Data Collection**  
   Input features include:
   - Age  
   - Sleep cycle  
   - Exercise habits  
   - Climate zone  
   - Historical cuisine exposure  

2. **Taste Prediction (Classification Model)**  
   Trained on labeled data using machine learning models like:
   - Logistic Regression  
   - Decision Tree  
   - Random Forest (final model used)

3. **Personalized Recommendation** *(not implemented here)*  
   Predicted taste can later be used in collaborative and content-based filtering systems to suggest dishes that best match the user's preferences.

---

## 📂 Dataset

Data is provided in two CSV files in the `Data/` directory:

- `train.csv` — 8000 rows with labels (preferred taste)
- `test.csv` — 1792 rows without labels (to be predicted)

Each row includes the following columns:

| Column                        | Type      | Description                              |
|------------------------------|-----------|------------------------------------------|
| `age`                        | float     | User's age                                |
| `sleep_cycle`                | category  | Sleep pattern                             |
| `exercise_habits`           | category  | User's exercise frequency/habits          |
| `climate_zone`              | category  | Geographic and weather information        |
| `historical_cuisine_exposure`| category  | Exposure to different global cuisines     |
| `preferred_taste`           | category  | Target column (only in train set)         |

---

## 🛠️ Preprocessing & Feature Engineering

- Missing values handled using median imputation
- Label Encoding for categorical features
- Age standardized using Z-Score scaling
- Outliers removed from training set based on Z-Score
- Train/Validation split with stratification to preserve label distribution

---

## 🤖 Model Training

Three models were evaluated:

- Logistic Regression → F1: ~0.57  
- Decision Tree → F1: ~0.85  
- ✅ **Random Forest (Best)** → F1: ~0.85

Macro-averaged F1-score was used as the primary evaluation metric, as required by the grading system.

---

## 📊 Evaluation

- Metric: `f1_score(average='macro')`  
- Achieved validation F1-score > **0.85**
- Ensured minimal overfitting between training and validation sets

---

## 🚀 How to Run

1. Clone the repository  
2. Place the dataset files (`train.csv`, `test.csv`) in `Data/` directory  
3. Run the main notebook or Python script:
   ```bash
   python main.py
   ```
4. The model will generate predictions and export a submission file:
   ```bash
   submission.csv
   ```

---

## 📈 Final Output

The output is a CSV file named `submission.csv` with one column:

| preferred_taste |
|-----------------|
| 3               |
| 1               |
| 0               |
| ...             |

---

## 📎 Dependencies

- Python 3.8+
- pandas
- numpy
- scikit-learn

Install via pip:
```bash
pip install -r requirements.txt
```

---

## 🧠 Future Work

- Integrate recommender systems (collaborative & content-based filtering)
- Experiment with neural networks
- Use more advanced feature engineering (e.g., interaction terms)

---

## 📬 Contact

Created as part of a university project on AI-based food recommendation systems.

Feel free to fork or contribute!
