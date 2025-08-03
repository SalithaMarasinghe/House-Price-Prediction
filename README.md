Bangalore House Price Prediction using Linear Regression
1. Introduction
Real estate prices in Bangalore vary significantly due to factors such as location, property size, and number of rooms. The objective of this project was to build a predictive model that estimates house prices based on these parameters. A Linear Regression model was chosen for its interpretability and effectiveness in problems involving continuous numerical prediction. The project also includes a Flask-based web application that allows users to interact with the model.

2. Dataset Description
Source: Bengaluru House Prices dataset

Key Features:

location – Geographical area of the property

size – Number of bedrooms (BHK)

total_sqft – Area in square feet

bath – Number of bathrooms

price – Target variable (price in lakhs)

3. Data Preprocessing and Feature Engineering
Data Cleaning:

Removed irrelevant columns such as area_type, availability, etc.

Handled missing values in critical features.

Handling total_sqft:

Converted ranges like 2100-2850 to averages.

Dropped non-standard measurements (e.g., “Sq. Meter”).

Feature Engineering:

Extracted BHK from the size column.

Created price per square foot for normalization and better comparability.

Location Simplification:

Grouped locations with fewer data points into an “other” category to reduce dimensionality.

4. Outlier Detection and Removal
Removed properties with extreme price per square foot values.

Dropped inconsistent configurations (e.g., unusually low price for large properties).

Filtered data to improve model robustness.

5. Model Development
Model Choice: Linear Regression was selected due to its simplicity and interpretability.

Training and Evaluation:

Split the dataset into training and test sets.

Used cross-validation to ensure generalization.

Evaluated using R² score and compared against baseline models.

6. Model Export
Saved the trained model using Pickle.

Exported column names and metadata to a JSON file for use in deployment.

7. Deployment with Flask
Backend:

Implemented a Flask API to accept user input (area, BHK, bath, location).

Returned the predicted price in lakhs using the trained model.

Frontend:

Built a simple web interface using HTML, CSS, and JavaScript.

The interface allows users to:

Enter property area (square feet).

Select BHK and bathrooms.

Choose location from a dropdown.

Get estimated price on button click.

(The interface screenshot you provided illustrates this functionality.)

8. Results and Observations
The model provides reasonable predictions for most configurations.

Feature engineering and outlier removal significantly improved performance.

Deployment using Flask makes the model accessible to end-users.

9. Conclusion and Future Work
This project demonstrates how machine learning can be applied to real estate price prediction. Future improvements could include:

Using advanced models (e.g., Gradient Boosting, Random Forests).

Incorporating additional features such as amenities and neighborhood ratings.

Deploying the app using a cloud service for broader accessibility.
