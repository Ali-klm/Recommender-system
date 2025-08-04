# JobRecSys-Persian-quera-karyabi

This project implements a user-based collaborative filtering recommender system for job advertisements using a dataset of job applications from the Quera platform.

## Dataset

The dataset is located in the `Data` folder and named `quera-karyabi.csv`. It contains interactions where users (applicants) apply to job postings.

## Features

- Data preprocessing and filtering to improve quality.
- Creation of a user-item interaction matrix with combined Job ID and Job Title for better interpretability.
- Calculation of Jaccard similarity between users to find similar users.
- A recommendation function that provides the top 10 job ads for a given user based on similar users' interactions.

## Usage

1. Load and preprocess the data from `Data/quera-karyabi.csv`.
2. Build the user-item matrix.
3. Compute user similarity matrix using Jaccard similarity.
4. Use the `recommender_system(user_id)` function to get job recommendations for any user.
5. Save recommendations to CSV files.

## Requirements

- Python 3.x
- pandas
- numpy
- scipy

## How to Run

```bash
# Example: Run recommendation for a specific user
recommendations = recommender_system(3902592.0)
recommendations.to_csv('3902592.csv', index=False)
