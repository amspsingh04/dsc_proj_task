## DSC Project Team Lead Submission - Shourya Pratap Singh
Dataset used is Sentiment140 which has about 1.6 million tweets classified into positive, negative and neutral(in some cases we classify into just negative and positive to make the computation easier otherwise Kaggle and my ISP will block me)

nbk1 uses shows how we can use TFIDF Vectorizer, Support Vector Machines and Naive Bayes algorithms to create our models

we use nltk to remove the stop words, punctuations, repeating characters and urls that may occur in our text, thereafter performing stemming and lemmatization on the textual data, in order to be able to obtain meaningful vector embeddings of the words 


nbk2 uses GloVE to provide globalised vector embeddings for the words, doing the preprocessing in a similar manner as with nbk1 using nltk, and then using a bidirectional lstm model with requisite dense and dropout layers

nbk3 uses nltk and tokenizers the same way as before, and thereafter uses a customised neural network which has a vector embedding layer for the text based data, followed by using a global average pooling 1D layer for downsampling and dimensionality reduction, followed by using dense layers and adam optimiser


on my server, while using gpus, i could achieve a 83% accuracy rating with nbk1 methods, 86% accuracy rating with nbk2 method and about 85% with nbk3 methods, however i was not able to, due to lack of computation and otherwise due to errors i dont think i have understood yet (wordnet caused an issue in nbk1 is one i still dont understand) we might achieve a lesser accuracy, however the least i achieved even when using Kaggle was ig 77%, not more than 10% lesser than that which i report through my local machine

i have made it into an ipynb so once can use it on Kaggle or colab, and in nbk3 i have also tried to make it interactive while displaying output. one can use this to obtain an (dot)h5 or a (dot)pt model file, or with a few fixes we can also obtain a (dot)keras file

this was developed in a very short time period because of my other ailments and wouldn't have been possible w/o gpt4, stackoverflow and the LBDL, thanks to them haha 

v0.1 -@amspsingh04
