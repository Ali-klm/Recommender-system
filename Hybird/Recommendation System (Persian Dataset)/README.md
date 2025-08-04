# 🔍 GalaxyJob: Hybrid Job Recommendation System (Persian Dataset)

This project implements a **hybrid recommendation system** designed to suggest jobs to users based on a combination of **content-based filtering** and **collaborative filtering** techniques. It works with a real-world Persian-language dataset and includes natural language preprocessing, feature extraction, and filtering based on user preferences.

---

## 📁 Dataset

- **File location:** `data/searching_job.csv`
- **Language:** Persian
- **Key Columns:**
  - `Applicant ID`, `Job ID`, `Seen`
  - `Careers Job - Job → Title`, `Minimum Salary`, `Maximum Salary`, `Hit Count`, etc.

---

## 🚀 Features

- **Text Preprocessing:** Persian title normalization using [Hazm](https://github.com/sobhe/hazm), removal of punctuation, and stopword filtering.
- **Technology & Domain Extraction:** Extracts job-related tech stacks (like Python, JavaScript) and domains (like AI, Frontend) using fuzzy matching.
- **Content-Based Filtering:** Uses TF-IDF vectors to compute similarity between job postings.
- **Collaborative Filtering:** Builds a user-item interaction matrix and computes item-item similarity using cosine similarity.
- **Hybrid Recommendation:** Combines both methods with adjustable weights.
- **Hard Filters:** Enables filtering based on:
  - City preferences
  - Remote job availability
  - Minimum salary
  - Seniority level
- **Cold-Start Handling:** Recommends jobs based on popularity and content similarity for new users.

---

## 🧠 Key Components

- `normalize_title()`: Cleans and standardizes job titles.
- `extract_features_from_title()`: Identifies technologies and job domains from titles.
- `content_based_filtering()`: Returns job similarity based on textual features.
- `collaborative_filtering()`: Computes similarity using user-job interactions.
- `hybrid_recommendation()`: Core function combining both systems with optional user filters.
- `apply_hard_filters()`: Applies rules to narrow down recommendations.

---

## 📊 Sample Output

For a given user (e.g., `user_id = 6003`) and various weights of content-based vs collaborative filtering, the system prints the top 5 job recommendations.

---

## 🛠️ Dependencies

Ensure the following packages are installed:

```bash
pip install pandas numpy hazm fuzzywuzzy scikit-learn nltk beautifulsoup4
```

You will also need to download some NLTK resources:

```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```

---

## 📌 How to Run

1. Clone the repository
2. Place the CSV file in the correct path: `data/searching_job.csv`
3. Run the Jupyter notebook or `.py` script
4. Adjust the user ID and weights as needed in the final section

---

## 📚 Future Improvements

- Web-based dashboard or API interface
- Integration with real-time job platforms
- Better handling of multilingual content
- More robust user profiling

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).