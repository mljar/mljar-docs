# Welcome

MLJAR is a platform for rapid prototyping, developing and deploying machine learning models. Yeah!

## Rationale

The reasons why MLJAR was created:

 - the universal learning algorithm does not exist, that's why to find good machine learning model you have to check many different algorithms - MLJAR makes it easy, don't worry!
 - learning algorithms have set of hyper-parameters that needs to be tuned for a problem - with MLJAR each selected algorithm is tuned to your dataset
 - training many different algorithms can take a lot of time - that's why MLJAR is doing this on many machines in parallel to give you results as fast as possible
 - there is a pain when you train a model and realize that you don't saved them, so you need to start training again - it will never happen with MLJAR, all models are always saved. What is more, we save models during training so you can check partial results and stop straining when you want. (We also store all models predictions produced during training, so ensembling is easy, yeah!)
 - sharing results with cooperators is a pain, you fill some spreadsheets and dump ROC curves into figures and attach them in email message - no more, with MLJAR you can easily share your results with others (even with whole world, by public projects)
 - to deploy your model you don't have to be a cloud hero, you just select algorithm, click and MLJAR provides you a REST API for your model

## What is MLJAR doing?

MLJAR makes algorithm search and tuning painless. It checks many different algorithms for you. For each algorithm hyper-parameters are separately tuned. All computations run in parallel in MLJAR cloud, so you get your results very quickly. At the end the ensemble of models is created, so your predictive model will be super accurate.

## User Interface

There are two types of interface available in MLJAR:

 - you can run Machine Learning models in your browser, you don't need to code anything. Just upload dataset, click which attributes to use, which algorithms to use and go! This makes Machine Learning super easy for everyone and make it possible to get really useful models,
 - there is a python wrapper over MLJAR API, so you don't need to open any browser or click on any button, just write fancy python code! We like it and hope you will like it too! To start using MLJAR python package please go to our [github][2].

## Machine Learning Tasks

For now, there are available two types of task that you can crunch in MLJAR:

 - binary classification (your target attribute should has binary values [0,1])
 - regression (your target attribute should has continuous values)

We are working on more tasks! If you need something please let us know!

## Contact

In case any questions, suggestions please reach us by email from [mljar website][1].

We hope you will get very useful models with MLJAR! Happy data mining to all!


[1]: https://mljar.com
[2]: https://github.com/mljar/mljar-api-python
