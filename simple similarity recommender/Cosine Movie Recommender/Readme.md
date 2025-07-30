# 🎬 Cosine-Based Movie Recommender

This is a simple **content-based movie recommender system** built using cosine similarity. It suggests movies based on the genres of the user's favorite titles.

## 📌 How It Works

The system:
- Uses movie genres as features.
- Applies `CountVectorizer` to convert genres to numerical vectors.
- Computes cosine similarity between movies.
- Builds a user profile based on favorite movies.
- Recommends movies similar to the user's profile.

## 🛠️ Dependencies

Make sure to install the following Python libraries:

```bash
pip install pandas scikit-learn
