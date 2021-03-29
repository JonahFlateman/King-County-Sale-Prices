# Module 2 Final Project readme

In this project, we will build a multiple linear regression model to predict sale prices for homes in King County, WA.  Using an iterative approach, we will clean, feature engineer, normalize, and model our data using an Ordinary Least Squares regression method to build the final model. 

## Dataset

We will use a sales dataset from 2014 and 2015 provided in the file 'kc_house_data.csv.' and imported as a DataFrame

## Goals

* Interpret and clean the data provided into a useful framework for our modeling
* Feature engineer variables as needed, analyzing relationships between variables and scaling as necessary
* Iterating on our model to reduce p-values and use R-squared as a key metric
* Creating training and testing sets of data used to validate our model

## Methodologies

### Importing and Cleaning

* Check for NaN values, removing and reassigning as necessary
* Using boxplots, identify and remove outliers to avoid skewing the model
* Identify continuous and categorical variables, using regplots to examine relationships to sale price

### Feature Engineering

* Change year rennovated, full date, and zipcode variables to categoricals
* Check for multicollinearity using a heatmap and drop highly correlated features
* Use boxplots to plot our categorical variables' relationships to sale price

### Normalization and Scaling

* Use distplots to examine distributions of continuous variables
* Use log transformations on continuous variables and standardize all variables
* Create dummy variables on categoricals, add to DataFrame and drop superfluous columns

### Modeling

* Iterate on model using a stepwise selection to eliminate variables with p-values greater than .05
* Create training and testing sets, calculate the mean squared error (MSE) and cross-validate over train-test split sizes
* Apply trained model to test set