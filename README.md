# Text-Summarization
Addresses different methods and algorithms used in "Extractive" and "Abstractive" text summarization

### Extractive Summarization
The first additions to this repo include extractive text summarization methods.

In extractive summarization, we need to devise a method to calculate sentence scores and rank them accordingly, and then output the top n sentences. There are several methods to assign scores and then ranks to sentences. 
#### textsum: 
This uses word-frequency as a metric for scoring sentences. Score of each sentence is calculated as the sum of the word-frequencies of each word that is the part of the sentence. The more common a word is, the higher its frequency. Therefore a sentence with most common words will have the highest score, since the sentence contains most talked about phrases in the document.
#### textsum2: 
This uses cosine distance to calculate similarity of sentences, and hence create a similarity matrix. This similarity matrix is then plotted as an undirect graph using NetworkX, with edge weights as similarity scores. Pageranking is then used to rank the sentences. This uses the principle that sentences with higher similarities with others are capable of expressing the most talked about points in the document.
