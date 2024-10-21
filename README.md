# portfolio-part-2-mdazizulaman
portfolio-part-2-mdazizulaman created by GitHub Classroom
## Introduction

In this Portfolio, we explore the task of predicting user ratings for e-commerce products using a linear regression model. We conduct a comprehensive analysis to understand the impact of feature selection and different sizes of training and testing data on the model's performance. The analysis is based on a cleaned e-commerce dataset, focusing on the correlations between various features and the target variable, 'rating.'

## Data Exploration

We begin by importing the dataset 'cleaned_ecommerce_dataset.csv' using the Pandas library and examining its characteristics. The dataset contains various columns, including 'userId', 'timestamp', 'review', 'item', 'rating', 'helpfulness', 'gender', 'category', 'item_id', 'item_price', 'user_city'. It is essential to understand the dataset's structure and data types before proceeding.

## Correlation Analysis

To determine the relationships between the features and the target variable 'rating,' we calculate correlation coefficients. However, since our dataset contains categorical features like 'gender,' 'category,' and 'review,' we first convert these categorical variables into numerical values using the OrdinalEncoder from Scikit-Learn. We then calculate correlations using the corr() method.

From the correlation analysis, we identify the most and least correlated features with 'rating':

**Most Correlated Features**: 'category' and 'review' (negative correlation).

**Least Correlated Features**: 'helpfulness' and 'gender' (very weak positive/negative correlation).

## Splitting Training and Testing Data

To assess how the size of the training and testing data affects model performance, we perform two splits:

Case 1: 10% training data, 90% testing data.
Case 2: 90% training data, 10% testing data.
We aim to investigate how varying the training data size impacts model performance.

## Model Training with Feature Selection

We train four linear regression models under different conditions:

(model-a) 10% training data, two most correlated features ('category' and 'review').
(model-b) 10% training data, two least correlated features ('helpfulness' and 'gender').
(model-c) 90% training data, two most correlated features ('category' and 'review').
(model-d) 90% training data, two least correlated features ('helpfulness' and 'gender').
These models allow us to assess the effects of both feature selection and training data size on prediction performance.
## Model Evaluation

We evaluate the performance of the four models using two regression metrics: Mean Squared Error (MSE) and Root Mean Squared Error (RMSE). These metrics provide insights into the accuracy of the rating predictions. I also include R2 Squared value.

## Visualizing and Analyzing Results

We visualize and analyze the results to draw insights:

Models (a and c), with the most correlated features and larger training data sizes, are expected to perform better due to more relevant information and better pattern capture.
Models (b and d), with the least correlated features and smaller training data sizes, may perform worse due to less relevant information and potential overfitting.

## Conclusion

This analysis provides valuable insights into building effective linear regression models for predicting user ratings in e-commerce. It underscores the importance of feature selection and training data size in model performance. Further experimentation and fine-tuning of models may yield even better results. Careful data preprocessing, random sampling, and consistent evaluation strategies are crucial for robust and accurate rating predictions.

By following this analysis plan, you can gain a deeper understanding of your e-commerce dataset and make informed decisions when building rating prediction models.
