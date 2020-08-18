# Polynomial Regression

Polynomial Regression is used when we know that our data is correlated, but the relationship doesn’t look linear.  
For example consider the given dataset 

<img src="/temp/plr2.png" alt="data" height="300">

Clearly, there is a correlation between position level and salary. When we try to use a simple linear regression in the above data, we get a graph as shown below  

<img src="/temp/plr3.png" alt="slr_graph" width="500">

The line doesn't fit very well :(  
To overcome this problem (or "under-fitting"), we need to increase the complexity of the model.

To generate a higher order equation we can add powers of the original features as new features.  
Hence the linear model can be transformed as shown below  

<img src="/temp/plr1.png" alt="plr_equation" width="500">  

*Note that this is still considered to be linear model as the coefficients/weights associated with the features are still linear. higher powers of x are only a feature. However, the curve is polynomial in nature.*  

<img src="/temp/plr4.png" alt="plr_graph" width="500"> 

It is clear from the plot that the quadratic curve is able to fit the data better than the linear line. Hence it is better to use polynomial regression in this case.
