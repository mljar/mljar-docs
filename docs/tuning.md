# Tuning

The algorithm tuning is important part of building machine learning model.
Each algorithm used in MLJAR is tuned to your data.
Tuning is done with cross-validation or separate validation dataset.
User needs to select a metric that will be optimized during tunning process.
All models constructed during tuning are available and displayed for user.
In the MLJAR there is a heuristic tuning method implemented that at first starts
with models with random parameters and based on their performance is trying to improve
them in next steps.

There are four modes of tuning:

 - **Normal** in this mode there will be trained about 5 to 10 models for each selected algorithm
 - **Sport** in this mode there will be trained about 10 to 15 models for each selected algorithm
 - **Insane** in this mode there will be trained about 20 to 25 models for each selected algorithm
 - **Perfect** in this mode there will be trained about 25 to 35 models for each selected algorithm
