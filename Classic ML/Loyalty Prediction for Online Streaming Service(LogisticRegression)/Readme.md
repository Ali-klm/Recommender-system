# Loyalty Prediction for Online Streaming Service

This project aims to predict customer churn (loss of loyalty) for an online streaming platform called **Pardekav**. Using historical user interaction data, the goal is to identify users who are likely to stop using the service based on their activity and subscription patterns. Early detection helps the platform improve recommendations and retain users by offering alternative suggestions.

---

## Dataset

The dataset consists of two CSV files located in the `Data` folder:

- `train.csv`: Contains 4000 rows and 14 columns including user demographics, subscription details, and interaction metrics. It also contains the target column `churned`, indicating whether the user stopped using the service.
- `test.csv`: Contains 1000 rows and similar columns as the training set but **does not** include the target column `churned`.

---

## Features Description

- `customer_id`: Unique identifier for each user
- `age`: Age of the user
- `gender`: Gender of the user
- `subscription_type`: Type of subscription plan
- `watch_hours`: Total hours spent watching content
- `last_login_days`: Days since last login
- `region`: Geographic region of the user
- `device`: Device used for watching
- `monthly_fee`: Monthly subscription fee paid
- `payment_method`: Payment method used
- `number_of_profiles`: Number of profiles under the user account
- `avg_watch_time_per_day`: Average daily watch time in hours
- `favorite_genre`: User's favorite genre of content
- `churned`: Target variable indicating if user churned (only in `train.csv`)

---

## Project Workflow

1. **Data Loading:** Reading the CSV files into pandas DataFrames.
2. **Exploratory Data Analysis (EDA):** Understanding data types, checking missing values, and basic statistics.
3. **Preprocessing:** Handling categorical variables with encoding, scaling numeric features, and ensuring the same transformations on train and test datasets.
4. **Train-Test Split:** Splitting the training data into training and validation sets.
5. **Model Training:** Training a Logistic Regression model to predict churn.
6. **Evaluation:** Using macro F1-score as the main metric for model performance on both training and validation sets.
7. **Prediction:** Predicting churn status for users in the test set.
8. **Output:** Preparing a submission DataFrame with the predicted churn labels.

---

## Usage

Make sure the data files `train.csv` and `test.csv` are placed inside the `Data` directory.

Run the notebook or script to execute all steps from preprocessing to prediction.

---

## Dependencies

- Python 3.x
- pandas
- numpy
- scikit-learn

---

## Contact

For questions or collaboration, feel free to open an issue or contact me.

---

Thank you for checking out this project!
