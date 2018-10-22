
# Week 7 - POS Weighting

This week we investigated a way to incorporate the POS-tag of a word (determined from a NLTK model) into the FastText based classifier. FastText currently works by converting each word of a sentence into a vector and averaging them together (evenly weighting the words) to form a whole sentence vector. This sentence vector is used in a linear classifier to form a prediction. The following image illustrates FastText's architecture.

![alt text](http://wellyzhang.github.io/img/in-post/fastText/model.jpg)

We extended on this idea by instead of evenly weighting every word in a sentence, we built a system that allows for POS-tag weightings to be applied to certain words, in order to change the final vector. For example if we were to heavily weight NOUNS over ADJECTIVES, when a noun like WEATHER is found in a sentence it heavily weights the entire sentence towards the vector of WEATHER. This should techinically make it much easier for the linear classifier to distiniguish different categories. But what are the optimal weightings? We can take a guess at weightings that would improve our model but there must be a better way, which we will look into next week.
