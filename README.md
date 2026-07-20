# MSCS634_Lab_4

# Regression Analysis with Regularization Techniques

## Lab Overview

This lab explores and compares several regression techniques using the Diabetes dataset from the scikit-learn library. The primary objective is to understand how different regression models perform when predicting a continuous target variable and to evaluate the effects of model complexity and regularization on prediction accuracy.

Throughout the lab, five regression algorithms were implemented and analyzed:

- Simple Linear Regression
- Multiple Linear Regression
- Polynomial Regression
- Ridge Regression
- Lasso Regression

Each model was trained and evaluated using the same training and testing datasets to ensure a fair comparison. Performance was measured using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and the Coefficient of Determination (R²). Visualizations were also created to compare predictions and demonstrate concepts such as underfitting, overfitting, and regularization.

---

## Dataset

The Diabetes dataset provided by scikit-learn was used for this lab. The dataset contains 442 patient records with ten standardized medical predictor variables, including age, body mass index (BMI), blood pressure, and several blood serum measurements. The target variable represents a quantitative measure of diabetes disease progression one year after baseline.

Because the dataset is clean and well-structured, no additional data cleaning was required before model development.

---

## Purpose of the Lab

The purpose of this lab was to gain practical experience implementing and evaluating regression algorithms while understanding the strengths and limitations of different modeling approaches. Specific objectives included:

- Building a Simple Linear Regression model using a single predictor.
- Developing a Multiple Linear Regression model using all available features.
- Exploring Polynomial Regression to study the effects of increased model complexity.
- Implementing Ridge and Lasso Regression to understand regularization techniques.
- Comparing all models using common regression evaluation metrics.
- Demonstrating how model complexity influences underfitting and overfitting.
- Visualizing predictions to better interpret model performance.

---

## Key Insights from the Regression Analysis

Several important insights were gained throughout this lab:

- **Multiple Linear Regression produced the best overall performance.** Using all ten predictor variables significantly improved prediction accuracy compared to relying on a single feature such as BMI.

- **Simple Linear Regression was limited by using only one independent variable.** Although BMI is correlated with diabetes progression, it could not explain enough variation in the target variable to achieve high predictive accuracy.

- **Polynomial Regression did not improve performance.** Adding polynomial features to BMI increased model complexity without improving prediction accuracy. This demonstrated that increasing complexity does not always lead to better models and may introduce unnecessary variance.

- **Ridge and Lasso Regression produced results very similar to Multiple Linear Regression.** Since the Diabetes dataset contains only ten well-behaved standardized features, the original multiple regression model did not exhibit significant overfitting. Regularization therefore improved model stability without noticeably changing prediction accuracy.

- **Regularization remains an important technique.** Ridge Regression shrinks all coefficients to reduce model complexity, while Lasso Regression can eliminate less important features by shrinking some coefficients to zero. These techniques become especially valuable when working with larger datasets or highly correlated predictors.

- **Evaluation metrics provided a comprehensive comparison.** MAE, MSE, RMSE, and R² each offered different perspectives on model performance, making it easier to compare prediction accuracy across all regression models.

---

## Challenges and Decisions

Several decisions were made during the implementation of this lab to ensure accurate and reliable model evaluation.

- A consistent 80/20 train-test split with a fixed random state was used for every regression model to allow fair comparisons.

- Feature scaling was applied before training the Ridge and Lasso Regression models because regularization methods are sensitive to differences in feature scales.

- Polynomial Regression was implemented using only the BMI feature to demonstrate how increasing polynomial degree affects model complexity, underfitting, and overfitting.

- Polynomial feature transformations were performed after splitting the dataset to avoid data leakage and ensure that the testing data remained completely unseen during model training.

- Multiple evaluation metrics were calculated for every model instead of relying on a single performance measure. This provided a more complete understanding of each model's predictive capabilities.

One challenge encountered during the lab was understanding why more complex models do not always outperform simpler models. Through experimentation with Polynomial Regression and regularization techniques, it became clear that increasing model complexity without meaningful additional information can reduce performance rather than improve it. This reinforced the importance of selecting models based on both predictive accuracy and their ability to generalize to unseen data.

---

## Conclusion

This lab provided valuable experience implementing, evaluating, and comparing multiple regression algorithms using a real-world medical dataset. The results demonstrated that selecting appropriate input features has a greater impact on prediction performance than simply increasing model complexity. The analysis also highlighted the importance of regularization techniques for controlling overfitting and improving model robustness. Overall, the lab strengthened practical understanding of regression modeling, evaluation metrics, feature engineering, and the trade-offs between model simplicity, complexity, and generalization.
