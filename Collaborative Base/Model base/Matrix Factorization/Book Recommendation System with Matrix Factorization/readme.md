## 📚 Book Recommendation System with Matrix Factorization

This repository contains a collaborative filtering-based recommendation system for books using matrix factorization and stochastic gradient descent (SGD). The model learns user and item latent features and biases to predict ratings and generate personalized book recommendations.

### 🔍 Project Overview

The system:

- Loads preprocessed data containing user-item interactions.
- Learns user/item latent features and bias terms.
- Trains using SGD and minimizes RMSE.
- Evaluates on unseen test data.
- Produces top-N book recommendations for specific users.

---

### 📁 Dataset Structure

The required data files are located in the `Data` folder:

| File Name          | Description                                                                                      |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| `train_matrix.npz` | Sparse matrix of user-item training ratings.                                                     |
| `test_matrix.npz`  | Sparse matrix of user-item test ratings.                                                         |
| `mapped_ids.npz`   | Contains ID mappings for users and items used in the model.                                      |
| `unique.npz`       | Contains `unique_user_ids` and `unique_item_ids` arrays used for ID mapping and inverse mapping. |

---

### 🚀 How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/book-recommender.git
   cd book-recommender
   ```

2. Make sure you have the required libraries:

   ```bash
   pip install numpy scipy
   ```

3. Run the notebook:

   Open the Jupyter notebook (`initial.ipynb`) and run all cells in order.

   > Make sure the `Data` folder with all `.npz` files is in the same directory as the notebook.

4. To generate the final submission file:

   Run the last cell to create a `result.zip` file which includes:

   - The trained notebook (`initial.ipynb`)
   - The final predictions (`submission.npz`)

---

### 📈 Model Evaluation

The model is evaluated using **Root Mean Squared Error (RMSE)** and **F1 Score** for top-N recommendations. Performance can be improved by tuning the following hyperparameters:

- Number of latent features (k)
- Learning rate (α)
- Regularization factor (λ)
- Number of epochs

---

### 📬 Output

The recommendation results are saved as a list of `(item_id, predicted_rating)` tuples per user. These are stored in `submission.npz` and used for evaluation.

---

### ✏️ Notes

- The recommendation function avoids suggesting books already rated by the user.
- The ID mapping ensures consistency between original IDs and the model’s internal indices.
- All predicted ratings are bounded and ranked to prioritize top suggestions.

---

Feel free to contribute, open issues, or fork the project if you find it helpful!

