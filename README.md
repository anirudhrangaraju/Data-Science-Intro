# Predictive and Text Aanlytics Intro

<h3>Algorithm</h3>

<b>Regression Algorithm:</b>
* `Linear Regression`

<b>Classification Algorithm:</b>

* `Logistics Regression(Aka MaxEnt)`
* `Decision Tree`
* `Random Forest`
* `Extra Trees`
* `Boost Variants(XGBoost, Sklearn modified xgboost, CatBoost,LightBoost,ADABoost)`
* `K-Nearest Neighbor(K-NN)`
* `7. Naive Bayes`
* `SVM(Support Vector Machines)`

<b>Cluster Algorithm:</b>

* `K-Means Clustering`

<u>Note:</u> <br>
Algorithms like Decision Tree, Random Forest, Naïve Bayes can be used for regression problem as well. However the accuracy differs based on the data set.

<h5>Step1: Data Acquisition</h5>

    1. The data can be stream data/ loaded in the form of csv file 
    2. Dealing with regression, classification(binary/multiclass) and clustering ML Models
    3. Target variable would be numerical/binary/multiclass(no text features)

<h5>Step2: Data Pre-Processing/Feature Engineering</h5>

```diff
@@ Predictive Analytics@@
```
    1. Missing Value Imputation(trivial techniques like mean/median/mode imputation and imputat algo's like MICE/missforest/ANNOVA/AMELIA)[1]
    2. Outlier Detection using boxplot[2]
    3. Multi-Collinear Attributes using (eigen value and eigen vector/ corrplot etc..)[3]
    4. Normalization(all features should be in the same scale to build the model efficiently)[4]
    5. Regularization(L1 Regularization(Lasso)/L2 Regularization(Ridge)/Elastic Regularization(combo of L1 and L2)[5]
    6. Sampling Techniques(Up-Sampling, Down Sampling, Weighted Average Sampling)[6]
    7. Principal Component Analaysi(PCA) for trimming down large features[7]
    8. Data Encoding using one-hot encoding, label encoding[8]


```diff
@@ Text Analytics@@
```
    1. ngrams(bigrams,trigrams)
    2. Stemming and Lemmatization
    3. Stop Words Removal
    4. data compression for large volume data
    5. Frequency Based and Predicton Based Embedding(tfidf vectorization, count vectorization, word2vec, word2vec+tfidf, doc2vec)

<h5>Step3: Data Analysis</h5>

```diff
@@ Predictive Analytics@@
```
    1. Number of Unique levels/predictors(Note: few algo such as missforest supports limited features)
    2. Types of Predictors(numerical,date,categorical,text,image)
    3. Missing Data Points for each features
    4. Distribution of numerical/categorical features in the dataset

```diff
@@ Text Analytics@@
```

    1. Corpus Level Analysis
      1. Topic Spread(Number of Topics and document/ topics)
      2. Word Count(number of words/document with - rare words/most frequent words)
      3. Document Length(Cut off the minimum and maximum document length)

    2. Topic Level Analysis
      1. Sample Distribution/topic
      2. word cloud 
      3. Top Influential words/category

<h5>Step4: Data Split</h5>

    1. Split the data into train/validate and test using random/stratified sampling

<h5>Step5: Model Building</h5>

    1. Build model using different algorithm specified above with different hyperparameters
    2. sample hyper parameters(number of trees(for tree based model), number of features(tree based model), seed, C(cost parameter for logistic regression),
                               number of iterations(for maxent,tree based model,L1/L2 inbuilt hyperparameter)
    3. Model can be build using jupyter notebook and generate a {pkl,joblib,bst} file for model deployment

<h5>Step6: Model Evaluation</h5>

```diff
@@ Predictive Analytics@@
```

    1. Precision[9]
    2. Recall[9]
    3. F1-Score(Macro,Micro,Average Weighted)[9]
    4. AUC(ROC Curve)[9]
    5. Lift/Gain[9]
    6. KS Metrics[9]
    7. Log Loss/brier loss(Note: Log Loss and AUC are inversly proportional)[9]

```diff
@@ Text Analytics@@
```
    1. Precision
    2. Recall
    3. F1-Score(Macro,Micro,Average Weighted)

<h5>Step7: Model Re-train</h5>
     
     Re-Train the model by modifying the data accordingly

<h5>Step8: Model Deployment</h5>

    Model Deployment using Flask/Django and using docker containers
    
 
 Appendix<br>
 [1]Missing Value Imputation: https://towardsdatascience.com/6-different-ways-to-compensate-for-missing-values-data-imputation-with-examples-6022d9ca0779 
 <br>
 [2]Outlier Detection: https://towardsdatascience.com/ways-to-detect-and-remove-the-outliers-404d16608dba 
 <br><
 [3]Multi-Collinearity: 
 <br>
 [4]Normalization:https://towardsdatascience.com/data-normalization-with-python-scikit-learn-e9c5640fed58
 <br>
 [5]Regularization: https://www.analyticsvidhya.com/blog/2017/06/a-comprehensive-guide-for-linear-ridge-and-lasso-regression/
 <br>
 [6]Sampling Techniques: https://analyticsindiamag.com/using-near-miss-algorithm-for-imbalanced-datasets/
 <br>
 [8]Encoding Techniques: https://towardsdatascience.com/categorical-encoding-using-label-encoding-and-one-hot-encoder-911ef77fb5bd
 <br>
 [9]Evaluation Metrics: https://neptune.ai/blog/evaluation-metrics-binary-classification
 <br>
