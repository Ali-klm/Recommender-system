# Music Recommender System

An intelligent music recommendation system that suggests similar songs based on a given track title using machine learning techniques.

---

## Project Overview

This project builds a content-based music recommender system using a dataset containing track information such as song title, artist, and audio features.  
The system processes text data with TF-IDF vectorization and normalizes numeric audio features to calculate cosine similarity between songs, enabling it to recommend tracks similar to the input.

---

## Project Structure

- `Music Recommender system.ipynb`: Jupyter Notebook containing the full implementation of the recommender system  
- `data/music_data.csv`: Dataset with 10,000 songs and their corresponding audio features and metadata

---

## How It Works

1. Load the dataset from `data/music_data.csv`  
2. Preprocess text and numeric features  
3. Extract text features using TF-IDF vectorization  
4. Normalize numeric features  
5. Combine text and numeric features into a single feature matrix  
6. Compute cosine similarity between songs  
7. Implement a recommendation function that returns 21 similar songs for a given track  
8. Generate a DataFrame of recommendations for a selection of tracks

---

## Dependencies

- numpy  
- pandas  
- scikit-learn  
- scipy

---

## Usage

1. Place the `music_data.csv` file inside the `data/` directory  
2. Run the notebook `Music Recommender system.ipynb` step-by-step  
3. Call the `recommender(music_name)` function with a track title to get 21 recommended songs  
4. Use the provided list of tracks to generate recommendations and store them in a DataFrame

---

## Notes

This project is intended for educational purposes to demonstrate content-based recommendation and machine learning concepts. It can serve as a foundation for more advanced recommendation systems.

---

## Contact

Feel free to open an issue or reach out if you have any questions or suggestions.

---

© 2025 Music Recommender System
