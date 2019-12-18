Homework 9 for MAIL.RU GROUP ML course --- searching similar docs. There are 3 approaches:

1) Naive algo
    Constructs a set of important words, according to it each document is assigned a vector V = (k1, k2, ..., kn), where n - capacity of built set of words, ki - how many words from the i-th position of built set in the document. Then we calc the cosine between the docs. The larger the cosine, the more similar the docs.

2) TF-IDF algo
    Same as naive, but TF*IDF is on i-th position of vector. TF is term frequency --- the ratio of the number of occurrences of a word to the total number of words in a document. IDF is inverted document frequency. Document frequency is the frequency with which a certain word occurs in collection documents. It should be inverted as less frequent words should be more valuable.

3) word2vec algo
    It uses documents semantics to cunstruct a basis for words. Every word not from basis is constructed with those who is from basis. So we can compute a mean vector of document words and find the cosines between docs.
