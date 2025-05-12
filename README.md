We want to use tf-idf vectors to implement a text search function in Python, Calculate the cosine similarity between tf-idf vecotrs using scikit-learn, Word vectors are incredibly useful for NLP use cases such as search engines. After calculating the tf-idf
vectors of a set of sentences or documents, we can use the same tfidf object to vectorize future sets of
text. Then, we can compute cosine similarity between our input vector and the matrix of other vectors
and sort by the most relevant documents.
Cosine similarities take on the range of [0, 1.0], with 0 being least similar and 1 being most similar.
Since we’re using tf-idf vectors to compute the similarity between vectors, the frequency of occurence
of a word is also taken into account. However, with a small corpus (set of documents) even “frequent”
words may not appear frequently. In the example above, “Sweden is best” is the most relevant text to
our search query “Brazil is the best”. Since the query mentions Brazil, we might expect that to be the
most relevant - however “Sweden is best” is the most similar due to the words “is” and “best”. As the
amount of documents we add to our corpus increases, less important words will be weighted less and
have less effect on our cosine similarity calculation
