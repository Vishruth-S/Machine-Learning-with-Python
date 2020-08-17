# Simple Linear Regression

Simple linear regression is used to estimate the relationship between **two** quantitative variables. One value is for the dependent variable and one value is for the independent variable.  

## The math 
Linear regression is nothing but a manifestation of the simple line equation  
*y = mx + c*  

The same equation of a line can be re-written as:  
![slr_equation](/temp/slr1.png)  

Consider the given Dataset containing "years-of-experience" and corresponding "salary". Clearly, there is a correlation that as years of experience increases, salary also increases.  
Hence it is possible to predict a person's salary based on years of experience using Simple Linear Regression.  
Here, x = years of experience, y = salary and b & b0 are the coeffiecients of the equation. So in order to predict y (salary) given x (years-of-experience), we need to know the values of b and b0 (the model’s coefficients).  

*While training and building a regression model, it is these coefficients which are learned and fitted to training data.*  

<img src="/temp/slr2.png" alt="alt text" width="600" height="600">  

In the figure, the red points are the data points and the blue line is the predicted line for the training data. To get the predicted value, these data points are projected on to the line.




