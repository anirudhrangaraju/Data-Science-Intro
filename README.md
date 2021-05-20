# Predictive and Text Aanlytics Intro

## Table of contents
* [Algorithms](#algorithms)
* [ML Life Cycle](#ml-life-cycle)
* [Additional Information](#additional-information)
* [Appendix](#appendix)

Handbook can be viewed here. https://github.com/anirudhrangaraju/Data-Science-Intro/blob/main/handbook.md

## Algorithms

<h5>ML Regression Algorithm:</h5>

* `Linear Regression`

<h5>ML Classification Algorithm:</h5>

* `Logistics Regression(Aka MaxEnt)`
* `Decision Tree`
* `Random Forest`
* `Extra Trees`
* `Boost Variants(XGBoost, Sklearn modified xgboost, CatBoost,LightBoost,ADABoost)`
* `K-Nearest Neighbor(K-NN)`
* `7. Naive Bayes`
* `SVM(Support Vector Machines)`

<h5>ML Cluster Algorithm:</h5>

* `K-Means Clustering`

<h5> Deep Learning Algorithm </h5>

* Tensorflow
* Keras(backend with tensorflow, CNTK, Theano)

<h5> Time Series Algorithm </h5>

* ARIMA<br>
<u>Note:</u> <br>
Algorithms like Decision Tree, Random Forest, Naïve Bayes can be used for regression problem as well. However the accuracy differs based on the data set.

## ML Life Cycle

##################################################################################################<br>
Data Acquisition -->Data Pre-Processing -->Data Analysis --> Data Split --> Model Building --> Model Evaluation --> Model Retrain --> Model Deployment<br>
##################################################################################################<br>
<h5>Step1: Data Acquisition</h5>

    1. The data can be stream data/ loaded in the form of csv file. how to load? : https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html
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
    1. ngrams(bigrams,trigrams)[9]
    2. Stemming and Lemmatization [10]
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

    1. Precision[11]
    2. Recall[11]
    3. F1-Score(Macro,Micro,Average Weighted)[11]
    4. AUC(ROC Curve)[11]
    5. Lift/Gain[11]
    6. KS Metrics[11]
    7. Log Loss/brier loss(Note: Log Loss and AUC are inversly proportional)[11]

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
 
 
 <b>Note:</b>
 More info on the scenerios like the below can be found in https://github.com/anirudhrangaraju/Data-Science-Intro/blob/main/Data%20Analysis/basic_datascience_info.xlsx
 * How to Choose the Algorithm ?
 * How to Choose the Metrics for Predictive/Text Analytics
 * various Feature Engineering techniques for Predictive/text Analytics


## Additional Information
1. How to know the statistical info about data such as min/max/percentile(p10/p30/p90) ?
2. What is Drift Detection and how to Identify ?
3. How can we build the model using External Services without building the model in python
4. How to handle the infrastructure limitations to stoe large volume of predictors

If Intereseted, please visit the link: 

## Appendix
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
 [9]ngrams:https://medium.com/@phylypo/nlp-text-segmentation-with-ngram-b5506dbb514c</br>
 [10]Stemming: https://medium.com/@tusharsri/nlp-a-quick-guide-to-stemming-60f1ca5db49e#:~:text=Stemming%20is%20basically%20removing%20the%20suffix%20from%20a%20word%20and,word%20from%20original%20stem%20word.</br>
 [10]Lemma: https://nlp.stanford.edu/IR-book/html/htmledition/stemming-and-lemmatization-1.html</br>
 [11]Evaluation Metrics: https://neptune.ai/blog/evaluation-metrics-binary-classification<br>
