# Recommender System Projects

This repository contains multiple content-based recommender systems developed using TF-IDF vectorization and cosine similarity. Each subfolder is an independent project focusing on a different domain of recommendation.

---

## Folder Structure

│ ├── persian news recommender system/
│ │ └── (A content-based recommender for Persian news articles using NLP)
│ │
│ ├── music recommender tfidf cosine/
│ │ └── (A music recommender system based on lyrics or metadata similarity)
│ │
│ └── movie match tmdb/
│ └── (A movie recommendation project using TMDb data and content-based filtering)

## Projects Overview

### 1. Persian News Recommender System
A system that recommends similar Persian news articles based on text content using TF-IDF and cosine similarity. Includes full preprocessing for Persian language using the `hazm` library.

### 2. Music Recommender (TF-IDF + Cosine)
This project recommends songs based on lyric similarity, genre, or other metadata. It uses TF-IDF to vectorize song descriptions or lyrics and ranks songs by cosine similarity.

### 3. Movie Match (TMDb)
A content-based movie recommender that uses data from TMDb (The Movie Database). Movies are matched and recommended based on metadata such as genres, keywords, cast, and overview.

---

## Requirements

Each subproject includes its own `README.md` and `requirements.txt` file. Please refer to them individually for detailed setup instructions.

---

## How to Run

1. Navigate to any of the subproject folders inside `content based/`.
2. Follow the individual setup and execution instructions.
3. Python 3.x is required. All projects are self-contained and use common data science libraries.

---

Feel free to explore each folder and try out the recommendation demos!
