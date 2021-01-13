# Fetch_similarity

This repository contains 2 approaches one that hase been asked to implement and another extra approach using libraries.

The following is the code flow:

1) We first convert all the words in each document into lower case and split them by space.

2) We then check for the valid word format using a regex condition.(This is called stemming)

3) We can the lemmatize the words i.e, get the core word(ex: doing --> do, helpful -->help etc).Currently this is not implemented as it needs a model to be trained.

4) Then we filter out the lists obtained in step 3 using the custom stopwords(like a ,an,the ,you etc) list to get the meaningful words out.

5) Then we create a corpus of all the unique words from all the documents(This will be our master corpus).

6) For each word in the unique data we check for each sentence how many times the word gets repeated in it.

7) This gives us the term frequency list(putting in dictionary)

8) We them calculate the Inverse document frequency for each word in the unique data list.

9) This can be done by checking how in how many documents a particular word appears and dividing the number of documents by the word appearence number.

10) Multiplying the two values will give us the TF-IDF value for each document.

11) We can then use this to calculate the cosine similarity between 2 vectors.

12) Cosine similarity can be calculated by taking the (dot product of 2 vectors)/product of mod of the vectors

13) This gives us a score(numerical value between 0 to 1) on how similar 2 texts are.

14) If the queried texts are more similar the score is nearer to 1 and vice versa.
