# Power Predictor

In this project, I used Bayesian Regression, a.k.a. Gaussian Process Regression, to solve the Kaggle [Energy Efficiency Dataset](https://www.kaggle.com/datasets/elikplim/eergy-efficiency-dataset).

The input feature vector contains 8 traits of simulated buildings, and the output is a vector of two elements containing the cooling load & heating load.

The data was split into a training set, and a test set. 

### What are Gaussian Processes?

Gaussian Processes (GPs) are a probabilistic model that define a distribution over random functions to make predictions about future data given some samples.

GP regression is a method that estimates the posterior distribution over functions from the dataset, by making an optimized inference of the data's mean & covariance.

My favorite source on GPs is [this one](https://cs.stanford.edu/~rpryzant/blog/gp/gp.html) from Stanford, which also leads to other great sources.

### Results & Conclusion

The two models experimented with are:
- Bayesian Regression on a [Gaussian Process](https://scikit-learn.org/stable/modules/gaussian_process.html) (GP) implemented with scikit-learn, and auto-tuned using the Limited Memory BFGS parameter optimization algorithm.
- A vanilla neural network implemented with PyTorch, fitted using Mean Squared Error.

The accuracy results in $R^2$ score were very good for both models:
- For the GP Regression, train set score 0.9966, test set score 0.9893
- For the neural network, train score 0.9943, test score 0.9912

More information is in the notebook :smile:

Future goal: implement the entire Bayesian Regression algorithm from scratch, using no machine learning libraries.

Overall, this project helped me get into statistics & optimization, which are both very cool topics that have myriad innovative applications!
