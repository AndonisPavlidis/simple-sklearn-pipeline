# Sandbox for Scikit-Learn's Pipeline 

Play around with the housing dataset to create a simple pre-processing and cross-validation pipeline.

## Pre-processing
* Missing values in numerical features will be imputed by replacing them with the median, as most ML algorithms don’t 
expect missing values. 
* In categorical features, missing values will be replaced by the most frequent category. 
* The categorical feature will be one-hot encoded, as most ML algorithms only accept numerical inputs. 
* A few ratio features will be computed and added: bedrooms_ratio, rooms_per_house, and people_per_house. Hopefully these will better correlate with the median house value, and thereby help the ML models. 
* A few cluster similarity features will also be added. These will likely be more useful to the model than latitude and longitude. 
* Features with a long tail will be replaced by their logarithm, as most models prefer features with roughly uniform or Gaussian distributions. 
* All numerical features will be standardized, as most ML algorithms prefer when all features have roughly the same scale.

## Fit Model and Fine Tune

* Cross validate a Random Forest byt tuning pre-processing and model hyper parameters.