# Predict

To get predictions from trained models you can download model in `Deploy` view or you can upload test dataset into MLJAR and use it for prediction. This situation is described below.

 1. Upload you data file in `Sources` view.
 2. Accept attributes usage in `Preview` for uploaded dataset.
 3. Go to `Predict` view, in top right corner select dataset which will be used for prediction.
 4. Select algorithm that will be used, by selecting checkbox.
 5. Press `Start Prediction` and wait a while. Click `Refresh` on the bottom of the page to see if prediction is computed.
 6. Your predictions will be displayed in the bottom of the page where you can download it.

## Predict method

In case of training with cross-validation (CV) all models computed during CV will be used for prediction
and their predictions will be averaged. For example, if you run algorithm training with 5 fold CV, then for
each parameter setting you have 5 models trained on different train folds. For computing a prediction
on new dataset, there will be computed 5 predictions from each model and averaged - this is what you download.

In case of training with separate validation dataset, there is only one model trained and only one model is
used for computing predictions.
