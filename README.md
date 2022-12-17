# Fake_News_Classifier

Fake news has become one of the biggest problems of our age. It has serious impact on our online as well as offline discourse.
More often we see conflicting facts for the same topic and wondering either it is true or not. The task to classify that either the news is fake or not can be done 
by using Python and Machine Learning.We can use classifier algorithm to train our model that can predict whether the news is fake or not.

## Resources
Google Colab Notebook for Project: [Click Here](https://colab.research.google.com/drive/1MPRy6rqmuLZBACpcmoIQg697z_ETHwk9#scrollTo=DyONN_zbQ3SL)

## About the Project
This is the project I am working on while learning the concepts of Machine Learning and Data Science.<br>
* <b>Aim</b> - The aim of the project is to build a fake news classifier using Natural Language Processing.
* We will take a dataset of labeled public-messages and apply classification techniques with frequency vectorizer like <b>Tf-idf vectorizer</b> and <b>Count vectorizer</b>. 
* In NLP(Natural Language Processing) we face stop words which we will remove using <b> Stemming Technique</b>
* We can later test different model like <b>Naive Bayes Model</b>, <b>Random Forest Model</b> and <b>K-NN (K-Nearest Neighbour)</b> for accuracy and performance on unclassified public-messages using both Tf-idf vectorizer and count vectorizer. 

## Data
I am using dataset from [kaggle.com](https://www.kaggle.com/c/fake-news/data) which contain following instances:
* <b>id</b>: unique id for a news article
* <b>title</b>: the title of a news article
* <b>author</b>: author of the news article
* <b>text</b>: the text of the article; could be incomplete
* <b>label</b>: a label that marks the article as potentially unreliable<br>
Label 1-> represent News is fake <br>
Label 0-> represent News is not fake

## Data Preprocessing and Text Cleaning
* <b>Data Preprocessing</b> - Before traing the model we have to do data preprocessing that is get the information of data structure and how many data values are null.
* <b>Text Cleaning</b> - Then after cleaning of inconsistence data. We have to do text claening i.e. removing all numbers which is attached to the letter, converting all uppercase to lowercase, replacing all \n to spaces and removing all non-Ascii characters.
* <b>Removing stop words and stemming the text</b> - In natural language processing, useless words are called stop words which on removing from the sentence does not affect the measning of sentence. Stop words like "a", "an", "the", "in", "on" etc. 
There is something called <b>Porter Stemming Algorithm</b> that is used to remove common morphological words. For more detail about the algorithm you can refer to the [link](http://snowball.tartarus.org/algorithms/porter/stemmer.html)

## Frequency Vectorizer
* <b>Tf-idf Vectorizer</b> - TF-IDF stands for “term frequency-inverse document frequency”, meaning the weight assigned to each token not only depends on its frequency in a document but also how recurrent that term is in the entire corpora.
* <b>Count Vectorizer</b> - The most straightforward one, it counts the number of times a token shows up in the document and uses this value as its weight.<br>
For more details : [Click Here](https://machinelearningmastery.com/prepare-text-data-machine-learning-scikit-learn/)

## Model
* We are using three models:
  1. <b>Naive Bayes Model</b>
  2. <b>Random Forest Model</b>
  3. <b>K-NN</b>
* We use both TfIdf Vectorizer and Count vectorizer to convert our text strings to numerical representations and initialize Naive Based Model,
Random Forest Model, K-Nearest Neighbour to fit the model.
* At the end we are comapring all different models using Confusion Matrix and Acuuracy score of scikit-learn
