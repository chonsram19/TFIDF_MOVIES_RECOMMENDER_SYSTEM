TF-IDF is a numerical statistic that reflects the importance of a word in a document. It is commonly used in NLP to represent the relevance of a term to a document or a corpus of documents. The TF-IDF algorithm takes into account two main factors: the frequency of a word in a document (TF) and the frequency of the word across all documents in the corpus (IDF).

The term frequency (TF) is a measure of how frequently a term appears in a document. It is calculated by dividing the number of times a term appears in a document by the total number of words in the document. The resulting value is a number between 0 and 1.

The inverse document frequency (IDF) is a measure of how important a term is across all documents in the corpus. It is calculated by taking the logarithm of the total number of documents in the corpus divided by the number of documents in which the term appears. The resulting value is a number greater than or equal to 0.

The TF-IDF score is calculated by multiplying the term frequency and the inverse document frequency. The higher the TF-IDF score, the more important the term is in the document.

TF-IDF = TF * IDF
TF-IDF = TF * log(N/DF)

Where:
. TF is the term frequency of a word in a document
. N is the total number of documents in the corpus
. DF is the document frequency of a word in the corpus (i.e., the number of documents that contain the word)

How does TF-IDF work?
TF-IDF is a commonly used technique in Natural Language Processing (NLP) to evaluate the importance of a word in a document or corpus. It works by assigning weights to words based on their frequency and rarity. Let’s walk through an example to better understand how TF-IDF works. Suppose we have a corpus of five documents

Doc1: The quick brown fox jumps over the lazy dog 
Doc2: The lazy dog likes to sleep all day 
Doc3: The brown fox prefers to eat cheese 
Doc4: The red fox jumps over the brown fox
Doc5: The brown dog chases the fox
Now, let’s say we want to calculate the TF-IDF scores for the word “fox” in each of these documents.

Step 1: Calculate the term frequency (TF)
The term frequency (TF) is the number of times the word appears in the document. We can calculate the TF for the word “fox” in each document as follows:

TF = (Number of times word appears in the document) / (Total number of words in the document)
Doc1: 1 / 9
Doc2: 0 / 8
Doc3: 1 / 7
Doc4: 2 / 8
Doc5: 1 / 6
Step 2: Calculate the document frequency (DF):
The document frequency (DF) is the number of documents in the corpus that contain the word. We can calculate the DF for the word “fox” as follows:

DF = 4 (Doc1, Doc3, Doc4 and Doc5)
Step 3: Calculate the inverse document frequency (IDF):
The inverse document frequency (IDF) is a measure of how rare the word is across the corpus. It is calculated as the logarithm of the total number of documents in the corpus divided by the document frequency. In our case, we have:

IDF = log(5/4) = 0.2231
Step 4: Calculate the TF-IDF score:
The TF-IDF score for the word “fox” in each document can now be calculated using the following formula:

TF-IDF = TF * IDF

Doc1: 1/9 * 0.2231 = 0.0247
Doc2: 0/8 * 0.2231 = 0
Doc3: 1/7 * 0.2231 = 0.0318
Doc4: 2/8 * 0.2231 = 0.0557
Doc5: 1/6 * 0.2231 = 0.0372
Therefore, the TF-IDF score for the word “fox” is highest in Doc4 indicating that this word is relatively important in this document compared to the rest of the corpus. On the other hand, the TF-IDF score is zero in Doc2, indicating that the word “fox” is not relevant in this document.
# TFIDF_MOVIES_RECOMMENDER_SYSTEM
