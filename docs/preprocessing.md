# Data Preprocessing

The MLJAR platform is doing data preprocessing for you.
It can fill missing values and convert categorical attributes into numbers.
If your dataset contains attributes that require preprocessing the MLJAR will
detect them and propose preprocessing methods for you.

## Missing values preprocessing

For missing values inputation there are available following techniques:

 - fill with median value
 - fill with mean value
 - fill with minimum value minus 1
 - for categorical attributes, missing values will be filled with the most frequent value

If you need other technique for missing values inputation please let us know or
prepare dataset by yourself before uploading into MLJAR.

## Convert categorical attributes

For converting categorical attributes into numerical there are following methods:

 - convert categorical values into integers
 - one-hot encoding

 If you need other method for converting categorical values please let us know or
 prepare dataset by yourself before uploading into MLJAR.

## Dates and text

We are currently do not support converting dates and time into numbers.
It is on our list. Please prepare your dataset correctly before uploading it into MLJAR.
