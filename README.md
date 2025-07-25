### Summary (obtained from project description within ipynb file):
**Overview**: In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. 
As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.

### Business Perspective:

From a business perspective, we are tasked with identifying key drivers for used car prices. In the CRISP-DM overview, we are asked to convert this business framing to a data problem definition. Using a few sentences, reframe the task as a data task with the appropriate technical vocabulary.

Using the provided dataset, we can visualize the data, build and train models that can predict factors such as, inventory alignment with demand, any opportunities that can yield high margins, and determine segment based marketing

## Methods of observation:
This project contains data cleaning methods of removing and replacing null data and columns, including handle "unknown" values that are difficult to classify and work with. We compared three different models (Polynomial Regression, Ridge and Lasso Regression) to predict the output and compare to the baseline accuracy. We also used hyperparameter tuning and feature importance to optimize the models even further and improve the accuracy. 
We also visualized trends within the data that affected the price.

### Report:
Upon cleaning the data and dealing with missing values, visualization of data trends, training and fine-tuning different types of models (Polynomial, Ridge, and Lasso), we were able to come up with a Ridge model with a polynomial degree of 6 and an alpha value of 0.001, which has achieved an accuracy score of 0.6977. Using this model, as well as the visualizations above, we can come up with the following trends:

Using Price as the target, the following features are listed in order of importance:

1. Year of the Vehicle
2. Odometer Reading
3. Type of the Vehicle
4. Manufacturer of the Vehicle
We can see from the analysis and plots above, that vehicles newer than 2015 retain stronger value and can dramatically increase sale price. In the future, we can implement a year-adjusted pricing model to avoid underpricing late models.

There appears to be an inverse relationship between odometer reading and price. After around 90,000 miles, the price trends tend to drop sharply, and drops even further for salvage titles.

Sedans and SUVs are the most common type of vehicle amongst all regions. Recommend doing a region by region analysis for most common type of vehicle, as well as the manufacturer.

For marketing and promotion, we can advertise premium fuel and condition within ads, given that fuel type also has a significant positive correlation. We can also target buyers by certain preferences. For "niche" vehicle types, we need targeted marketing to appeal to that demographic, such as for manual cars, or fuel-efficient cars.

In terms of acquiring vehicles, we should prioritize vehicles that:

1. Have less than 100,000 miles
2. Clean titles (not salvage)
3. Good condition ratings
4. Reputable and reliable manufacturers
