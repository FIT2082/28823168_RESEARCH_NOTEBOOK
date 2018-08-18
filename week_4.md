# Week 3 - Experiments with libraries

### Gensim
We got gensim working within a python virtual env. With a small example corpus of 15 sentences (5 topics, 3 sentences each), we removed "stop words", vectorized and did a tfdif transform on our examples. We trained a LSI model (Latent Semantic Indexing) to rank our query sentence against 15 example sentences to determine intent. 

The accuracy was admirable but could be be better. Will have to continue to test with larger corpuses.

### FastText
We got fastText working with the same dataset that we used for gensim. It's important to pre-process data for example, converting to lower case, padding punctuation with spaces (i.e "today?" becomes "today ?") this insures that fastText will recognize "today" as a word it can understand, where by adding a question mark on the end it becomes a completely different word that could be unrecognizable to fastText. 

The accuracy for fastText was good. It did a good job of correctly labelling similar sentences it had never seen before.
