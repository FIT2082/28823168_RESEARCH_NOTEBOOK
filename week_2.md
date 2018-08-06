# Week 2 - Introduction

Dilpreet introduced us to our project and goals for this semester. Dave is a small robot to help guide people around SensiLab. The purpose of this project is to give Dave the ability to accurately respond to any questions a user asks. Currently only a few questions are given as example sentences that we will train our model on. For example, the following sentence: "Hey Dave what's the weather today?", will produce a question intent of *weather* allowing Dave to recognize the user is asking about the weather, and respond appropriately.

### Current state

* Dave converts speech to text via Microsoft's services.
* Corpus of example sentences and their responses
* Remove stop/common words from input
* Calculate a frequency-inverse document frequency (TF-IDF)
* Generate feature vector for sentences 
* Classify input sentences with a trained Bayes classifier to determine intent

### Goals

* Semantic understanding of words and sentences
* Feature extraction of sentences
* Using these features to predict a questions intent 

* HIGH LEVEL: Have Dave usefullly/naturally respond to questions
