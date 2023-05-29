# breast-cancer-detection-using-LR-and-Naive-Bayes
In this problem, LR and Naïve bayes classifiers will be used to detect the breast cancer. Load dataset by
sklearn “load_breast_cancer” function.(split ratio: 2:8)
( https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html#sklearn.datasets.load_breast_cancer)

a) Use the sklearn`s built-in function and train a LR model to detect cancer; Also, explain the
parameters that used in built-in model and their effects. Tune the model and get better
result as you can; report your tries and confusion matrix as well as accuracy.

b) Repeat previous part for gaussian naïve bayes classifier and compare the results. Which
one performs better? How much and why?

c) A classic A classic simple technique for feature selection as pre-processing is calculating the
direct importance of each feature on target; then, keeping some important features and
dropping the others. 

In this part, you are asked to simulate the mentioned strategy.
First, train the LR model for each feature and obtain 30 related models (For each model
only one feature with the target is used).

Second, calculate the AUC of each model and select the top 20 related features.
Third, Using the obtained 20 features, Train the best LR and naïve Bayes classifiers that you
obtained in parts (a) and(b); then, compare the results. Also, Report the results in each step
and model. Is the feature selection worth it? Why?
Note: You are allowed to use any libraries or functions.

d) Another interesting technique is feature extraction using LR. In this strategy, the goal is to
extract the normed features that are informative about the target. For this aim, use the 30
trained LR models from the previous part. For each feature, pass the feature`s value to its
related model and obtain its probability (using predict_proba or predict_log_proba
functions); now replace the feature`s value with its probability. Do the mentioned
procedure for each feature and sample. Now, you have a probabilistic dataset. As you
learned, the Bayes classifier gets along with probabilistic data. Use the new dataset to train
Gaussian and Multinomial Naïve Bayes and detect cancer. Compare the results to previous
parts and discuss them. Also, report AUC, and confusion matrix.
