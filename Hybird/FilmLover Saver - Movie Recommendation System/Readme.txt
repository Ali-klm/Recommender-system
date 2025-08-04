# FilmLover Saver - Movie Recommendation System

This project implements a hybrid movie recommendation system using the MovieLens dataset. It combines content-based filtering and collaborative filtering techniques to recommend movies to users.

## Dataset

The dataset files are located in the `Data` folder:
- `u.data`: User ratings data (user_id, item_id, rating, timestamp)
- `u.item`: Movie metadata including movie titles, release dates, IMDb URLs, and genre indicators

## Project Overview

- Load and preprocess MovieLens data.
- Create user profiles based on highly rated movies.
- Compute movie similarity using content features (genres).
- Implement content-based recommendation.
- Implement collaborative filtering using user similarity based on ratings.
- Combine content-based and collaborative filtering for hybrid recommendations.
- Evaluate the recommendation system using Precision@K metric.

## Usage

1. Load the dataset from the `Data` folder.
2. Run the notebook/script to generate recommendations.
3. Use functions:
    - `get_content_based_recommendations(user_id, num_recommendations=10)`
    - `get_collaborative_recommendations(user_id, num_recommendations=10)`
    - `get_hybrid_recommendations(user_id, alpha=0.5, num_recommendations=10)`

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## How to Run

Make sure you have the required packages installed. You can install them via:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
