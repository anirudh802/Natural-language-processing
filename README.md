# Finding relevant paragraphs and answering bbased on those

In this task we had to do two things.
Firstly to get the five most relevant paragraphs.
And then to answer the given question based on those.

For doing the first task I employed three methods.

###### 1. Counting keyword frequency in the question and the paragraph.

This was my first approach to tackle this problem.
This was a naive approach as it does not give higher weight to more significant keywords.
After this I tried using nltk.Rake to find keywords with their weights but this library also did not work

###### 2. Using Tfidf to get word vectors and using cosine similarity to find the most relevant paragraphs.

Next was to use tfidf vectors as it give higher weightage to the more significant words.
But i again faced a problem as this approach worked well in getting related topics but could not capture the relevance of the question.

###### 3. Using GLoVe embeddings to find the most similar.

Lastly i tried using word embeddings
first i tried using Word2vec embeddings but the library did not work correctly as some terp module was depricated
So i shifted to Glove embeddings
they work well but take a long time (approx. 5 minutes)

### How to run

clone the github repo and then run all the codeblocks in the nlptask.ipynb file
in the last code block edit the question to whatever the question you would like to ask and then wait fro some time to get the results

### model on the run



we can see that the the model performs better on tfidf and frequency approaches than on the word embedding approach which is surprising
and possibly due to it also matching the general sentiment rather than the context

