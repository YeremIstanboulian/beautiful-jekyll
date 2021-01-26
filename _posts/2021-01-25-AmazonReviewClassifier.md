---
layout: post
title: Classifying Amazon Reviews using Naive Bayes
subtitle: Building a Naive Bayes Model to classify video gmae reviews as positive or negative
#gh-repo: daattali/beautiful-jekyll
#gh-badge: [star, fork, follow]
#tags: [test]
comments: true
---

This project started as a coding assignment for my senior year Artificial Intelligence course at UC Santa Barbara. We were assigned to write code to run the Naive Bayes algorithm from scratch in Python without using any external packages like sci-kit-learn. We were given a training set and a testing set in the form of txt files which contained the lower case text from Amazon reviews of video games with punctuation removed and an associated label of positive or negative. Although the program I wrote worked, it ran quite slowly. After finishing the course, I decided to re-do the project using iPython and sci-kit-learn. 

To read in the data I used the pandas package. I stored the training and testing data in separate pandas dataframes with 2 columns: one for the text of the review and one with the binary good review/bad review indicator. I then fit the Naive Bayes model on the training data and used the model to make predictions about the text from the testing data. 

After comparing the predictions to the observed values, the model had an accuracy of 85.3% , a precision of 86.8%, and a recall of 83% and ran in 5 seconds. I experimented implementing n-grams into the model, but with no significant improvement in my model diagnostics, I opted for the most simple Naive Bayes model.
To see the full iPython notebook
[click here](https://github.com/YeremIstanboulian/Amazon_Review_Classifier)

