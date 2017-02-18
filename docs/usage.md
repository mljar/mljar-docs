# Quick Start

Building machine learning models should be easy! (you see too many steps below to start? come on, it is only like that at the beginning, go and do it! Trust me it is easy!)

## Analysis steps

 1. Login and create a project.
 2. Go into a project by clicking on its title.
 3. In project main view, you should be redirected to `Sources` if it is an empty project.
 4. In `Sources` view, please add a dataset by clicking `Add new dataset`.
 5. In `Add new dataset` box please provide a name for your dataset and select a data file. (Please check available data formats)
 6. OK, after uploading dataset please wait for a while, we are computing a dataset basic statistics. You will see a message in data source that it is ready for preview in MLJAR service.
 7. Please click on `Preview` or go to `Preview` from left menu and select your dataset. Each dataset should be accepted before analysis. You need to select attributes which will be used as models input (select for them `Use it` value) and you need to specify `Target` attribute, which will be model output. For attributes not used in analysis please set column usage to `Don't use`. You can also specify `Id` column if exists. After selecting attributes please `Accept` dataset in top of the view.
 8. With accpeted dataset you are ready to define machine learning experiments (yes, you have to experiment a lot if you want to do good ML :) ). Please go to `Compute` view.
 9. In `Compute` view, please click on `Add new experiment`.
 10. While defining a new experiment you need to define:
      * input dataset
      * learning algoritms
      * tuning parameters

 11. `Save` experiment and click on it on the list. Check if its details looks like expected and click `Start experiment` after that all the machine learning magic will start!
 12. To review models go to `Results` from left menu. To check algorithm details click on it.


## Predict

To get predictions from trained models you can download model in `Deploy` view or you can upload test dataset into MLJAR and use it for prediction. This situation is described below.

 1. Upload you data file in `Sources` view.
 2. Accept attributes usage in `Preview` for uploaded dataset.
 3. Go to `Predict` view, in top right corner select dataset which will be used for prediction.
 4. Select algorithm that will be used, by selecting checkbox.
 5. Press `Start Prediction` and wait a while. Click `Refresh` on the bottom of the page to see if prediction is computed.
 6. Your predictions will be displayed in the bottom of the page where you can download it.

## Deploy

To deploy your model:

 - you can download it from `Deploy` view - we are working on script that will allow you easy deploy models locally, so checkout our [github](https://github.com/mljar)
 - or your model can be accessed by REST API (we are working on this feature !!!)
