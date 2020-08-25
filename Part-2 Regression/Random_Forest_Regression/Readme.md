# Random Forest Regression

Random Forest Regression is a supervised learning algorithm that uses ensemble learning method for regression. (Ensemble learning method is a technique that combines predictions from multiple machine learning algorithms to make a more accurate prediction than a single model.)

Random forest Regression overcomes the common problem of overfitting in Decision Trees.  
The basic idea is to combine multiple decision trees in determining the final output rather than relying on individual decision trees.  

<img src="/temp/rfr1.png" alt="rfr_diagram" width="600"/>
In the above image, many decision trees run in parallel with no interaction amongst them. The prediction is done by taking the mean of the prediction of all the trees.  

A Random forest regression model involves the folowing steps:  
1. Select K random data points from the training set.  
2. Build a decision tree associated to these K data points.  
3. Choose the N number of trees you want to build and repeat steps 1 and 2.  
4. For predicting a new data, first make each decision trees predict the value of y and then take the average of all y values to get the final prediction.
