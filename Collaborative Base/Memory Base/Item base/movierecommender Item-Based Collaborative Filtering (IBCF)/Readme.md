# 🎬 Movie Recommendation System - Item-Based Collaborative Filtering (IBCF)

This project implements a **movie recommendation system** using **Item-Based Collaborative Filtering (IBCF)**. It uses rating data from IMDb-like sources to recommend personalized movies for users based on similarity between items (movies) rather than users.


## 📊 Dataset

- `imdbMovies1.csv`: Contains user ratings for various movies.  
  Columns include: `userId`, `movieId`, `rating`, `title`, etc.
- `test.csv`: Additional test data for evaluation (optional).

## 🔍 Features

- Exploratory Data Analysis (EDA)
- Data Filtering (users ≥ 5 ratings, movies ≥ 10 ratings)
- Train/Test Splitting (Stratified 80/20)
- User-Movie Matrix Creation
- Similarity Calculation (Cosine & Pearson)
- Rating Prediction
- Evaluation (RMSE, MAE)
- Top-N Recommendation Generator
- Detailed Similarity-Based Insights

## ⚙️ How It Works

1. Filter sparse data
2. Train/test split
3. Create user-item matrix
4. Calculate item-item similarity
5. Predict ratings using top-k similar items
6. Evaluate with RMSE and MAE
7. Recommend top-N unseen movies

## 🧪 Evaluation Metrics

- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**

## ✅ How to Run

1. Clone the repository
2. Add `imdbMovies1.csv` and `test.csv` to the `Data/` folder
3. Open `Main.ipynb` in Colab or Jupyter and run all cells

