# Data science project in E-commerce using transactional data for predictive analysis

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

=====Predictive Modeling Project # 1=====

Objective: Build a binary classifier to predict whether a product will be recommended for purchase using exploratory data analysis, feature selection based on importance,binary classification, and then comparing/verifying results with AutoML generated classifier.

Methods: 

Following steps are followed:

   1. EDA

   2. Data pre-processing: selecting input/target features, one-hot encoding

   3. Feature selection: pearson correlation, p-value, LassoCV, feature importance from decision trees

   4. Classifiers:  RandomForest with vs without class weights balanced

   5. Auto-ML for verification

Results: 
1. Feature selection based on importances determined from:

    A. Pearson Correlation: total # of features:36 ,# of features recommended to drop: 6, were these features dropped: yes
  
    B. P-value selection: total # of features: 30, # of features recommended to drop: 22, were these features dropped: yes
  
    C. LASSO feature importance: total # of features: 8, # of features recommended to drop:4, were these features dropped: no
  
2. Random Forest Classifier without balancing class weights:

          Accuracy = 0.9332954868010218, Precision = 0.9870485224370668, Recall = 0.9313253012048193, F1-score = 0.9583776124690045
          Confusion Matrix is:
            [[1165   71]
            [ 399 5411]]
            
3. Random Forest Classifier with class weights balanced:

         Accuracy = 0.9332954868010218, Mean Recall = 0.932, Mean F1 Score = 0.958
         Confusion Matrix is:
         [[1165   71]
        [ 399 5411]]
        
4. TPOT for classification: Bernoulli Naive-Bayes Classifier with beset internal CV score: 93%

         Accuracy = 0.5141924496168039, Precision = 0.842467718794835, Recall = 0.5053356282271945, F1-score = 0.6317374932759547
         Confusion Matrix is:
          [[ 687  549]
          [2874 2936]]
 
Conclusions:

Random Forest Classifier predicts with 93% accuracy that the customer would make a recommendation for purchase. The prediction with AutoML deduced classifier is significantly less accurate.

Next steps:
1. Conduct hyperparameter tuning to improve on the output metrics for the chosen classifer.
2. Add few more metrics for results: Classification report, ROC_AUC curve etc to determine the classifier's performance w.r.t each class.
3. Build multi-class classifier based on Rating.

=====Predictive Modeling Project # 2=====

Objective: Building a Classifier predicting the recommendation through sentiment analysis of customer reviews

Methods: 

Following steps are followed:

   1. EDA

   2. Data pre-processing: selecting input/target features, one-hot encoding
    
   3. Conducting Sentiment Analysis: From reviews predicting the recommendation; TF-IDF algorithm
    
 Results: 
 
    Accuracy = 0.8868861765540732, Precision = 0.8987058635564786, Recall = 0.9718382861091914, F1-score = 0.9338424504025898
    Confusion Matrix is:
    [[ 624  634]
    [ 163 5625]]
    
 Conclusions:

  Logistic Regression Classifier predicts with 89% accuracy that the customer would make a recommendation for purchase based on their reviews. 

 Next steps:
 
1. Conduct hyperparameter tuning to improve on the output metrics for the chosen classifer.
2. Try out other classifer such as SVM, Random Forest etc. and determine the performance/accuracy and do the comparison with the above chosen classifier.
3. Add few more metrics for results: Classification report, ROC_AUC curve etc to determine the classifier's performance w.r.t each class.
4. Use AutoML to determine the best classifier and the resultant output metrics.
 

