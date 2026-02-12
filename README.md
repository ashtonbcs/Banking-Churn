# Banking-Churn
TECH STACK:
Python, scikit-learn, Pandas, Matplotlib, imbalance

This model consists of a multivariate classification model to predict bank member churn.
I tried Logistic Regression, Random Forest, XGBoost, and Linear Support Vector Classification.
Overall Random Forest and XBoost were the best and the same in terms of performance.
Logistic Regression perfomed poorly, 91% of the members predicted to stay did and 43% of members predicted to exit did so.
Linear Support Vector Classification was not that far ahead.
I beleive that XGBoost was a little aggressive, there were no deep interactions between features and the data set was fairly clean.
More importantly between each algorithm used the F1 score was pretty imbalanced. I improved it a little bringing it up to 0.91 for those who stayed and 0.61 for those that exited.
I tried multiple ways to fix this imbalance issue, first i tried under sampling which dropped the scores all around. I then tried over sampling for the minority which balanced out the counts but the F1 score barely budged.
I tried feature selection and feature engineering but the model scores would not improve. 
I came to a realization that at this point no amount of tuning could improve this model. The lack of performance stemmed from the features itself.
The features are not predictive enough for the the exit class.
