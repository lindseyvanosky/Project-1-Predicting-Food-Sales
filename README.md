# Predicting Food Sales Revenue
## An Analysis of Grocery Store Data

**Author**: Lindsey Vanosky

### Business problem: 
As an introduction to Data Science, we need to predict potential food sales using data from various grocery stores and supermarkets. 

### Data:
Our data source is a csv file that originally had 12 columns and 8,523 entries.  
  <br> Item_Identifier:            object 
  <br> Item_Weight:                float64 
  <br> Item_Fat_Content:           object 
  <br> Item_Visibility:            float64 
  <br> Item_Type:                  object 
  <br> Item_MRP:                   float64 
  <br> Outlet_Identifier:          object 
  <br> Outlet_Establishment_Year:  int64
  <br> Outlet_Size:                object
  <br> Outlet_Location_Type:       object 
  <br> Outlet_Type:                object 
  <br> Item_Outlet_Sales:          float64

## Methods
- For the first part of the project (Data & Visualization) I used pandas dataframes to explore and imputate the data set. After exploring the data several null values were identified and imputated using numpy. Once I had a complete data set, I was able to plot the features using matplotlib and seaborn to both explore and interpret my data, as well as plot explanatory models to identify important metrics and correlations within the data. 
- For the second part of the project (Machine Learning) I returned to the original data set and prepped it for machine learning using a preprocessing pipeline consisting of scikit column selectors, one hot encoding and a simple imputer. Once the data was processed, I used a linear regression model as well as a decision tree to learn the data. 

## Results
- I ended up with two clean data sets - one used to plot exploratory and explanatory models, and another used to build the regression models. Using these two data sets I created the following graphs and models:

#### Bar Chart: Sales by Food Type
![Bar chart](https://user-images.githubusercontent.com/105459145/177413685-57e730e3-dac9-46a1-a985-6cef641cc276.png)
> This bar graph is a representation of total sales categorized by Food Type. This base level interpretation shows us which food types sell the best/worst. At this level you can only make educated guesses on which food types will sell best, as we do not have any other features plotted such as Outlet Size and Item MRP. Do fruits and vegetables sell the most because they are the most expensive? Or is it simply a popularity contest? We do not know. 

#### Line Graph: Sales by Outlet Type
![line graph](https://user-images.githubusercontent.com/105459145/177416171-105441a1-5fa8-4add-ba6a-2ac53f067a17.png)
> This simple line graph shows us the total sales by Outlet Type. Supermarket Type 1 has the highest total sales, but why? Is it because those are the biggest stores? Or because they are located in major cities? We do not know. 

## Model
My final model was a Decision Tree. This model allowed for the most hyperparameter tuning. After determining the ideal values for relevant hyperparameters, I ran the regression tree and calculated the following metrics from our test data:
- r2 score: 0.59
- RMSE: 1063.76
<br>
This r2 score is telling us that this model can speak for 41% of the data. This is a low r2 score. Our RMSE score is telling us that there is a +/- $1,063,760 error on the predictions. Arguably, this model does not do a good job at solving the business needs. 

## Recommendations:
This model is underfitting, as the model performed poorly on both our train and test data. We need to make the more complex in order to yield more accurate results.

## Limitations & Next Steps
Here we only tested two different regression models. There are other models that may work better for this type of data set, such as the Bagged Tree model. My next step would be to try this model, as well as clean the data a little more, focusing on columns with stronger correlations. 

### For further information
For any additional questions, please contact **lindsey.vanosky@gmail.com**
