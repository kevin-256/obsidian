### Preprocessing
- Lowering the case of every character
- Word Stemming: word are reduced to their stemmed form
- Lemmantization: is like stemming but with the meaning like better became good
- Stop words and punctuation: removing this words and symbols decrease the size of the representation without affect the scores (this must be done carefully)
- Regular Expressions: to remove non words like tabs and new line and replaced with one char or stripping html tags

### Bag of Words - Integers
Each word is added to a vector, representing our vocabolary, so each word gets an index.
For each phrase that we want represent, we can use a vector the same size as our "vocabolary" and for each word keep the count of how many times it appears inside the phrase.

### TF-IDF
TF-IDF = tf * idf
###### tf (Term Frequency)
for each phrase is the times a word occurs inside the phrase over the total word count of the phrase (is a float between 0 and 1)
###### idf (inverse document frequecy)
is the logarithm of the total number of documents over the number of documents that have that word

### Bag of Words - One-hot Vectors
Each word is added to a vector like in Integer version, but this time each word is represented as a vector with all zeroes except in the index that represent this word.


### Basic Word Representations – Word Embedding
Each word is represented as a vector, that is in a lower-dimensional space than the bag of words
for example for a food we can add three axes, dessertness, sandwichness and liquidness, for each food we can set a three values array with the three coordinates in space of that food.