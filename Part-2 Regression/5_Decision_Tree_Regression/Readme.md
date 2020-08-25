# Decision Tree Regression

Decision tree uses a flow chart like tree structure to predict the output on the basis of input described by a set of properties.   
Consider a dataset having 2 independent variables x1 and x2. The values are plotted as shown below:

<img src="/temp/dlr2.png" alt="dlr_graph" width=600 >

The decision tree algorithm will split the data into parts based on some calculations. For simplicity, let's say the decision tree looks like this:  

<img src="/temp/dlr1.png" alt="dlr_tree" width=500 >

So the algorithm would split our graph as shown below:  

<img src="/temp/dlr3.png" alt="dlr_graph" width=600 >

In this case, the value in green is calculated by the average of all values in that split. This is used to predict a new value depending on which split our data falls into.
