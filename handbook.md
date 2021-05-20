Details regarding choice of ML Algorithm, Feature Engeneering techniques and metrics can be found below

```diff
@@ Choice of ML Algorithm @@
```

| Domain | Application | Type of ML Task | Input Data Type | Output Data Type | Choice of ML Algorithm | Notes
| --- | --- | --- | --- | --- | --- | --- |
| `Predictive Analytics` | Credit Card Fraud Modelling | Regression | continous | binary/multiclass | Sampled XBOOST,Decision Tree | need to handle large volume by sampling techniques
| `Predictive Analytics` | Loan Approval Modelling | Classification | continous,categorical | binary/multiclass | Logistic Regression | Tuning the hyper parameter is not complex
| `Predictive Analytics` | No Show Appointment | Classification | continous | binary/multiclass | Decision Tree,Logistic Regression
| `Predictive Analytics` | Employee Attrition | Classification | continous,categorical | binary | Decision Tree, Random Forest | Tree based technique would handle effectively
| `Text Analytics` | Topic Detection | Text Classification | text | binary/multiclass | Logistic Regression,Naïve Bayes,SVM | Logistic Regression handles text features effectively
| `Sentiment Analysis` | Sentiment Analysis | Classification | text | miulticlass(pos/neg/neu) | Logistic Regression | Vader sentiment algo  can be used here
| `Big Market Sales App` | Big Market Sales App | Regression | continous,categorical | contnious | Linear Regression | performs good on small dataset
| `Text Analytics` | Author Identification | Text Classification | Text | Multiclass | SVM,Naïve Bayes | Predictive based(word2vec)/Frequency based embedding(tfidf) can be used here

```diff
@@ Predictive Analytics Feature Engeneering Techniques @@
```

| Feature Engeneering Techniques | How ? 
| --- | --- |
| `Missing Value Imputation` | * Mean/Median Imputation <br> * Imputing using most frequent/zero values <br> * KNN Imputer <br> * MICE <br> * Missforest
| `Outlier Detection` | * Box Plot <br> * Scatter Plot <br> * IQR Score <br> * Zscore  
| `Multicollinearity` | * VIF <br> * Scatter Plot <br> * corrplot <br> 
| `Normalization` | * Min-Max Normalization <br> * Z-Score <br> *  single feature scalling <br> 
| `Regularization` | * Min-Max Normalization <br> * L1(Lasso regularization) <br> *  L2(Ridge Regularization) <br> * Elastic Net 
| `Sampling Techniques` | * Up-Sampling(SMOTE Algorithm) <br> * Down-Sampling(NEAR MISS Algorithm) <br> *  Weighted Sampling(Balanced Hyperparameter) <br> 
| `Encoding Techniques` | * One-Hot-Encoding <br> * Label Encoding <br> * Categorical Encoding <br> 

```diff
@@ Text Analytics Feature Engeneering Techniques @@
```

| Feature Engeneering Techniques | How ? |
| --- | --- |
| `Feature Vectorization` | * Count Vectorizer <br> * TF-IDF Transformation <br> * Word2Vec <br> * Doc2Vec <br> * Word2Vec+Tfidf 
| `Stemming Techniques` | * SnowBall Stemmer <br> * Porter Stemmer <br> * Lancaster Stemmer  
| `n grams` | * uni-grams <br> * bi-grams <br> * tri-grams <br> *n-grams 

```diff
@@ Predective Metrics Evaluation @@
```

|Type | Metrics |
| --- | --- |
| `Classification` | * Precision/Recall/F1-Score <br> * AUC <br> * logg loss / brier loss / hamming loss <br> * confusion metrics/classification report <br> * kappa score
| `Regression` | * R2 Score <br> * RMSE

<b>Note: </b> F1-Score can be further viewed as micro,macro and average weighted

More Detailed Metrics can be found here: https://neptune.ai/blog/evaluation-metrics-binary-classification

```diff
@@ Text Metrics Evaluation @@
```

|Type | Metrics |
| --- | --- |
| `Topic Classification` | * Precision <br> * Recall <br> * F1-Score
| `Sentiment Analysis` | * pos/neg/neu
| `Entity` |* Expected <br> * Predicted <br> * F1-Score
