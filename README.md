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
