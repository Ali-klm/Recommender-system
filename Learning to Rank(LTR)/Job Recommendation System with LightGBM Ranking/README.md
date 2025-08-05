
# Job Recommendation System with LightGBM Ranking

This project presents a **hybrid job recommendation system** using **LightGBM's LambdaRank** algorithm along with item-based collaborative filtering (IBCF). The system is designed to recommend jobs to applicants based on their past applications and inferred preferences.

## 📌 Features

- **Data Cleaning & Normalization**: Preprocesses job titles, converts Persian job titles to standardized English keywords.
- **Job Categorization**: Classifies jobs into domains like `Frontend`, `Backend`, `Mobile`, `AI/Data`, `DevOps`, `UI/UX`.
- **Technology Extraction**: Extracts core technologies (e.g., `python`, `react`, `flutter`) from job titles.
- **User Profiling**: Builds static profiles for users based on their preferred job level, city, tech stack, and remote work tendency.
- **Negative Sampling**: Uses multiple negative sampling strategies, including:
  - Hard negatives (different domain/tech)
  - Dissimilar items from IBCF
  - Random (easy) negatives
- **Hybrid Recommendation**:
  - Candidate generation using **Item-Based Collaborative Filtering**
  - Ranking using **LightGBM LambdaRank** model trained on handcrafted features
- **Explainability**:
  - Feature importance visualization
  - Utilities to inspect user application history

## 🧠 ML Algorithm

- **Ranking Model**: [LightGBM LambdaRank](https://lightgbm.readthedocs.io/en/latest/Parameters.html#objective)
- **Evaluation Metric**: NDCG@10 (Normalized Discounted Cumulative Gain)
- **Group-Aware Splitting**: Preserves user-wise splits to prevent leakage

## 📁 Project Structure

| Component | Description |
|----------|-------------|
| `df_final` | Final dataframe with features and labels |
| `user_profiles` | Static user profile containing preferences |
| `job_features` | Cleaned job dataset with derived fields |
| `interaction_matrix` | User-job interaction matrix for IBCF |
| `generate_candidates_ibcf()` | Item-based collaborative filtering candidate generation |
| `generate_hybrid_recommendations_final()` | Final hybrid recommender pipeline |
| `extract_final_tech()` | Extracts most relevant technology from a job title |
| `get_job_domain()` | Classifies job title into major domain categories |

## 🛠 Technologies & Tools

- **Language**: Python
- **Libraries**: 
  - `pandas`, `numpy`, `scikit-learn`
  - `LightGBM`
  - `scipy` for sparse matrices and cosine similarity
  - `matplotlib`, `seaborn` for plotting

## ⚙️ How It Works

1. **Data Cleaning**: Drops irrelevant and incomplete rows, filters low-activity users and jobs.
2. **Title Normalization**: Persian job titles are mapped to English standard forms.
3. **Job Classification**: Each job is labeled with domain and key technology.
4. **Interaction Engineering**: Computes interaction features such as:
   - City match
   - Level match
   - Domain match
   - Technology match
5. **TF-IDF Vectorization**: Captures semantic signals from job titles.
6. **Model Training**: Trains LambdaRank using user groups and evaluates using NDCG@10.
7. **Recommendation**: Combines IBCF and LTR to generate final job rankings for a user.

## 🔍 Example Usage

```python
final_recommendations, candidates = generate_hybrid_recommendations_final(
    user_id=12345,
    ranker_model=ranker,
    ibcf_candidates_func=generate_candidates_ibcf,
    user_applied_jobs_map=user_applied_jobs,
    job_features_df=job_features,
    user_profiles_df=user_profiles,
    vectorizer_model=vectorizer,
    feature_cols_list=feature_cols,
)
```

## 📊 Visualization

- Displays top 30 most important features from LightGBM model.

## ✅ Results

The hybrid recommendation model successfully ranks job recommendations by:
- Matching user preferences
- Considering historical behavior
- Leveraging content similarity and collaborative filtering

## 📎 Credits

- Developed using data from `ltr-quera.csv`.
- Title normalization and NLP logic includes Persian-language preprocessing.

## 📄 License

This project is licensed under the MIT License.
