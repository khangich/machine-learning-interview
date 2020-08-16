# ML system design usecases
* I'm updating this section, if you're interested click on Watch button or send me an email to helpreparemle@gmail.com. 
* List of ML system design\

## Ad Click Prediction in social network. 
* Build a machine learning model to predict if an Ads will be click. For simplicity reason, 
we will not focus about cascade of classifiers that is commonly used in adtech. 

* Background how Adtech bidding works

![Score distribution](images/ad_bidding.png)

1. Requirements
* ML model with good performance. 
* System can scale to larger number of users with low latency. 
* Imbalance data: you can assume CTR is very small in practice (1%-2%). 
* Serving: from the RTB worfklow diagram, it's important to have low latency (150 ms) for ad prediction. 


2. Calculate and estimation
* Data: historical ad clicks data which store combination of (user, ads. click_or_not). Assume 4K ads requests per second. Within 1 month, there will be 10 billions ads requests.
* Features: several hundreds thousands modalities
* Train/validation data split:  We split train/validation to simulate the actual online system. 
* Serving: 1M model predictions per second.
* Training: ability to retrain many times within one day.


3. Metrics evaluation
* During training phase, we can focus on machine learning metrics instead of revenue metrics or CTR metrics. Regarding revenue-related metric, we usually monitor during deployment and it's out of scope. 
* Normalized Cross Entropy: predictive log loss divided by the cross entropy of the background CTR. One benefit is to have NCE insensitive to background CTR. 

![Score distribution](images/nce.png)

* Calibrationn measured by the expected clicks vs the actual observed clicks. Read more about calibration [here](https://arxiv.org/pdf/1706.04599.pdf)

4. Modelling: features scaling, major sub-sambling. 
* Model: We can use probablistic sparse linear classifier (logistic regression). It's popular because of the computation efficiency and sparsity features.
* Feature engineering:
    * AdvertiserID: it's easily to have millions of advertisiers. One common way to is to use embedding as a distributed representation for advitiserID. If you're not familiar with [embedding](https://blog.twitter.com/engineering/en_us/topics/insights/2018/embeddingsattwitter.html). Another way is use [feature hashing by Kilian Weinberger](https://arxiv.org/pdf/0902.2206.pdf) to handle large sparse column. Feature hash helps increase speed and reduce memory usage. See video [here](https://www.coursera.org/lecture/machine-learning-applications-big-data/hashing-trick-GswXH). 
    * Numeric columns: pay attention to [feature scaling](https://www.datacamp.com/community/tutorials/preprocessing-in-data-science-part-2-centering-scaling-and-logistic-regression).
* Data processing:
    * One way is to subsampling majority negative class at different sub-sampling ratio. The key here is to keep validation dataset have same distribution as test data set. 
    * Another common way is to use [SMOTE](https://arxiv.org/pdf/1106.1813.pdf).

5. Model evaluation and optimization
* We can use NCE metrics, AUC to choose the best model. 
* Once we pick the best model we need to calibrate model predictions. 

6. Model deployment and testing

7. Further readings
* [Machine Learning in Adtech](https://www.slideshare.net/databricks/machine-learning-for-adtech-in-action-with-cyrille-dubarry-and-han-ju)
* [Ad Click Prediction: a View from the trenches](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/41159.pdf)
* [Practical lessons from Predicting Clicks on Ads at Facebook](https://research.fb.com/wp-content/uploads/2016/11/practical-lessons-from-predicting-clicks-on-ads-at-facebook.pdf)
* [Predictive Model Performance: Offline and Online Evaluation](http://chbrown.github.io/kdd-2013-usb/kdd/p1294.pdf)
* [Kaggle CTR prediction](https://www.kaggle.com/c/avazu-ctr-prediction/overview)