---
layout: post
title: "Preprocessing for text data"
date: 2019-06-06
---

Let it be the first post in the series of abut Natural Language Processing. I'll create them in the course of my research for work.

I start with one important part for machine learning, that often can be more important and play essential role in the quality of the learning of model. It's data peprocessing.
 
 All etapes , that I'll describe here are specific for preprocessing text data. Also depending on the algorithm and the model you are going to use, some can be skept or even are harmful. We'll talk about it later.
 
 Now, I want to introduce some standart etapes, that you' ll find in almost every blog or book with NLP. That's:
 
 <ul>
  <li>Lower every character in text </li>
  <li>Delete punctuation</li>
  <li>Delete stopwords (special words, that help to create a sense in sentences, but have no impact in the actually a sense)</li>
  <li>Find the most frequent and the least frequent words in the text, delete them if needed</li>
  <li>Lemmatize text</li>
  <li>Stemmatisation</li>
  <li>Tokanisation </li>
 </ul>

And there are few etapes in preprocessing, that I found useful in case of my data:

<ul>
 <li>If your data in other latin language then English, try to change special characters for the standard. Let me give you an example, In french we have è,é,à etc. that I changed for e,e,a consequently. </li>
 <li>It is possible to delete all numbers. Often it's a personal data, that has no impact in definition of the topic of text</li>
 <li>Next step, to use NER (Named-Entity Recognition) to define personal names, locations, name of organisations. Delete some of that objects</li>

</ul>
  So we know the possible etapes for text data preprocessing. Now, we can discuss which are good to use in the particular case, depending on methodes, that we want to implement.
  
  I found significant improvement of the results, using every etape for preparation of data for LDA (Latent Dirichlet Allocation).
  In the other side, after studying the principe of word embedings (word2vec and based on its fasttext, doc2vec and Glove), I made the conclusion, that etapes that suppose deleting of some words (stopwords, frequent and rare words etc.) , stemmatisation, lemmatisation can be even harmful. THe reason is that they use neural networks to train the word vectors, so the bigger vocabulary is, the better results. Also by their architecture, if the word is used to often in different contexts, the method gives it very small weights, so they don't play a role in the learning.
  
  In next posts, we will dive into most populars methods for topic modeling
