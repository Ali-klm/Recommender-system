
# Restaurant Rating Prediction

This project aims to help Misha recommend the best Russian restaurants to Mosha using a simple linear regression model. The model predicts restaurant ratings based on user personality traits and restaurant characteristics.

## Dataset

The dataset consists of two files located in the `Data` folder:

- `train.csv`: Training data with user ratings and restaurant details.
- `test.csv`: Test data without ratings (target variable) for prediction.

## Files

- `train.csv`: Contains 15,235 rows and 21 columns, including user ID, restaurant info, personality traits, and the rating given by the user.
- `test.csv`: Contains 5,079 rows with the same features except the rating.

## How to run

1. Make sure the `Data` folder with `train.csv` and `test.csv` is in the root directory of the project.
2. Run the notebook or script to:
   - Load and preprocess data (handling categorical variables with One-Hot Encoding).
   - Split training data into train and validation sets.
   - Train a linear regression model.
   - Evaluate the model using R² score.
   - Predict ratings on the test dataset.

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn

## Notes

- The project uses One-Hot Encoding for categorical features to improve prediction accuracy.
- The evaluation metric is R² score, with a threshold of 0.85 for acceptable performance.
