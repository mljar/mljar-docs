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

## Examples

To see examples please go to [mljar-examples on github][1].

## API details

The wrapper makes it easy to interact with MLJAR, so we try to make it intuitive to use. However, there are few arguments that can be set.

### `Mljar` constructor:

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

 - **validation_kfolds** the number of folds to be used in validation,
                       it is omitted if validation_train_split is not None
                       or there is validation dataset provided.
                       It can be number from 2 to 15.
 - **validation_shuffle** the boolean which specify if shuffle samples before training.
                       It is used in `k-fold CV` and in validation split. Default is set True.
                       It is ignored when validating with separate dataset.
 - **validation_stratify** the boolean which decides whether samples will be
                       divided into folds with the same class distribution.
                       In regression tasks this flag is ignored. Default is set to True.
 - **validation_train_split** the ratio how to split training dataset into train and validation.
                       This ratio specify what ratio from input data should be used in training.
                       It should be from (0.05,0.95) range. If it is not None, then
                       validation_kfolds variable is ignored.
 - **tuning_mode** string that sets how many models for each algorithm will be checked. Available modes:
    * *Normal* - there will be checked 5-10 models
    * *Sport* - there will be checked 10-15 models
    * *Insane* - there will be checked 15-20 models

     The default is *Normal* mode.

 - **create_ensemble** boolean that decides if ensemble of all available will be created. The default is `True`.
 - **single_algorithm_time_limit** integer that sets how much time (in minutes) there will be spend for training single algorithm.
             The default value is 5 minutes.

### `fit` method:

 - **X** matrix with training attributes, it can be `pandas` or `numpy` type.
 - **y** vector with target values, it can be `pandas` or `numpy` type.
 - **validation_data** tuple (X,y) with validation data. If set to None, then
                           the k-fold CV or train split validation will be used.
                           Default is set to None.
 - **wait_till_all_done** boolean which decides if fit function will wait
                         till experiment is done, default is set to `False`.
### `predict` method:

 - **X** matrix which will be used for computing predictions, it can be `pandas` or `numpy` type.


[1]: https://github.com/mljar/mljar-examples
