# Preprocessing Data
In any Machine Learning process, Data Preprocessing is that step in which the data gets transformed, or Encoded, to bring it to such a state that now the machine can easily parse it. In other words, the features of the data can now be easily interpreted by the algorithm.

## Steps in Data preprocessing
* ### Step 0: Installing the required libraries  
  The following libraries are the core libraries used in ML    
  1. [Numpy](https://numpy.org/)  
  ```
  pip install numpy
  ```
  2. [Pandas](https://pandas.pydata.org/)  
  ```
  pip install pandas
  ```
  3. [Matplotlib](https://matplotlib.org/)
  ```
  pip install matplotlib
  ```
  
* ### Step 1: Importing the libraries  
  Once you have installed the required libraries, the next step is to import them.    
  ```
  import numpy as np
  import pandas as pd
  import matplotlib.pyplot as plt
  ```
  
* ### Step 2: Importing the dataset   
  In this step, you need to import the dataset/s that you have gathered.  
  You can import the dataset using the “read_csv()” function of the Pandas library. This function can read a CSV file (either locally or through a URL) and also perform various     operations on it. The read_csv() is written as:
  ```
  dataset = pd.read_csv("your_data_file.csv")
  ```
  During the dataset importing process, there’s another essential thing you must do – extracting dependent and independent variables. For every Machine Learning model, it is     necessary to separate the independent variables (matrix of features) and dependent variables in a dataset.  
  
  To extract the independent variables, you can use “iloc[ ]” function of the Pandas library. This function can extract selected rows and columns from the dataset.
  ```
  x = dataset.iloc[:, :-1].values
  ```
  In the line of code above, the first colon(:) considers all the rows and the second colon(:) considers all the columns. The code contains “:-1” since you have to leave out the last column containing the dependent variable.  
  Similarly, to extract the dependent variable(which is the last column),
  ```
  y = dataset.iloc[:, -1].values
  ```
  Visit [this link](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iloc.html) to read more about iloc documentation  
  
* ### Step 3: Identifying and handling the missing values    
  In data preprocessing, it is pivotal to identify and correctly handle the missing values, failing to do this, you might draw inaccurate and faulty conclusions and inferences from the data.  
  Basically, there are two ways to handle missing data:
   * Deleting a particular row 
   * Calculating the mean  
   
  The [sklearn](https://scikit-learn.org/stable/) library is used for this. Check the code to see implementation.  
  
* ### Step 4: Encoding the categorical data  
  Categorical data refers to the information that has specific categories within the dataset. For example, in the given dataset, "Country" is a categorical data while all other entries are numerical. Since ML models are based on mathematical equations, we only need numbers and hence it is needed to change categorical data into numbers (encoding).  
  This is also done using the sklearn library modules. Refer code.     
  visit [this link](https://towardsdatascience.com/all-about-categorical-variable-encoding-305f3361fd02) to read more about encoding categorical data.    
  
* ### Step 5: Splitting the dataset  
  Every dataset for Machine Learning model must be split into two separate sets – training set and test set.  
  Training set denotes the subset of a dataset that is used for training the machine learning model. Here, you are already aware of the output. A test set, on the other hand, is the subset of the dataset that is used for testing the machine learning model. The ML model uses the test set to predict outcomes.  
  
   To split the dataset, you have to write the following line of code
   ```
   from sklearn.model_selection import train_test_split  
   x_train, x_test, y_train, y_test= train_test_split(x, y, test_size= 0.2, random_state=0) 
   ```
   The test_size parameter specifies the size of the test set. 0.2 means 20% test set and 80% training set. This can be modified according to the needs.  
   The last parameter, “random_state” sets seed for a random generator so that the output is always the same.   
   
* ### Step 6: Feature scaling  
  Feature scaling is a method to standardize the independent variables of a dataset within a specific range.  
  In other words, feature scaling limits the range of variables so that you can compare them on common grounds.  
  Read [this aricle](https://towardsdatascience.com/all-about-feature-scaling-bcc0ad75cb35) to learn more about Feature scaling  

Check the code for implementation of all the above mentioned steps in Data preprocessing
  
  

