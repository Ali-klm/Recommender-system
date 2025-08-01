# Persian News Recommender System

This project implements a simple recommender system for Persian news articles. Using Natural Language Processing (NLP) techniques and TF-IDF vectorization, it suggests news articles that are semantically similar based on their textual content.

---

## Features

- Persian text preprocessing including normalization, punctuation removal, number removal, tokenization, lemmatization, and stopword removal.
- Creating combined tags by merging news category labels and cleaned news text.
- Vectorizing text using TF-IDF with a limit of 5000 most frequent terms.
- Calculating semantic similarity between news articles using cosine similarity.
- Implementing a recommender function that returns the top 5 most similar news articles given a news index.

---

## Project Structure

├── Data/
│ └── news_data.csv # Raw news dataset
├── main.py # Main script containing the implementation
├── README.md # This README file
└── requirements.txt # Required Python packages
Place the dataset file news_data.csv inside the Data folder.

Run the main script:
python main.py
Use the find_similar_news(news_index, similarity_matrix) function to get the top 5 similar news articles for any news index.

Dataset Description
The dataset news_data.csv contains the following columns:

content: Full text of the news article.

label: News category label (e.g., Sports, Politics, International).

label_id: Numeric ID corresponding to the news category.

Requirements
Python 3.x

pandas

scikit-learn

hazm (Persian NLP library)
