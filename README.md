## BERT - Topic Modelling

#### Topic Modelling using BERT

As BERT is an architecture that is capable of having Bi-Directional context, this project is an attempt to try to use BERT for topic modelling, where we try to find similarities between documents/words from different files, based on what context they appear in and the similarities between them.

In essence this was looked at as an alternative to LDA.



#### Data

-   The dataset is a Reddit web-scraped dataset containing 118k document, all not similarly formatted. The documents have been passed through a Wikifier, which has wikified some many of the words in the corpus. 
-   The data provided also is such that it has been passed through a wikifier that has removed punctuations and Wikified the data. Essentially it has identified words that have a Wikipedia page and converted them in-place to the respective wiki-tag that has the following format : `wiki__<word>__<jargons>`.
-   These wiki-words are the words of importance to us in this particular project. These are the words whose similarities and embeddings are needed.
-   Reach out to me to get access to the data.



#### Pipeline

1.  Clean and Preprocess the data.
2.  Pre-train BERT on this cleaned dataset.
3.  Extract the word embeddings of the words that we need.
4.  Run K-Means clustering using these extracted word embeddings.
5.  Generate a CSV of the findings.



-   Tasks 1 and 2 are done in [1.BERT_Pretraining](https://github.com/AceEV/BERT-TopicModelling/blob/master/1.BERT_Pretraining.ipynb)
-   Tasks 3, 4, 5 are done in [2.Word_Embeddings](https://github.com/AceEV/BERT-TopicModelling/blob/master/2.Word_Embeddings.ipynb)



#### Running the files and using the code

-   All the work in this was done on Google Colab.
-   References from multiple sources were used.
-   All the details for running the files are mentioned within the notebooks in detailed comments.
-   In brief :
    -   Start with running [1.BERT_Pretraining](https://github.com/AceEV/BERT-TopicModelling/blob/master/1.BERT_Pretraining.ipynb). Make sure to accurately set the `BUCKET_NAME` and the directories.
    -   Once done, but the `.ckpt, vocab.txt, config.json` files in a Google Drive Folder.
    -   Then run [2.Word_Embeddings](https://github.com/AceEV/BERT-TopicModelling/blob/master/2.Word_Embeddings.ipynb) with the proper paths set.
