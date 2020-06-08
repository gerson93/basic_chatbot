# This is a basic chatbot

## Here you have an example of a chatbot with NLTK, working with a txt file about "lavado de mascarillas". You can ask for information about how you can wash your mask, and the chatbot will answer you.

## The idea is simple:

1. First, we will import all we need

2. Then, we will read our file, and configure some things:
   * the *content* in lower case,
   * the *stopwords* and the "stemmer" in spanish,
   * and *sent* tokenize the content sentence by sentence

3. The main function, *GenerateAnswer*, request for an user's input. We add this request to *sent*, and TfidfVectorizer takes the function stemmm and return to *tfidf_vectorizer_vectors* the results of the training with the content of *sent*. The function *stemmm* takes each sentence from *sent* tokenize the sentence word by word, and each tokens goes to the stemTokens function. This function *stemmize* these tokens, and returns it.
4. Before that, we find the cosine similarity with cosine_similarity function, between the input and the content of *sent*. We look for the most similar sentence to our input, and we show it through the last return **sent[id_sent]**.
5. If we didn't find any similar content, if **request_tfidf == 0**

The next step will to control the accuracy of answers, and read more articles or texts.
