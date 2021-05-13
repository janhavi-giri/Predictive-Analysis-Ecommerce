Kaggle dataset problem:
E-commerce : Transactional data for predictive analysis: To build predictive models on online shopping portal data streams

Data sets:  https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews
Contains: 23486 rows and 10 feature variables where each row corresponds to a customer review. 
The 10 feature variables are:
1. Clothing ID: Integer/Categorical variable
2. Age: Positive integer variable of the reviewer’s age
3. Title: String for review title
4. Review Text: String variable for review body
5. Rating: Positive integer, 1 worst to 5 best
6. Recommended IND: Binary, 1 recommended, 0 not recommended
7. Positive Feedback Count: Positive integer of # of customers who found the review helpful
8. Division Name: Categorical name of the product high level division
9. Department Name: Categorical name of the product department name.
10. Class Name: Categorical name of the product class name.

=====

Objective#1: Build a binary classifier to predict whether a product will be recommended for purchase

Methods: 

Following steps are followed:

#1: EDA

#2: Data pre-processing: selecting input/target features, one-hot encoding

#3: Feature selection: pearson correlation, p-value, LassoCV, feature importance from decision trees

#4: Classifiers: Linear (LogisticRegression, LinearSVM), Non-linear (KernelSVM, RandomForest)

#5: Hyper-parameter tuning

#6: Auto-ML for verification

Results: Metrics(Confusion matrix, precision/recall for each class, roc_auc)

Conclusions

Next steps

