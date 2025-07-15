### Preprocessing
- Lowering the case of every character
- Word Stemming: word are reduced to their stemmed form
- Lemmantization: is like stemming but with the meaning like better became good
- Stop words and punctuation: removing this words and symbols decrease the size of the representation without affect the scores (this must be done carefully)
- Regular Expressions: to remove non words like tabs and new line and replaced with one char or stripping html tags

### Bag of Words
Each word is added to a vector, representing our vocabolary, so each word gets an index.
For each phrase that we want represent, we can use a vector the same size as our "vocabolary" and for each word keep the count of how many times it appears inside the phrase.

### TF-IDF
