# House Price Prediction Project

## Overview
This project aims to predict the sale prices of houses based on their features using various regression models. The dataset contains information about various characteristics of houses, such as area, number of bedrooms, quality of materials, and more. The goal is to develop a robust regression model that can accurately predict the sale prices of houses based on these features.

## Project Structure
- Data Preparation and Exploration: The initial phase of the project involves data loading, exploration, and understanding the dataset's features. Basic data analysis and visualization are performed to gain insights into the distribution of the target variable (SalePrice) and other features.
- Data Preprocessing: The dataset is preprocessed to handle missing values, encode categorical features, and deal with skewness in the target variable. Some additional features are also created based on domain knowledge to enhance the model's performance.
- Model Selection and Training: Several regression models are chosen, including LightGBM, XGBoost, Ridge, SVR, Gradient Boosting, and Random Forest. Each model is trained using cross-validation to evaluate its performance.
- Model Blending and Stacking: The predictions from different models are blended together using weighted averaging to create a final ensemble model. Stacking is also applied using a meta-regressor to further improve the model's performance.
- Evaluation: The performance of each individual model, as well as the blended model, is evaluated using Root Mean Squared Logarithmic Error (RMSLE). The model with the lowest RMSLE is selected as the final model for predictions.
- Submission: The final predictions are made on the test dataset using the selected model and saved in a submission file for submission to the competition platform.

## Prerequisites
- Python 3.x
- Jupyter Notebook
- Necessary Python libraries: numpy, pandas, seaborn, matplotlib, scikit-learn, lightgbm, xgboost, mlxtend

## Usage
- Clone the repository to your local machine.
- Install the required Python libraries listed in the Prerequisites section.
- Download the dataset (train.csv and test.csv) and place them in the appropriate directory.
- Open the Jupyter Notebook "code.ipynb" and run each cell to execute the code step-by-step.

## Results
The final submission file "submission_final.csv" contains the predicted sale prices for houses in the test dataset.

## Notes
- The project uses a 12-fold cross-validation to train the models.
- Feature engineering and preprocessing techniques are used to handle missing values, encode categorical features, and deal with skewness.
- The blended model outperforms individual models, achieving a low RMSLE score.
- The 'submission_initial.csv' file contains initial predictions made by the blended model, while the 'submission_final.csv' file contains the improved and scaled predictions after post-processing and outlier adjustments.
