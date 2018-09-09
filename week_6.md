# Week 6 - Combining FastText and POS Tagging

### Market Research
Danie conducted a survey to research what kind of questions people would ask Dave. As an attempt to get an idea of how many ways your can ask one question such as "What is the weather". Since our point of view is quite biased, as in, we understand how the system works so it can be difficult to ask an unbias, but still realistic, question to Dave.

### The Experiment
This week I built a quick system with a few layers that was more of a proof of concept of how we can use the tools we have researched to have Dave respond to questions.

The first layer involved a simple fastText model to form a prediction of the intent of a question. This model was trained on a few example conversations for each intent. 

The second layer handles feature extraction. Using the NLTK POS-Tagger and some grammar rules we extract "entities" from sentences as metadata for the next layer. 

The final layer includes an individual handler for each intent, since specific intents require a certain response. The handlers are parsed the sentences entity metadata that is used to effectively form a response. 

Consider the example sentence: __"What is the weather in New York City"__

1. FastText predicts this sentence to be of __WEATHER__ intent
2. NLTK extracts the entity __"New York City"__ and parses as an argument to the __WEATHER__ handler
3. The __WEATHER__ handler treats the argument as the query location and responds with the weather

In practice, this method is only effective for a finite set of questions. Next week, we plan to improve the intent predictor (layer one).
