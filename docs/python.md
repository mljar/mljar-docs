# Python Wrapper for MLJAR API

This wrapper enables you to run model search and tuning with MLJAR with two lines of code! It is super easy and super powerful.

```python
from mljar import Mljar

model = Mljar(project='My awesome project', experiment='First experiment')
model.fit(X,y)

model.predict(X)
```


## How to install

You can install mljar with **pip**:

    pip install -U mljar

or from source code:

    python setup.py install

## How to use it

 1. Create an account at mljar.com and login.
 2. Please go to your users settings (top, right corner).
 3. Get your token, for example 'exampleexampleexample'.
 4. Set environment variable `MLJAR_TOKEN` with your token value:
```
export MLJAR_TOKEN=exampleexampleexample
```
 5. That's all, you are ready to use MLJAR in your python code!

## API details

The wrapper makes it easy to interact with MLJAR, so we try to make it intuitive to use. However, there are few arguments that can be set.

For `Mljar` constructor:

 - **project** - string with project title
 - **experiment** - string with experiment title
 - **metric** - string with the metric which will be used for optimization. For classification valid metrics are: `logloss` and `auc`. The `logloss` is a default for binary classification. For regression task valid metrics are: `rmse`, `mse`, `mae`, the default is `rmse`.
 - **algorithms** - list of selected algorithms that will be checked and tuned. For binary classification there are following algorithms:
    * *xgb*  which is for Xgboost
    * *lgb*  which is for LightGBM
    * *mlp*  which is for Deep Neural Network
    * *rfc*  which is for Random Forest
    * *etc*  which is for Extra Trees
    * *knnc*  which is for k-Nearest Neighbors
    * *logreg*  which is for Logistic Regression

     The default selection for classification is `[xgb, lgb, mlp]`. For regression task there are following algorithms available:

    * *xgbr*  which is for Xgboost
    * *lgbr*  which is for LightGBM
    * *rfr*  which is for Random Forest
    * *etr*  which is for Extra Trees

     The default selection for regression is `[xgbr, lgbr]`.  

 - **validation** string which set a validation mode, valid strings are: `3fold`, `5fold`, `10fold`. This sets number of folds during cross validation. The default is `5fold`.
 - **tuning_mode** string that sets how many models for each algorithm will be checked. Available modes:
    * *Normal* - there will be checked 5-10 models
    * *Sport* - there will be checked 10-15 models
    * *Insane* - there will be checked 15-20 models

     The default is *Normal* mode.

 - **create_enseble** boolean that decides if ensemble of all available will be created. The default is `True`.
 - **single_algorithm_time_limit** integer that sets how much time (in minutes) there will be spend for training single algorithm.
             The default value is 5 minutes.
