# House-Price-Prediction-System
A Python Linear Regression based prediction model has been used. A website in HTML, CSS and JavaScript is used to allow the user to provide the input parameters based on which the model makes a prediction.

The Bangalore house price dataset from Kaggle has been used to train the prediction model. Before model training, a number of steps were taken to clean up the data set and remove outliers.

Data Cleaning Steps used :
a) Removing unimportant columns i.e 'area_type','society','balcony','availability'.
b) Removing Rows with null values.
c) Cleaning up the size column and making a new bhk column with consistent single number values for bedroom,hall,kitchen.
d) The total_sqft area column has rows where the values are in ranges and not a single value. 
e) We use a function to convert the range into an average value.
f) We create a price_per_sqft column.
g) For all locations that have less than or equal to 10 rows, we rename them to 'other'.

Outlier Detection and Removal :
a) Remove rows where the sqft area per bhk is less than 300.
b) Remove rows where price per sqft is either very high or very low.
c) Remove cases where sqft area is same but if no of bedrooms is more the price is same as houses with less bedrooms.
e) Remove houses where no of bathrooms is > no of bedrooms + 2.

Matplotlib has been used for data visualisation at each stage.

Data after removing the price_per_sqft outliers per location :
![c](https://github.com/salil-fernandes/House-Price-Prediction-System/assets/48954206/1b0c5ad0-ec6f-4df1-9cf0-c3b107155755)

A few other visualizations after removing outliers :
![d](https://github.com/salil-fernandes/House-Price-Prediction-System/assets/48954206/419e2f6e-5893-4687-ba80-7bbddc9f248a)

![e](https://github.com/salil-fernandes/House-Price-Prediction-System/assets/48954206/0c7e0bd5-42df-49a1-9a6f-7376da575811)

GridSearch CV has been used to compare the Lasso, Linear and Decision Tree regresion algorithms to find out which gives the ebst accuracy according to specified hyperparameters. The results show Linear Regression was the best algorithm.
![a](https://github.com/salil-fernandes/House-Price-Prediction-System/assets/48954206/4937baae-0de3-4a93-b8b9-85f6b7830cf7) ![b](https://github.com/salil-fernandes/House-Price-Prediction-System/assets/48954206/c2b13347-fb28-471b-9162-95f2402402ed)


