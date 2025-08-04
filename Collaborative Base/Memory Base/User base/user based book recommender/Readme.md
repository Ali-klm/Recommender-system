# User-Based Book Recommender 📚

A simple user-based collaborative filtering (UBCF) recommendation system that predicts book ratings and generates personalized suggestions for users using similarity-based techniques.

---

## 🔍 Project Overview

This project builds a recommender system using **explicit rating data**. Given a dataset of user ratings for various books, we:
- Clean and filter the data.
- Construct a user-item matrix.
- Compute user-user similarity using **cosine similarity**.
- Generate book recommendations based on the top-K similar users.
- Predict ratings for unseen books.
- Evaluate the model using **Mean Absolute Error (MAE)**.

---

## 🗃️ Dataset

The project uses three CSV files located in the `Data/` folder:

- `bookdata2.csv`: Main dataset containing user-book ratings.
- `test_95359.csv`: Evaluation set for user with ID `95359`.
- `test_158295.csv`: Evaluation set for user with ID `158295`.

> ℹ️ These datasets include book ISBNs, titles, and user ratings on a 0–10 scale.

---

## 🧠 Techniques Used

- User-Based Collaborative Filtering (UBCF)
- Cosine Similarity
- Weighted average prediction for ratings
- Mean Absolute Error (MAE) for evaluation

---

## 📁 Project Structure
Data/
├── bookdata2.csv
├── test_95359.csv
├── test_158295.csv
/
├── Main.ipynb # Main Jupyter notebook with all code

---

## ✅ How to Use

1. Clone the repository:
```bash
git clone https://github.com/yourusername/user-based-book-recommender.git
cd user-based-book-recommender
2.Run the Jupyter notebook recommender.ipynb.

3.Make sure the Data/ folder contains all three CSV files.
Evaluation
The system estimates user ratings for test books and evaluates the predictions using MAE.

