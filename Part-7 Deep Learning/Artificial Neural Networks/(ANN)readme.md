## This is a model where we will predict probability where user has clicked an ad or not with some given features from the dataset with the use of Artificial Neural Network
#This is a really big dataset

## IMPORTIG PACKAGES
## numpy and pandas packages helps in handling dataframes and sns , matplotlib helps in visualizing them 

import numpy as np

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

%matplotlib inline

## Importing the datasets of 1 million rows(limit of jupyter notebook)

df=pd.read_csv('train_data.csv',sep='|',nrows=1000000)
df2=pd.read_csv('test_data_A.csv',sep='|',nrows=1000000)
df.head()

## Seeing the corelated features of the lable columnd

plt.figure(figsize=(12,10))

sns.heatmap(df.corr(),annot=False,cmap='viridis')

df.columns

## Seperating the target and training set

X=df.drop(['communication_onlinerate','label'],axis=1)

y=df['label']

## dropping less related columns from testing set as well

X_test2=df2.drop(['id','communication_onlinerate'],axis=1).values

## choosing 1 percent of input datasets for faster training

X1=X.sample(frac=0.01,random_state=1)

y1=y.sample(frac=0.01,random_state=1)

## Importing random sampler which creates equal sets in both labels of 1 and 0 (to decrease bias)

from imblearn.over_sampling import RandomOverSampler

os=RandomOverSampler()

X_res,y_res=os.fit_sample(X,y)
## checking for number of columns in our sapmled dataset
X_res.columns.nunique()

# Neural network contruction and for our dataset
X_res=X_res.values

y_res=y_res.values

## splitting the datsets to check for accuracy of our model

from sklearn.model_selection import train_test_split

X_train,X_test,y_train, y_test = train_test_split( X_res, y_res, test_size=0.33, random_state=42)

## Scaling the features
from sklearn.preprocessing import StandardScaler

scaler=StandardScaler()

X_train=scaler.fit_transform(X_train)

X1=scaler.transform(X1)

X_test2=scaler.transform(X_test2)

## Importing packages for construction of simple neural network

from tensorflow.keras.models import Sequential

from tensorflow.keras.layers import Dense

from tensorflow.keras.callbacks import EarlyStopping

## Constructiong neural network of 8 layers (the output layer is 1 which is type sigmoid for calculating probability)
## more datasize=more layers

model=Sequential()

model.add(Dense(200,activation='relu'))

model.add(Dense(100,activation='relu'))

model.add(Dense(50,activation='relu'))

model.add(Dense(50,activation='relu'))

model.add(Dense(25,activation='relu'))

model.add(Dense(10,activation='relu'))

model.add(Dense(5,activation='relu'))

model.add(Dense(1,activation='sigmoid'))

## optimizer is adam to enhance our training and loss is binary crossentropy 

model.compile(loss='binary_crossentropy', optimizer='adam',metrics=['accuracy'])

## fitting our model in 40 epochs and batch size of 300

model.fit(x=X_train,y=y_train, epochs=40,validation_data=(X1,y1),verbose=1, batch_size=300)

## predicting our labels from our neural network

predictions1=model.predict_classes(X1)
 # Importing classification metrics for checking accuracy
 from sklearn.metrics import classification_report, confusion_matrix

print(classification_report(y1,predictions1))

print('\n')

print(confusion_matrix(y1,predictions1))

# This model gave 96 percent precision 84 percent recall and 88 percent f1 score
