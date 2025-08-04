# Alternating Least Squares (ALS) Recommender System

This project implements a **collaborative filtering recommender system** using the **Alternating Least Squares (ALS)** algorithm with user and item bias terms. The model is trained to predict user-item interactions (e.g., ratings) and generate personalized top-N recommendations.

## 📁 Dataset

The data used in this project is stored in the `Data/` directory. It includes:

- `train_matrix.npz`: Sparse user-item matrix used for training (in COO format).
- `test_matrix.npz`: Sparse user-item matrix used for evaluation (in COO format).
- `unique.npz`: A NumPy archive containing:
  - `users`: Array of unique user IDs.
  - `items`: Array of unique item IDs.

## 🧠 Model Overview

The recommender model factorizes the user-item interaction matrix into two low-rank matrices:

- **P**: User latent feature matrix.
- **Q**: Item latent feature matrix.

Each user and item also has a learned **bias term**, and the model is regularized using L2 regularization.

The rating prediction formula is:

```
predicted_rating = global_average + user_bias + item_bias + dot(P_user, Q_item)
```

## 🔁 ALS Training Loop

The training procedure iteratively updates:

1. **User features and bias** (fixing item features and bias)
2. **Item features and bias** (fixing user features and bias)

Using the **Least Squares method**, it solves for each user/item independently using observed interactions.

## 📈 Evaluation

The model performance is measured using **Root Mean Squared Error (RMSE)** on both training and test datasets.

Example RMSE log per epoch:
```
Iteration 1/10, Train RMSE: 0.9123, Test RMSE: 0.9476
...
```

## 🔮 Inference and Recommendations

- **Single prediction**: You can predict the rating a user might give to an item.
- **Top-N recommendations**: The function `get_recommendations(...)` generates the top-N recommended items for a given user.

Example:
```python
get_recommendations(original_user_id=8, n=5, ...)
```

## ⚙️ Hyperparameters

| Parameter      | Value |
|----------------|-------|
| `k` (latent factors) | 5     |
| `lambda_reg`   | 10    |
| `num_epochs`   | 10    |

## 🛠️ Requirements

- Python 3.x
- NumPy
- SciPy
- Pandas

Install dependencies with:
```bash
pip install numpy scipy pandas
```

## 📌 Notes

- The model uses **mapped internal indices** for matrix operations. Original IDs are recovered using the `unique.npz` mapping.
- The code handles cold-start users/items by falling back to the global average.

## 📄 File Structure

```
├── initial.ipynb              # Main notebook (exported script)
├── Data/
│   ├── train_matrix.npz       # Training data (COO sparse matrix)
│   ├── test_matrix.npz        # Test data (COO sparse matrix)
│   └── unique.npz             # Mapping from internal indices to original user/item IDs
```

## 📬 Contact

For questions or feedback, feel free to open an issue or contact the project maintainer.
