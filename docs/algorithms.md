# Algorithms

Right now there are available algorithms for following machine learning tasks:

 - binary classification
 - regression

More is coming soon!

## Binary Classification

For binary classification there are following algorithms available:

 - Xgboost
 - LightGBM
 - Random Forest
 - Extra Trees
 - Regularized Greedy Forest
 - k-Nearest Neighbors
 - Logistic Regression
 - Neural Networks

## Regression

For regression task there are following algorithms available:

 - Xgboost
 - LightGBM
 - Random Forest
 - Extra Trees
 - Regularized Greedy Forest

## Libraries

The MLJAR is standing on the shoulders of giants:

 - [scikit-learn github][2]
 - [xgboost github][3]
 - [lightGBM github][4]
 - [keras github][5]
 - [tensorflow github][6]
 - [RGF paper][7]

## Ensemble

There is an option to build ensemble of models based on trained algorithms.
Currently, there is available an ensemble average method, which does a greedy search
over all results and try to add (with repetition) a model to the ensemble to improve
ensemble performance. The ensemble performance is computed based on out-of-folds predictions
of used models. For more details please take a look on [Caruana paper][1].


[1]: http://www.cs.cornell.edu/~alexn/papers/shotgun.icml04.revised.rev2.pdf
[2]: https://github.com/scikit-learn/scikit-learn
[3]: https://github.com/dmlc/xgboost
[4]: https://github.com/Microsoft/LightGBM
[5]: https://github.com/fchollet/keras
[6]: https://github.com/tensorflow/tensorflow
[7]: https://arxiv.org/abs/1109.0887
