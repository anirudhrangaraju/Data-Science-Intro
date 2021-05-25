
## Table of contents
* [Drift Detection](#drift-detection)
* [External Services Model](#external-services-model)
* [PDF Data Extraction](#pdf-data-extraction)
* [Additional Concepts](#additional-concepts)


## Drift Detection

Change in the input/output data over a period of time which affects the model can be considered as drift detection

<h5>How to Identify Drift Detection ?</h5>

1. Model Based Approach(Sliding Window Technique)
   * Adwin
   * Hoeffding Inequality

2. Statisitical Based Approach(Fixed Window Technique)
   * KL(Kullback Leibler) Divergence
   * JS(Jensen Shannon) Divergence
   * KS(Kolmogorov-Smirnov) Test
   * Chi-Square

<h5> Statistical Approach Details </h5>

| Statistical Test | Analysis |
| --- | --- |
|`Kullback Leibler`| * not normalized.<br><br> * scores doesn't have boundaries and it hence it is difficult to identify the most deviated distribution.<br><br> <b>Source:</b>https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.entropy.html 
|`Jensen Shannon`| * normalized version of KL Divergence. <br><br> * requires probability vector to compare the distribution.<br><br> <b>Source:</b> https://docs.scipy.org/doc/scipy/reference/generated/scipy.spatial.distance.jensenshannon.html
|`Kolmogorov-Smirnov`| * measures the distance between the continous distribution of data <br><br> <b>Source:</b> https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ks_2samp.html
|`Chi- Square`| * effective for categorical and not continuous variables.<br><br> * invalid when the reference and target frequencies in each distributions are too small. <br><br> <b>Source:</b>https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.chisquare.html


## External Services Model
We can build the ML/DL model using external services instead of in-house model(training/validating using python scripts)
  
<h5> External Services Support: </h5>

1. Predicitive Analytics
   * Amazon Sage Maker
   * Amazon Sage Maker Autopilot
   * GCP
   * Azure ML Studio
   * H20

2. Text Analytics
   * Amazon Comprehend
   * Google Auto ML
   * Google Cloud Natural Langauge
   * Microsoft Luis
   * H2O

## PDF Data Extraction
 
* Machine Learning Algorithms:
 
Tabular Data Extraction | Text Data Extraction | Image Data Extraction
| --- | --- | --- | 
| * camelot(stable) <br> * Tabula(stable) | * pypdf2(stable and widely used) <br> * pdfplumber(stable and widely Used) <br> * pdfminer(stable and widely Used) <br> * fitz(Unstable) <br> * slate(Unstable) <br> * pdftotree(unstable) <br> * invoice2data(template based) | * tesaract <br> * Flexy Abby Capture and Layout | 

* Deep Learning Algorithms

| Tabular Data Extraction |
| --- | 
| DeepDeSRT |
| TableNet |

<b>Notes</b>
Please find the suporting documents below:

| Library | Documentation |
| --- | --- |
| pdfplumber | https://github.com/jsvine/pdfplumber |
| pypdf2 | https://pythonhosted.org/PyPDF2/index.html |
| tabula | https://tabula-py.readthedocs.io/en/latest/tabula.html <br> https://tabula-py.readthedocs.io/en/latest/ |
| pdfminer and fitz | https://pdfminer-docs.readthedocs.io/programming.html | 
| pdftotree | https://github.com/HazyResearch/pdftotree |
| invoice2data | https://pypi.org/project/invoice2data/ |


## Additional Concepts

Additional Key Concepts to be covered:
1. How to handle the infrastructure limitations to stoe large volume of predictors
2. Set up Flas, Docker Container and Deploying ML Model in Heroku
3. Calcualte statistical Analysis(min/max/percentile(p10/p30/p90)
4. How does Text Recommendation works, and the implementation using algo such as (IBCF)
5. Example for CNN, RNN, Tensorfloe, Keras
6. What is Fuzzy Logic and how does it help in the real world
7. Explain Time Series Slgorithm
8. Neural Netrwork Achitecture
9. Image classificationa and Recognition using OpenCV, Pre-trained Model(Inception, VGGNet, DenseNet, Retinanet)
10. What is Word2Vec,Doc2Vec, Word2Vec + Tfidf. Explaination with example
11. Voice Pricessing(Voice to text)




