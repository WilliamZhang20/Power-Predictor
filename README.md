# Power Predictor

In this project, I used Bayesian Regression, a.k.a. Gaussian Process Regression, on the Kaggle [Energy Efficiency Dataset](https://www.kaggle.com/datasets/elikplim/eergy-efficiency-dataset).

The input feature vector contains various traits of simulated buildings, and the output is a vector of two elements containing the cooling load & heating load.

Through this project, I gained experience working on both statistics and optimization.

My favorite resource on Gaussian Processes by far is [this one](https://cs.stanford.edu/~rpryzant/blog/gp/gp.html) from Stanford.

The two models experimented with are:
- Bayesian Regression on a [Gaussian Process](https://scikit-learn.org/stable/modules/gaussian_process.html) (GP) implemented with scikit-learn.
- A vanilla neural network implemented with PyTorch.

The accuracy results in $R^2$ score were:
- For the GP Regression, train set score 0.9966, test set score 0.9893
- For the neural network, train score 0.9905, test score 0.9884

More information is in the notebook.
