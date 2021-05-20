

<b> Drift Detection </b>

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

| Statistical Test | Analysis |
| --- | --- |
|`Kullback Leibler`| * not normalized.<br><br> * scores doesn't have boundaries and it hence it is difficult to identify the most deviated distribution.<br><br> <b>Source:</b>https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.entropy.html 
|`Jensen Shannon`| * normalized version of KL Divergence. <br><br> * requires probability vector to compare the distribution.<br><br> <b>Source:</b> https://docs.scipy.org/doc/scipy/reference/generated/scipy.spatial.distance.jensenshannon.html
|`Kolmogorov-Smirnov`| * measures the distance between the continous distribution of data <br><br> <b>Source:</b> https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ks_2samp.html
|`Chi- Square`| * effective for categorical and not continuous variables.<br><br> * invalid when the reference and target frequencies in each distributions are too small. <br><br> <b>Source:</b>https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.chisquare.html


<b> External Services Model</b>
We can build the model using external services instead of in-house model(training/validating using python scripts)
  
External Services:
  1. Amazon(Amazon Sage Maker, Amazon Comprehend)<br>
  2. Google(Google Auto ML, Google Cloud Natural Langauge,  GCP)<br>
  3. Microsoft(Microsoft ML Studio, Microsoft Luis)<br>
  4. H2O<br>
  
How to handle the infrastructure limitations to stoe large volume of predictors

How to know the statistical info about data such as min/max/percentile(p10/p30/p90) ?


