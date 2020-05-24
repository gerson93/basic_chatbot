# This is a basic chatbot

## Here you have an example of chatbot with NLTK, working with a txt file about "lavado de mascarillas".
## The idea is simple:

1. First we import all we need
2. Then we read our file, and configure somethings:
  * the *content* in lower case,
  * the *stopwords* and the "stemmer" in spanish,
  * and *sent* tokenize the content sentence by sentence

3. The main function, *GenerateAnswer*, request for an user's input. We add this request to *sent*, and TfidfVectorizer takes the function stemmm and return to *tfidf_vectorizer_vectors* the results of the training with the content of *sent*. The function *stemmm* takes each sentence from *sent* tokenize the sentence word by word, and each tokens goes to the stemTokens function. This function *stemmize* this tokens, and returns it.
4. Before that, we find the cosine similarity with cosine_similarity function, between the input and the content of *sent*. We look for the most similar sentence to our input, and we show it throw the last return **sent[id_sent]**.
5. If we didn't find any similar content, if **request_tfidf == 0**

