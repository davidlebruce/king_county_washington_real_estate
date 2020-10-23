# King County Housing Price Predictive Model

**Author**: [David Bruce](mailto:david.bruce14@gmail.com)


## Overview

Given a set of data about the housing market in King County, Washington by the Flatiron School, NYC, the task to perform was to create the best predictive model for a house's sale price. My goal was to take the 17,000+ rows of data and break them up into a set of training data and testing data to find the best performing model based on the lowest RMSE. I would then aggregate all the data to train my best performing model on, to then put it to one final test on a set of holdout data with no price column.


## The Data

The data provided by Flatiron School, NYC had roughly 17,000 rows of houses with 20 columns of descriptive numerical data. There were no missing values in the initial dataset, so minimal cleaning was done by me. Just from basic knowledge of real estate, one could start to come up with ideas about what factors are most important to buyers and sellers of houses. 

## Methods

I used a variety of methods to try to improve my linear regression model. I played with polynomial interactions and ran two-sample t-tests on different sample means. 

## Conclusions & Next Steps

In the end, I was able to create a better model than my baseline model by creating a bunch of polynomial and interactive features, but it is not interpretable in terms of the coefficients.

Given more time I would have liked to explore more with feature engineering and creating different columns of dummy features as well as diving deeper into the location data. In my exploration I was able to create a very crude map with geopandas, but there is a lot more to explore there especially if I was able to scrape more data based around lat, long, and zipcode.



### Further Research

- Scrape the web for zipcode census data to enrich the my spatial data
- Scrape the web for locations of schools and public transport to increase spatial data
- Look for the ratio between listings and sales throughout a year. Domain research indiates that is an important seasonal variable. 

### Navigation
- `Final_Notebook.ipynb`: Finalization of preprocessing and data analysis contains model used to predict on holdout data
- `Exploration_Folder`: Folder containing initial exploration into data and statistical tests
- `Predict_holdout.ipynb`: Where holdout data is predicted and sent to .csv
- `kc_house_data_test_features.csv`: Holdout set of data to predict on (no 'price' column)
- `kc_house_data_train.csv`: Training dataset
- `housing_preds_david_bruce.csv`: My price predictions on the holdout set
- `model.pickle`: Model from Final_Notebook used on holdout data
- `images`: Folder containing images used in repository

