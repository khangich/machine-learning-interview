# ML system design usecases [Work in progress]
* I'm updating this section, if you're interested click on Watch button. You can also send me an email helpreparemle@gmail.com. 
* List of ML system design
## Adtech
### Ad Click Prediction in social network. 
* Build a machine learning model to predict if an Ads will be click. In adtech stack, it's common to have a cascade of classifiers of increasing computational cost to handle with l;arge volumne of ads candidate. For this excercise, 
the last stage click prediction model of a cascade classifier, that is the model that produces predictions for the final set of candidate ads.

1. Requirements
* ML model need to be able to recommend ads with high likelyhood of click. 

2. Non-functional requirements
* Imbalance data: you can assume CTR is very small in practice (1%-2%) hence the available labels will be extremely imbalance.
* Serving: low latency 150 ms for recommending ads. 
* Ability to retrain model many times during the day. 
* Datafreshness: online social network users behaviour are unpredictable and fast changing especially for trending topics. Therefore datafreshness plays an important role in model performance. 

3. Identify data
* We can start with historical ad clicks data which store combination of (user, ads. click_or_not). For model to be well generalize we pick training data that have similar distribution with real data. We split train/validation to simulate the actual online system. 

4. Metrics evaluation
* For this exercise we can assume we want to improve model performance. Therefore we focus on machine learning metrics instead of revenue metrics or CTR metrics. 
* Normalized Cross Entropy: predictive log loss divided by the cross entropy of the background CTR. One benefit is to have NCE insensitive to background CTR. 
* Calibrationn measured by the expected clicks vs the actual observed clicks. 

5. Modelling: features scaling, major sub-sambling. 
* We can use probablistic sparse linear classifier (logistic regression). It's popular because of the computation efficiency and sparsity features.
* Feature engineering:
    * AdvertiserID: it's easily to have millions of advertisiers. One common way to is to use embedding as a distributed representation for advitiserID. If you're not familiar with [embedding](https://blog.twitter.com/engineering/en_us/topics/insights/2018/embeddingsattwitter.html). Another way is use [feature hashing by Kilian Weinberger](https://arxiv.org/pdf/0902.2206.pdf) to handle large sparse column. Feature hash helps increase speed and reduce memory usage. See video [here](https://www.coursera.org/lecture/machine-learning-applications-big-data/hashing-trick-GswXH). 
    * Numeric columns: pay attention to [feature scaling](https://www.datacamp.com/community/tutorials/preprocessing-in-data-science-part-2-centering-scaling-and-logistic-regression).
* Data processing:
    * One way is to subsampling majority negative class at different sub-sampling ratio. The key here is to keep validation dataset have same distribution as test data set. 
    * Another common way is to use [SMOTE](https://arxiv.org/pdf/1106.1813.pdf).

6. Model evaluation and optimization
* We can use NCE metrics, AUC to choose the best model. 
* Once we pick the best model we need to calibrate model predictions. 

7. Further readings
* [Machine Learning in Adtech](https://www.slideshare.net/databricks/machine-learning-for-adtech-in-action-with-cyrille-dubarry-and-han-ju)
* [Ad Click Prediction: a View from the trenches](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/41159.pdf)