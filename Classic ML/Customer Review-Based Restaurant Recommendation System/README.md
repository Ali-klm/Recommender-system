
# 📌 Customer Review-Based Restaurant Recommendation System

This project is a machine learning-based **restaurant recommendation system** that leverages **user reviews** to predict whether a customer will like a restaurant. It includes **data cleaning**, **text processing**, **feature extraction**, **classification models**, and **recommendation logic**.

---

## 📂 Project Structure

```
project/
│
├── Data/
│   └── comments.csv         # Raw dataset containing user reviews
│
├── initial.ipynb            # Main notebook containing all steps
└── README.md                # Project overview
```

---

## 📊 Dataset

- The dataset file is located at: `Data/comments.csv`.
- It includes user reviews, ratings, restaurant codes, delivery experience feedback, and metadata like `feeling`, `expeditionType`, and `vendorType`.

---

## ⚙️ Workflow

### 1. **Data Loading and Cleaning**
- Loads review data from `comments.csv`.
- Drops irrelevant or missing data and fills missing values where appropriate.
- Removes unneeded columns (e.g., address, deliveryComment, replies).

### 2. **Text Preprocessing**
- Normalization and tokenization using the **Hazm** library.
- Persian stopwords removed.
- Cleaned text is stored in `cleaned_comment`.

### 3. **Feature Engineering**
- **TF-IDF Vectorization** for both users and restaurants.
- Generated:
  - `user_*` features (user text profile)
  - `resto_*` features (restaurant text profile)
- Aggregated user statistics: average rating, comment count.

### 4. **Label Creation**
- Defined a binary label `will_like`: 
  - `1` if rating > 6 
  - `0` otherwise

### 5. **Data Encoding & Scaling**
- Categorical encoding using `LabelEncoder`.
- Normalization with `StandardScaler`.

### 6. **Model Training**
Multiple models were trained:
- Logistic Regression
- Decision Tree
- Random Forest (including smaller & larger versions)
- Gradient Boosting

All were evaluated using:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

### 7. **Recommendation Engine**
- For a selected user (e.g., ID: `1322757`), the system:
  - Identifies unrated restaurants.
  - Predicts probability of liking each restaurant.
  - Recommends top restaurants based on predicted scores.

---

## 📦 Dependencies

Install required packages (e.g., in Google Colab or a local environment):

```bash
pip install hazm
```

Other dependencies:
- pandas
- numpy
- scikit-learn
- hazm
- re

---

## 🚀 How to Run

1. Make sure your `comments.csv` file is placed in the `Data/` folder.
2. Open and run the notebook `initial.ipynb` (preferably in **Google Colab**).
3. Follow the cells sequentially to process data, train models, and generate recommendations.

---

## 📈 Example Output

The model predicts a **recommendation score** for each restaurant. The top 250 recommended restaurants for a user are extracted as the final result in:

```python
submission = recommendation_df[["code", "recommendation_score"]].head(250)
```

---

## 🙋‍♂️ Author

This project was developed as part of a machine learning pipeline to explore Persian-language user reviews and generate personalized recommendations.

Feel free to open issues or suggest improvements.
