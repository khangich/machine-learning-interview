# Machine Learning Interview Preparation (MLIP)
## Intro
* Problem: ML engineer interview has a wide range of technical areas i.e big data, ML fundamental, Deep Learning fundamentals, Leetcode etc. Trying to study everything within short time is a bad strategy. I have only one goal: save your time, prepare interview effectively. I've been helping around 50 people to prepare for MLE interview. Now I want to do it at scale.

* Solution: provide a **minimum** set of focus area which covers all interview questions. I have interviewed at a lot of big companies (FAAG, MS, SnapChat, StitchFix, Intuit etc). I will not shared interview questions because of NDA. 

## How to prepare for interview? 
1. Before you prepare for interiview, you can read [common questions](faqs.md). 
2. What should I study? Use the [study guide](README.md) as a collections of focused areas. 
3. Am I ready for interview? Use [readyness tests](ready.md) to see if you're  ready for interview. 
4. How do I prepare for ML system design? Use [ML usecase](design.md) to go practice actual ML system design usecases. 



## LeetCode
![LC time tracking](https://previews.dropbox.com/p/thumb/AA5UKPqIq0abcCwpsHSnIQFwDCQJvBOGCeivjH4WFAQve0y3NmTRpzwJsTsNr3GbZR0_EDrx8Am3LPz-mMHdQbwKmPfyZ4Qx4p-etJkDwwN_ZMS5ABX_xva5esf9j5dSRvDHG_dL80jrKGAafVtnllZSaVuwCsprT0lucYM2FdKFZtr4sBKtji3kuYay_3OnsAVQ_S-CfI7_lihmdcMWvC19iHMEMk2wm-EbMU-jsq8vhPq2t7QeVJrLAEkuo9ceRpres-qgNfGH5YSEY6mqutUUlXOzW5bSV5eYSo3X-AumO2IqeuILPs8NDBR4uScBNh6ETQQczhnLEwllhzAKMvbUMksnj5hKDkwtzbjU2hy3Jw/p.png?fv_content=true&size_mode=5)

 I use this [LC time tracking](https://docs.google.com/spreadsheets/d/1RCb1dVQCLmtOGlJ5J-NJ5pIC7Tda-N2U/edit#gid=274831950) to keep track how many times and how long I spent each time for each question. Once I finish non-trivial medium LC question 3 times, I have absolutely no issue to solve them in the actual interview sometime within 8-10 minutes. It makes a big difference.

### Tree
* [Ser/deser tree](https://leetcode.com/problems/serialize-and-deserialize-n-ary-tree/)

* [Distributed coins in tree](https://leetcode.com/problems/distribute-coins-in-binary-tree/)

### Recursive/Graph/DP
* [Course schedule ii](https://leetcode.com/problems/course-schedule-ii/)
* [Rotting oranges](https://leetcode.com/problems/rotting-oranges/)
* [Maximum depth of tree](https://leetcode.com/problems/maximum-depth-of-n-ary-tree/)
* [Maximum differences between node and ancestor](https://leetcode.com/problems/maximum-difference-between-node-and-ancestor/)
* [Lowest common ancestor in binary tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree)
* [Critical connections](https://leetcode.com/problems/critical-connections-in-a-network)
* [Task scheduler](https://leetcode.com/problems/task-scheduler/)
* [Coin change](https://leetcode.com/problems/coin-change/submissions/)
* [Word break ii](https://leetcode.com/problems/word-break-ii/)
* [Word search ii](https://leetcode.com/problems/word-search-ii/)
* [Combination sum iv](https://leetcode.com/problems/combination-sum-iv/)
* [Frog jump](https://leetcode.com/problems/frog-jump/)
* [Number of islands](https://leetcode.com/problems/number-of-distinct-islands)
* [Permutations](https://leetcode.com/problems/permutations)
* [Subset ii](https://leetcode.com/problems/subsets-ii/submissions/)
## BST
* [Divide two integers](https://leetcode.com/problems/divide-two-integers/submissions/)
* [Find in sorted array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array)
* [Search in rotated array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
### LinkedList
* [Copy list with random pointer](https://leetcode.com/problems/copy-list-with-random-pointer/)
### Design
* [LRU cache](https://leetcode.com/problems/lru-cache/solution/)

## SQL
* Know SQL join: inner, left, right etc. 
* Cumulative sum of top 10 most profitable products of the last 6 months for customers in Seattle. select product, sum(quantity*price) total from transactions where datediff(transaction_dt, CURDATE()) <= 6*3 group by product order by total desc limit 1
* [Self join](https://www.sqlservertutorial.net/sql-server-basics/sql-server-self-join/)

## Programming
* [Python pass-by-object-reference](https://robertheaton.com/2014/02/09/pythons-pass-by-object-reference-as-explained-by-philip-k-dick/)
* [Python GIL](https://realpython.com/python-gil/)
* [Python multithread](https://realpython.com/intro-to-python-threading/)
* [Python concurrency](https://realpython.com/python-concurrency/)

## Statistics and probability
* Let A and B be events on the same sample space, with P (A) = 0.6 and P (B) = 0.7. Can these two events be disjoint?
Alice has 2 kids and one of them is a girl. What is the probability that the other child is also a girl? 
A group of 60 students is randomly split into 3 classes of equal size. All partitions are equally likely. Jack and Jill are two students belonging to that group. What is the probability that Jack and Jill will end up in the same class? 
* Assume we have a bag with 6 coins in it. 5 coins are fair, and 1 coin has heads on both sides. I randomly picked one coin from the bag, tossed it 3 times, and they were all heads. If I toss the coin again, what is the probability that it is still heads?

* Given an unfair coin with the probability of heads not equal to .5. What algorithm could you use to create a list of random 1s and 0s.  
Some [exercise in Bayesian](https://blogs.kent.ac.uk/jonw/files/2015/04/Puza2005.pdf)

## Big data
* Spark [architecture](http://datastrophic.io/core-concepts-architecture-and-internals-of-apache-spark/)
* Spark [lessons learned](https://databricks.com/blog/2016/08/31/apache-spark-scale-a-60-tb-production-use-case.html) (outdated since Spark 3.0 release)  
* Spark [OOM](https://stackoverflow.com/questions/21138751/spark-java-lang-outofmemoryerror-java-heap-space)
* Cassandra [best practice](https://tech.ebayinc.com/engineering/cassandra-data-modeling-best-practices-part-1/) and [here](https://cassandra.apache.org/doc/latest/data_modeling/intro.html)


## ML fundamentals
* [Collinearity](https://statisticsbyjim.com/regression/multicollinearity-in-regression-analysis/) and [read more](https://www.youtube.com/watch?v=Cba9LJ9lS8s)
* [Random forest vs GBDT](http://fastml.com/what-is-better-gradient-boosted-trees-or-random-forest/)
* [Synthetic method for unbalanced data](https://www.jair.org/index.php/jair/article/download/10302/24590)
* [Compare discriminative vs generative model](https://medium.com/@mlengineer/generative-and-discriminative-models-af5637a66a3) and [extra read](http://ai.stanford.edu/~ang/papers/nips01-discriminativegenerative.pdf)
* [Logistic regression](https://www.youtube.com/watch?v=-la3q9d7AKQ). Try to implement logistic regression from scratch. Bonus point for vecrtorize version in numpy and complete in 20 minutes. Followup with MapReduce version. 
* [Quantile regression](https://www.youtube.com/watch?v=s203ScTy4xQ&t=954s)
* [L1/L2 intuition](https://www.linkedin.com/pulse/intuitive-visual-explanation-differences-between-l1-l2-xiaoli-chen/)

* [Decision tree and Random Forest fundamental](https://people.csail.mit.edu/dsontag/courses/ml16/slides/lecture11.pdf)
* [Explain boosting](https://web.stanford.edu/~hastie/TALKS/boost.pdf)
* [Explain gradient boosting](https://www.youtube.com/watch?v=wPqtzj5VZus)
* [Least Square as Maximum Likelihood Estimator](https://www.youtube.com/watch?v=_-Gnu498s3o)
* [Maximum Likelihood Estimator introduction](https://www.youtube.com/watch?v=jpHreXjtw1Q)
* [Kmeans](https://stanford.edu/~cpiech/cs221/handouts/kmeans.html). Try to implement Kmeans from scratch. Bonus point for vecrtorize version in numpy and complete in 20 minutes. Followup with worst case time complexity and improvement for initialization. 

Extra
* [Sampling techniques](https://towardsdatascience.com/sampling-techniques-a4e34111d808)
* [Partial residual plot](https://en.wikipedia.org/wiki/Partial_residual_plot)
* [SMOTE synthetic minority over-sampling technique](https://arxiv.org/pdf/1106.1813.pdf)
* [SVM tuning](https://www.hackerearth.com/blog/developers/simple-tutorial-svm-parameter-tuning-python-r/)

* [kmeans initialization](https://www.coursera.org/lecture/cluster-analysis/3-3-initialization-of-k-means-clustering-bPyBl)
* [Compare GINI index and Information Gain](https://www.unine.ch/files/live/sites/imi/files/shared/documents/papers/Gini_index_fulltext.pdf)
* [Explain tf-idf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.97.7340&rep=rep1&type=pdf)
* [Understanding L-BFGS](https://aria42.com/blog/2014/12/understanding-lbfgs)
* [Optimizer Quasi newton method](http://www.seas.ucla.edu/~vandenbe/236C/lectures/qnewton.pdf)


## DL fundamentals
* [The deep learning book](https://www.deeplearningbook.org/). Read [Part ii](https://www.deeplearningbook.org/contents/part_practical.html) and 
* [Machine Learning Yearning](https://d2wvfoqc9gyqzf.cloudfront.net/content/uploads/2018/09/Ng-MLY01-13.pdf). Read from section 5 to section 27.
* [Neural network and backpropagation](http://cs231n.stanford.edu/slides/2020/lecture_4.pdf)
* [Activation functions](https://missinglink.ai/guides/neural-network-concepts/7-types-neural-network-activation-functions-right/)
* [Loss and optimization](http://cs231n.stanford.edu/slides/2020/lecture_3.pdf)
* [Convolution Neural network notes](https://cs231n.github.io/convolutional-networks/)
* [Recurrent Neural Networks](http://cs231n.stanford.edu/slides/2020/lecture_10.pdf)

Extra
* [Calibration in modern neural network](https://arxiv.org/pdf/1706.04599.pdf)
* [Attention model](https://www.youtube.com/watch?v=quoGRI-1l0A&list=RDCMUCcIXc5mJsHVYTZR1maL5l9w&index=2)
* [Word2vec](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)
* [Ilya's thesis](https://www.cs.utoronto.ca/~ilya/pubs/ilya_sutskever_phd_thesis.pdf)


## ML system design
### ML classic paper
* [Technical debt in ML](https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems.pdf)
* [Ad click prediction trend](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/41159.pdf)
* [Rules of ML](https://developers.google.com/machine-learning/guides/rules-of-ml)
* [An Opinionated Guide to ML Research](http://joschu.net/blog/opinionated-guide-ml-research.html). Valueable advices in Personal development section at the bottom.

### ML productions
* [Scaling ML at Uber](https://eng.uber.com/scaling-michelangelo/)
* [DL in production](https://github.com/alirezadir/Production-Level-Deep-Learning)
### Food delivery
* [Uber eats trip optimization](https://eng.uber.com/uber-eats-trip-optimization/)
* [Uber food discovery](https://eng.uber.com/uber-eats-query-understanding/)
* [Personalized sore feed](https://blog.doordash.com/personalized-store-feed-with-vector-embeddings-251ad7a2c09a)
* [Doordash dispatch optimization](https://doordash.engineering/2020/02/28/next-generation-optimization-for-dasher-dispatch-at-doordash/)
* [Postmates estimated delivery time](http://engineering.postmates.com/Estimating-Delivery-Times/)

### Fraud detection (TBD)

### Adtech
* [Delayed feedbacks](https://blog.twitter.com/engineering/en_us/topics/insights/2019/improving-engagement-on-digital-ads-with-delayed-feedback.html)
* [Entity embedding](https://blog.twitter.com/engineering/en_us/topics/insights/2018/embeddingsattwitter.html)
* [Star space, embedding all the things](https://arxiv.org/pdf/1709.03856.pdf)
* [Ad Clicks CTR](https://research.fb.com/wp-content/uploads/2016/11/practical-lessons-from-predicting-clicks-on-ads-at-facebook.pdf)
* [Twitter timeline ranking](https://blog.twitter.com/engineering/en_us/topics/insights/2017/using-deep-learning-at-scale-in-twitters-timelines.html)

### Recommendations:
* [Instagram explore](https://ai.facebook.com/blog/powered-by-ai-instagrams-explore-recommender-system/)
* [TikTok recommendation](https://newsroom.tiktok.com/en-us/how-tiktok-recommends-videos-for-you)


# Provide feedbacks
1. You can create Issue on this repo. 
2. Send ane mail to helppreparemle@gmail.com. 