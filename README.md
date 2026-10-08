# MSCS 634 Lab 4 – Regression Analysis with Regularization Techniques

## Purpose of the Lab

The purpose of this lab was to apply and compare different regression techniques using the Diabetes dataset from `sklearn.datasets`. The analysis included Simple Linear Regression, Multiple Regression, Polynomial Regression, Ridge Regression, and Lasso Regression. The models were evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² to determine how well each model predicted disease progression.

## Key Insights from the Regression Analysis

The results showed that Simple Linear Regression using BMI alone had limited predictive performance, with an R² of 0.2333. Multiple Regression performed considerably better, achieving an R² of 0.4526, which showed that using multiple features provided more useful information for predicting disease progression.

Polynomial Regression with degrees 2 through 5 did not consistently improve performance. The polynomial models produced R² values between approximately 0.2023 and 0.2329, showing that increasing model complexity did not necessarily improve predictions on the test data.

Regularization provided the strongest results. Ridge Regression performed best with an alpha value of 0.10, achieving an R² of 0.4609. Lasso Regression also performed best with an alpha value of 0.10 and achieved the highest R² of 0.4719, along with the lowest MSE of 2798.1935 and RMSE of 52.8980 among the models evaluated. Therefore, Lasso Regression with alpha = 0.10 was the best-performing model in this analysis.

The analysis also showed that very large alpha values reduced model performance. This demonstrated that excessive regularization can cause underfitting, while a moderate alpha value can provide a better balance between model complexity and predictive performance.

## Challenges and Decisions

One of the main decisions during the lab was selecting BMI as the single independent variable for Simple Linear Regression so that its performance could be compared with models using multiple features. For Multiple Regression, multiple available features were used to provide a broader prediction of disease progression.

Another decision was to test several polynomial degrees and alpha values rather than relying on a single configuration. This made it possible to observe how increasing polynomial complexity and regularization strength affected model performance. The models were compared using the same MAE, MSE, RMSE, and R² metrics to maintain consistency.

A challenge was determining whether increasing model complexity actually improved generalization. The polynomial results showed that higher complexity did not consistently improve the test results. Similarly, the Ridge and Lasso results showed that very large alpha values substantially reduced performance, so alpha = 0.10 was selected based on the strongest test-set results.

## Conclusion

Overall, the lab demonstrated that choosing an appropriate regression technique and model complexity is important for predictive performance. Multiple Regression improved substantially over Simple Linear Regression, while Polynomial Regression did not provide consistent improvements. Ridge and Lasso regularization produced better results, with Lasso Regression using alpha = 0.10 achieving the strongest overall performance among the models tested.