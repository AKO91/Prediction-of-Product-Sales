# Prediction-of-Product-Sales
## Ammar Owaineh
This project aims to analyze a dataset of sales of items of various types in multiple stores in order to predict patterns of future sales of  outlet stores based on the features provided in the data. The project starts by initial inspection of the dataset, then visualizing columns both seperately and in relation to each other, then it will move on to professionally handling any flaws in the data, and finally several prediction models will be trialed and tuned to attempt to get the best predicition results. 
In the first section of the project, the repository was created to load any relevant files and the data was cleaned by removing duplicate cells and adding placeholders to missing cells as appropriate. 
In the second and third section of the project, data visualization tools were used to identify and significant features and properties of the data and to look for patterns that may be useful to achieve the goal of the project. 
As part of the analysis, it was noted that while plotting the Item Visibility and Item Outlet Sales columns, there was a significant number of outlers in both categories as shown below: 

![image](https://github.com/AKO91/Prediction-of-Product-Sales/assets/170138532/a719110b-467d-40cf-b3d5-ac089309d816)
![image](https://github.com/AKO91/Prediction-of-Product-Sales/assets/170138532/ba17c4ba-e2ba-4f85-bc02-7e277061007a)

The plots show a high number of extreme values outside the interquartile range, which indicates a skew in the data, making it potentially harder to predict in these categories. However, it should be noted that these indications are preliminary and further thorough investigation of the date is needed to determine their significance. 

Another finding in the visualized data shows that both small and medium outlets have higher sale numbers than larger-sized outlets as highlighted below: 

![image](https://github.com/AKO91/Prediction-of-Product-Sales/assets/170138532/f6fbc03d-bdc1-4cb0-bea1-6246dfa49899)

The data also shows that supermarkets categorized as "Type 1" have almost five times the sales of other types included in the data ("Type 2," "Type 3," and "Grocery Store") as illustrated in the below plot: 

![image](https://github.com/AKO91/Prediction-of-Product-Sales/assets/170138532/d630e996-2b66-4eab-a61a-40f657e15d26)

Both the above illustrations toghether indicate that small and medium sized "Type" supermarkets would have the highest sale numbers. 

In addition, when plotting features against each other, there were some observations that could help with our predictions. 

One observation was in the plot below, which shows that supermarkets of all types, generally have significantly higher sales that grocery stores. 
![image](https://github.com/AKO91/Prediction-of-Product-Sales/assets/170138532/b2e35a6c-065e-4f0a-bd1c-1bbc52b6cca6)

Another potentially useful predicting feature found is the item's maximum retail price (MRP), which correlates moderately with the item outlet sales as shown below. 
![image](https://github.com/AKO91/Prediction-of-Product-Sales/assets/170138532/0f53d7e6-0883-45d3-b6d7-aded87556dc3)

In the fourth section, pipelines were created to impute any missing values, encode any categorical cloumns, and scale numerical values. In addition, the dataset was split randomly into two groups; %75 of the data was used to train the prediction models in the upcoming section, and %25 of the data was set aside to test the validy of the models. 

In the final section, the Linear Regression and Random Forest models from Scikit-learn were used both in their default and tuned versions to predict the item outlet sales. However The models have not performed excellently. The best model to use from the options available is the Random Forest model with tuned hyperparameters, as it is the only model that does not result in overfitting.
The R-squared metric of the best chosen model is 0.611 on the training data and 0.603 on the test data. This means that the model can predict results with approximately %60 accuracy.
When looking at the mean absolute error of the model's training and test data, we can see an absolute error averge of about 750, which is a large error margain considering the average of the target column (Item outlet sales) is 2181. However, it still remains the best model of the options available, as the Linear Regression model has absolute error averge of over 800 and the default Random Forests model has absolute error averge of approximately 765 on the test data. This metric is significant when looking at ther performance of the model, since it gives the number of discripency in item sales perdicted for each outlet when using the model to predict. 

Overall, after cleaning and visualizing the data and training models on it, the best result achieved is to predict item outlet sales with %60, whcih is helpful but not significant. If more data is available and more prediction models are trialed, prediction accuracy can be improved. 




