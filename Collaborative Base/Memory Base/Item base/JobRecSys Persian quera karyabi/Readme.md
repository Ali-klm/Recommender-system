# Job Recommendation System – Quera Dataset (Item-Based Collaborative Filtering)

This project implements an **Item-Based Collaborative Filtering (IBCF)** recommender system using job application data from [Quera](https://quera.org). The goal is to suggest relevant job postings to users based on past interactions with similar job postings.

## 🔍 Overview

The system analyzes how users have interacted with job listings (by submitting resumes) and builds a model that:

- Calculates item-to-item similarity using binary interaction data.
- Supports multiple similarity metrics including **Jaccard**, **Dice**, and **Cosine**.
- Recommends job opportunities to users based on their application history.

This approach differs from traditional User-Based Filtering by focusing on the relationships between **jobs (items)** rather than **users**.


---

## 📊 Evaluation

The recommendation precision is evaluated using:
- **Precision@10**: Measures how many of the recommended items are in the same domain as the user's past applications.

The Jaccard and Cosine metrics showed strong correlation (Pearson ~0.99), but **Cosine** was ultimately chosen for recommendations due to its stable performance on sparse data.

---
🛠 Requirements
Python 3.7+

pandas

numpy

scikit-learn

matplotlib

scipy


