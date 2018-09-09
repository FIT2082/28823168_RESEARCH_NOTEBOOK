# Week 5 - NLTK & POS tagging

### NLTK
NLTK (Natural Language Tool Kit) is a library containing plenty of useful tools for NLP. They have in-built models, sentence (and word) tokenizers, parse tree visualizers and a POS tagger. 

### POS Tagging
POS Tagging (Part-of-speech) involves tagging words with part-of-speech tags (i.e Noun, Verb, Adjective etc). Here is an example of a parse tree:
https://www.nltk.org/_images/tree.gif

This week we implemented a system using NLTK's POS tagger that was capable of classifing the words of a sentence with it's respective part-of-speech label. We split the sentence into "chunks" that matched our specified grammar. Specifically, we chunked the sentence with a rule that matched consecutive nouns and/or proper nouns. This would successfully highlight entities such as locations or names in the following sentences:
* 
