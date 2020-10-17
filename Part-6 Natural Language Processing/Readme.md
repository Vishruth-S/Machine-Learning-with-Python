# Natural Language Processing (NLP)
In any Machine Learning process, NLP is the ability of a computer to understand, analyze, manipulate, and potentially generate human language. Some of its uses include Search Engines, Translation Softwares, Spam filters, etc.

## Steps in Natural Language Processing (NLP)
* ### Step 0: Installing the required libraries  
  The following libraries are the main libraries used for NLP in ML
  1. [(Natural Language Toolkit)NLTK](http://pypi.python.org/pypi/nltk)  
  ```
  pip install nltk
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
  import nltk
  import pandas as pd
  import matplotlib.pyplot as plt
  ```
  #### After importing nltk
  * Type `nltk.downlaod('stopwords)`
  * After typing that, we get an NLTK Downloader Application which is helpful in NLP Tasks.
  * Other useful packages can be installed similarly.
  
* ### Step 2: Importing the dataset   
  In this step, you need to import the dataset/s that you have gathered.  
  You can import the dataset using the “read_csv()” function of the Pandas library. This function can read a CSV file (either locally or through a URL) and also perform various     operations on it. The read_csv() is written as:
  ```
  dataset = pd.read_csv("your_data_file.csv")
  ```
  
* ### Step 3: Preprocessing Data    
  In data preprocessing, it is pivotal to highlight attributes that we’re want our machine learning system to pick up on. Cleaning (or pre-processing) the data typically consists of a number of steps:
   * Remove Punctuation (for our vectorizer which counts the number of words and not the context, punctuation does not add value)
   * Tokenization (separates text into units such as sentences or words)
   * Remove Stopwords (common words that will likely appear in any text)
   * Stemming (simply chops off suffices, like “ing”, “ly”, “s” at end of the word, without understanding the context) OR Lemmatizing (derives the canonical form ‘lemma’ of a word. i.e the root form and is better than stemming)
  
* ### Step 4: Vectorizing Data
  Vectorizing is the process of encoding text as integers i.e. numeric form to create feature vectors so that machine learning algorithms can understand our data.
  
* ### Step 5: Feature Engineering: Feature Creation
  Feature engineering is the process of using domain knowledge of the data to create features that make machine learning algorithms work. It is like an art as it requires domain knowledge and it can be tough to create features, yet fruitful for ML algorithm to predict results as they can be related to the prediction.
   
* ### Step 6: Building ML Classifiers: Model selection
  We use an ensemble method of machine learning where multiple models are used and their combination produces better results than a single model(Support Vector Machine/Naive Bayes). Ensemble methods are the first choice for many Kaggle Competitions. Random Forest i.e multiple random decision trees are constructed and the aggregates of each tree are used for the final prediction. It can be used for classification as well as regression problems.

Refer to [this article](https://towardsdatascience.com/natural-language-processing-nlp-for-machine-learning-d44498845d5b) for detailed steps and approach.

Check the code for implementation of all the above mentioned steps in Data preprocessing
  
  

