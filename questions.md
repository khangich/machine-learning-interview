# Yet another questions list

* Why do we need the 8209th questions list on github? The questions here sorted by different area and focus on testing your actual knowledge instead of checking your memorization. 
* How do you pick questions? A good question can distinguish candidate that **understand** ve candidates that **knows** the concept. There are two level of questions: fundamental and advance, depend on your timeline you might want to priortize your learning accordingly. 



| Question | Level |
| ------------- | ------------- |
| Underlying decision tree algorithm, what's the difference between regression and classification? | Fundamental |
| What is the difference between logistic regression vs multilayer perceptron? | Advance |
| [Why L1 sparse?](https://stats.stackexchange.com/questions/45643/why-l1-norm-for-sparse-models) | Advance |
| Why do RNNs have a tendency to suffer from exploding/vanishing gradient?  | Fundamental |
| What is the problem with sigmoid during backprop?  | Advance |
| What is the problem with Relu? Why do we need Leaky Relu?  | Fundamental |
| What are the assumptions of linear/logistic regression?  | Fundamental |
| If some features have strong colinearity does it make model performance worse?  | Fundamental |
| What does the decision boundary of logistic regression look like?  | Fundamental | 
 

 # List 99 ML questions
 ## Basic stats questions
1. What is the normal distribution and its functions?
2. What is the variance?
3. What is stddev?
4. What is exponential distribution?
5. What is the binomial distribution?
6. What is Bernoulli distribution?
7. What is the multinomial distribution?
8. What is the lognormal distribution?
9. What is logistic distribution?
10. P value and test hypothesis.
11. Bias coin, unbiased coin posterior probability. Observe the head, what is the likelihood of
coin bias.
12. What is hypothesis testing? chi-squared test: determine if any statistically significant
difference between expected frequencies and observed frequencies in one or more
categories. More popularly used in medicine.
13. What is the gamma distribution and its functions?
14. Poisson distribution and its function.
15. What is the Central Limit Theorem and why is it important?
16. What is sampling? How many sampling methods do you know?
17. Basic Bayes Theorem. P(A|B) = P(B|A) * P(A) / P(B). Conditional prob and marginal prob
18. What is an example of a data set with a non-Gaussian distribution?
19. Given a generator of unbiased Bernoulli numbers (0 or 1 with p=0.5), create a biased Bernoulli trial generator (generate 0 or 1 with the specified 0 < p < 1)
## Machine Learning fundamentals
20. Explain collinearity: how is it possible to have negative coefficient in glm?
21. Assumptions about linear regression: 3 residual errors follow a normal distribution and
independent with each other, output and input have linear distribution, low collinearity
between input features.
22. Explain the concept of bias vs variance
23. Assumptions about logistic regression?
24. Overfitting how to avoid
25. Type of regularization, which one easier to use: L1 and L2. L1 is easier.
26. What are the different metrics to classify the dataset?
27. explain bagging vs boosting
28. Is random forest bagging or boosting?.
29. how to handle unbalanced data.
30. how do you inspect missing data and when are they important
31. how to compare two regressions.
32. What is k-mean? What is kmean loss function? what kind of distance metric would you choose, what if different features have a different dynamic range Kmeans is an algorithm to group similar data points into the same groups. The loss function used L2 norm: sum
of the square of the distance to the centroid. Similar to the Expectation-Maximization algorithm.
33. general ML questions like generative v.s.
34. What is the difference between type I vs type II error?
35. What is the linear regression? What do the terms p-value, coefficient, and r-squared
value mean? What is the significance of each of these components?
36. What is selection bias? It is the bias introduced by the selection from groups that is not
achieved by randomness.
37. What is regularization? How does it solve bias, variance problems?
38. What is the learning curve tool?
39. What is the meaning of the contour visualization of the cost function in linear regression?
40. Explain logistic regression?
a. Why is the name logistic function?
b. Interpretation of logistic function
i. Why do we need continuous output of the logistics function?
c. What does the decision boundary look like?
d. What kind of normalization is needed?
e. Relationship with cross-entropy
f. What are the other logit families?
41. How does the optimization algorithm work i.e to minimize the cost function?
a. Gradient descent, Conjugate gradient, BFGS, L-BFGS
42. Explain SVM
a. What is the decision boundary?
b. What is a kernel trick?
c. What is the cost function?
d. How to tune hyperparameters to avoid underfit, overfit?
i. kernel choice
ii. c parameter
iii. Math formula
43. Explain the decision tree
a. Why do we need a decision tree?
b. How does it work? How do we split? How do we select which feature to split?
c. What is the meaning of the parameters?
d. What is the cost function? Why do we need that cost function? And in which case
do we need which
e. What does tree pruning mean?
44. explain random forest
a. How does it work?
b. How to tune parameters to avoid underfit/overfit?
c. Is it an ensemble of bagging?
45. Explain boosting
a. Basic intuition
b. When to do it?
c. What problem does it solve?
d. What are the parameters?
e. How to tune?
46. Explain PCA. What is physical intuition?
47. Explain MLP: kind of fully connected feedforward neural network that use sigmoid or tanh as activation functions, widely used for classification task similar to logistic regression.
48. Explain MLE
49. Explain MAP
50. what is cross-validation: the purpose is to estimate how a model performs on unseen data by partition data set into many sets and pick a model with higher
accuracy on the validation set.
51. SVM: how to choose the model and how to determine if a model is better than another
52. Explain how you select the best model?
53. Explain TPE hyperparameter optimization. explain hyper optimization: BayesOptimization
54. pros and cons of random forest and why. Pros: effective, better than tree, effective feature importance. Cons: not easy to interpret, prone to out of range input issue, less
effective with big data or nonsmooth assumption.
55. How GMM works (EM algorithm)
56. When using the Gaussian mixture model, how do you know it is applicable?
57. Describe some criteria for model selection? Why is dimension reduction important?
58. How do you choose the best model among all possible models? explain neural network assumptions of linear regression models if you have a large number of predictors how do you handle them?
59. What is the bias-variance tradeoff? How is XGBoost handling bias-variance tradeoff?
60. How do you find an anomaly in a distribution? How do you investigate that a certain trend in distribution is due to anomaly?
## Deep learning fundamentals
61. Explain all standard activation functions? tanh, relu, leakyRelu, sigmoid, softmax, softplus
62. How does a neural network with one layer and one input and output compare to logistic regression? It’s the same with logistic regression if the NN is using sigmoid function and logistic regression.
63. Explain RNN Problem. How does LSTM help solve it?
## Companies Interview questions:
64. Netflix question – When you split a population for A/B testing, what are some reasons you could see a significant difference in the control and variant groups?
65. Google question – Find the width of the confidence interval
66. Facebook question – If you draw 2 cards from a shuffled 52 card deck, what is the probability that you’ll have a pair?
67. Microsoft question – Generate 7 integers with equal probability from a function which returns 1/0 with probability p and (1-p).
68. Given an unfair coin with the probability of heads not equal to .5, what algorithm could
you use to create a list of random 1s and 0s?
69. Groupon question – You are on a number line and you can jump to one of the neighboring points with equal probability, with the exception of n=0 where you can’t go to negative numbers but have to come back to n=1. If you start at n=44, what is the expected number of steps to reach n=4444?
70. CA Technologies question – How do you design an algorithm for fraud detection?
71. LinkedIn question – Come up with some of the factors that could be used to produce certain algorithms (‘people you may know,’ and an algorithm to discover when a person is starting to search for new job). PYMK: uses many features to calculate a connection probability among two people. Some examples are: companies position overlap (How
many months/years both individuals work together at same company,  similar/related
field), school education overlap, strong unconnected people in LinkedIn connection graph. (both individuals have many common friends) etc.
72. An important metric goes down, how would you dig into the causes?
73. Amazon question – Estimate the cumulative sum of the top 10 most profitable products
of the last 6 months for customers in Seattle.
74. Booking question – How can we automatically propose ‘good value deals’ to customers,
including hotels that don’t have a rating yet?
75. If you have a customer and want to decide whether they will “buy today” or “not buy
today” and you know 1. where they live, 2. their income, 3. their gender, 4. their
profession, how would you define a machine-learning algorithm to figure this out?
76. LinkedIn question – How would you design an A/B test for the homepage?
77. Netflix question – Given a month’s worth of login data from Netflix such as account_id,
device_id, and metadata concerning payments, how would you detect fraud? (identity
theft, payment fraud, etc.)
78. Booking question – How would you tag a listing as value for money? How would you
measure the “value”? What features would you select to explain the “value”?
79. Apple question – How do you take millions of users with 100s of transactions each,
amongst 10ks of products and group the users together in a meaningful segment?
80. Facebook question – How many high schools that people have listed on their profiles are
real? How do we find out, and deploy at scale, a way of finding invalid schools?
81. We have a product that is getting used differently by two different groups. What is your
hypothesis about why and how would you go about testing it?
82. Intuit question – How would you design a ranking system?
83. Uber question – Explain how network effects might influence your choice of how to
assign experimental/control units and measure your main outcome metrics
84. LinkedIn question – What product metrics do you construct? How do you tell if your experiment is successful?
85. What trends in the data indicate that a given market is healthy? What does price tell you?
86. Facebook question – Given a series of tables; write the SQL code you would need to count subpopulations through joins.
87. Pinterest question – Write a SQL query to count the number of unique users per day who logged in from both an iPhone and the web, where iPhone logs and weblogs are in
distinct relations.
88. Spotify question – Given a sample set of tables, write a SQL query to get a summary metric from those tables.
89. Twitter question – How can you illustrate a tree-based system with a SQL query?
90. If you have a table with a billion rows, how would you add a column inserting data from
the original source without affecting the user experience?
91. Facebook question – There is a table that tracks every time a user turns a feature on or off, with columns for user_id, action (“on” or “off), date, and time. How many users turned the feature on today? How many users have ever turned the feature on? In a table that tracks the status of every user every day, how would you add today’s data to it?
92. Check if an integer is a palindrome (do not convert the integer to string)
93. Given 2 sorted arrays of integers, code to find a number from each array such that their
sum is closest to some integer K
94. Amazon question – Write a Python function that displays the first n Fibonacci numbers.
95. Cisco question – Merge 2 sorted linked list
96. eBay question – Given a function roll() that uniformly returns a double between 0 and 1 and an array/list of numbers of length N (no duplicates), create a function shuffle() that returns a permutation of equal probability.
97. How would you create/design/implement a certain algorithm from start to end?
98. LinkedIn question – Given a random generator that produces a number 1 to 5 uniformly,
write a function that produces a number from 1 to 7 uniformly
99. Generate a sorted vector from two sorted vectors.

 # Other question list
 * [List of ML questions](https://github.com/Sroy20/machine-learning-interview-questions/blob/master/list_of_questions_machine_learning.md)
 * [List of DL questions](https://github.com/Sroy20/machine-learning-interview-questions/blob/master/list_of_questions_deep_learning.md)
 * [Other interview questions](https://github.com/Feynman687/Interviews/blob/master/StatML.md)

* If you find this helpful, you can Sponsor this project. It's cool if you don't. 
 

