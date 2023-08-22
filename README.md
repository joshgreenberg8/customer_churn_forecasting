# customer_churn_forecasting

A project in which I developed and tuned a model using customer data to predict churn for retention offer targeting. The final model exceeded the target metric with a 0.93 ROC-AUC score against the test set (target score 0.88).

I faced challenges with making decisions about features to add and remove, and how to handle potential data leaks with customer begin/end dates while preserving the valuable information. I am happy with my decision to remove the dates after calculating customer account age as an additional feature.

I had difficulty with my models overfitting during grid search, but my project leader pointed out the likely effect that upsampled data was having on my cross validation folds. This was resolved by the implementation of a pipeline process to resample the data for each fold.

By carefully handling my data, identifying trends with EDA, and following good practices with splitting, sampling, and model training, I was able to create a model of high enough quality to exceed the goal of a target metric above 0.88 against a test set.

The LGBM Classifier performed the best in this analysis, slightly outperforming the CatBoost Classifier. It is not surprising that these boosted models outperformed the Logistic Regression and Random Forest models.

The boosted models' quality might be improved with more iterations or higher depth, as evidenced by the highest settings we tried for these parameters were giving the best scores.
