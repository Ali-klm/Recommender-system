# 🎬 Movie Recommendation System

This project is a **Content-Based Movie Recommendation System** built using Python. It analyzes metadata from more than 5,000 movies provided by the [TMDB 5000 Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) and recommends similar movies based on cast, crew, genres, keywords, and overview.

---

## 📁 Project Structure

```
project-root/
│
├── Data/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
│
├── movie_recommender.py   # Main script
└── README.md              # Project documentation
```

Make sure both dataset files are located inside the `Data/` folder.

---

## ⚙️ Features

- Merges two datasets (`movies` and `credits`) on the title field.
- Parses and extracts meaningful features from JSON-like fields such as genres, keywords, cast, and crew.
- Applies NLP techniques: stopword removal, lemmatization, and token cleaning.
- Constructs a unified `tags` column representing each movie's content.
- Converts text into numerical vectors using TF-IDF.
- Computes cosine similarity between movies.
- Recommends top 5 similar movies for any given title.

---

## 📦 Installation & Requirements

### 1. Install Dependencies

```bash
pip install numpy pandas scikit-learn nltk
```

### 2. Download NLTK Resources

```python
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
```

---

## 🚀 How to Run

1. Place both CSV files inside a `Data/` directory.
2. Open and run `movie_recommender.py`. Ensure the file paths are correctly set:

```python
movies = pd.read_csv("Data/tmdb_5000_movies.csv")
credits = pd.read_csv("Data/tmdb_5000_credits.csv")
```

3. Call the `recommend()` function with any movie title as a string:

```python
recommend("Avatar")
recommend("Batman")
recommend("Spider-Man")
recommend("Die Hard")
```

---

## 🧪 Example Output

```
Batman Begins
The Dark Knight
Batman v Superman: Dawn of Justice
The Dark Knight Rises
Justice League
```

---

## 🧠 Possible Improvements

- Add a simple UI using Streamlit or Flask
- Include movie posters and metadata using TMDB API
- Add collaborative filtering for hybrid recommendations
- Use dimensionality reduction (e.g., PCA) for faster similarity computations

---

## 📚 Dataset Information

- Source: [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- Files used:
  - `tmdb_5000_movies.csv`
  - `tmdb_5000_credits.csv`

---

## 📌 License

This project is for educational purposes only. Dataset is provided by TMDB and distributed via Kaggle under their terms of use.

---
