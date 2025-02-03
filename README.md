📊 Kaggle Playground Series - Season 5, Episode 1


🏆 Sticker Sales Forecasting


🔗 Competition Link -- https://www.kaggle.com/competitions/playground-series-s5e1/data



🚀 Overview

This project is my submission for the Kaggle Playground Series - Season 5, Episode 1 competition. The goal was to predict sticker sales in various countries and stores using historical sales data. The evaluation metric used was Mean Absolute Percentage Error (MAPE).

Final Rank: 2550
Score: 2.95087
Kaggle Profile: Ayushi_Raj




📂 Dataset
The dataset consists of sales data for Kaggle-branded stickers, including:

train.csv: Sales data with date, country, store, product, and num_sold.
test.csv: Data without num_sold, for which predictions were made.
sample_submission.csv: The required format for submission.





🛠 Approach
🔎 Feature Engineering
Date Features: Extracted year, month, day, and day of the week.
Lag Features: Used lag_1 to capture previous day sales trends.
Rolling Statistics: Computed rolling_mean and rolling_median over 7-day windows.
Weekend Effect: Added an is_weekend feature.
One-Hot Encoding: Converted categorical features (country, store, product) into numerical form.


🤖 Models Used
1️⃣ H2O AutoML – Trained multiple models and selected the best-performing one.
2️⃣ XGBoost with Hyperparameter Tuning – Used RandomizedSearchCV for optimizing learning_rate, n_estimators, max_depth, etc.





📈 Model Performance
The best model was XGBoost, achieving an MAE of 104.01 on the validation set.

Feature Importance:
rolling_mean and lag_1 were key predictors.
is_weekend improved the model’s ability to handle seasonality.




📌 Lessons Learned
🔹 Feature engineering played a huge role in improving model performance.
🔹 Hyperparameter tuning with RandomizedSearchCV helped optimize XGBoost.
🔹 Using H2O AutoML provided insights into different model performances.
🔹 Time-series forecasting requires careful handling of date-based trends.




📁 Files in This Repository
📌 notebook.ipynb → Full Kaggle notebook with data preprocessing, model training, and predictions.
📌 train.csv & test.csv & sample_submission.csv → Dataset 
📌 submission.csv → Final predictions file submitted to Kaggle.
📌 README.md → This file with project details.




💡 Future Improvements
✅ Try LSTM/RNN-based models for sequential sales prediction.
✅ Explore feature selection techniques to reduce overfitting.
✅ Implement stacked ensemble models (e.g., blending XGBoost, LightGBM, and CatBoost).
✅ Use time-based cross-validation instead of random splitting.






🔗 Connect with Me
💻 GitHub: https://github.com/ayushiraj02
📊 Kaggle: Ayushi_Raj
