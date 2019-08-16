# deep_sentiment
# Sentiment Analysis using Deep Learning

## Sentiment Analysis of Three University Hospitals in Thailand by Deep learning
## Introduction
One of the most important elements for businesses is to understand what their customers or clients think about the products or services that they create (customer's voice). The business owner will be able to improve their products and services with more cost-effectiveness. Thanks to the advent of online social networks which has produced online customer expression of the products or services. The sentiment analysis is one way to extract customer opinion.

Sentiment analysis is also known as opinion mining is a field within Natural Language Processing (NLP) which builds systems to identify and extract opinions within sentences. Sentiment analysis is widely applied to the voice of the customer materials such as reviews and survey responses, and social media. For the health care sector, the applications range from marketing to customer service to clinical medicine.

This study aims to understand the patient's opinion in three large university hospitals, including Ramathibodi hospital, Siriraj hospital, and Chulalongkorn hospital and use that knowledge to improve hospital services and operations quality. The patient's comments on social media are retrieved, then summarize into two groups, positive, and negative sentiments. The deep learning approaches are used to create models to predict the patient's opinion. The word cloud is used to visualize the positive and negative views of each hospital.

## Methodology
The study methodology consists of ten phases, range from web scraping which retrieves patient's comments on social media to word cloud that visualizes the top ten positive and negative opinions of the patient who receives care or interact with a service provided by three large university hospitals in Thailand.

### 1. Data Retrieval

The patient's comments with satisfaction scores of three hospitals were retrieved from www.honestdocs.co, the score range from one (low satisfaction) to five (high satisfaction).

### 2. Data Translation

Since the www.honestdocs.co reviews all Thai's hospitals, most of the comments are written in Thai. In this study, we aim to analyze the document in English. As a result, we used Google cloud translate API to translate Thai's comments into English.

### 3. Data Preparation

There are four steps for preparing data,

#### 3.1) Deduplication

The duplicated samples will be removed from the data set.

#### 3.2) Merging Database

The data from three different sites were merged.

#### 3.3) Class Labeling

The comment's score will be transformed into three categories, including negative sentiment, neutral sentiment, and positive sentiment. The neutral sentiment will be excluded from this study as the study aims to discover positive and negative opinions.

#### 3.4) Class Balancing

The dataset's classes will be balanced by using the number of smallest class as the class balancing number.

### 4. Data Splitting

The dataset was split into three sets, including train set, validate set, and test set with splitting ratio at 60: 20: 20

### 5. Data Preprocessing

The data preprocessing consist of 6 steps including,

####   5.1) Lower Case
The capital letter will be lower case to the non-capital letter.

####  5.2) Word Normalization
The word such as "I'll", "I'm" will be normalized to the full sentence (I will, and I am).

####  5.3) Word Lemmatization
The process of grouping the inflected forms of a word so they can be analysed as a single item. for example, "nation", "national", and "nationality" will be arranged into the word "nation".

####  5.4) Punctuation Removal
All punctuation will be removed.

####  5.5) Stopword Removal
A stop word is a commonly used word (such as "the", "a", "an", "in") that a search engine has been programmed to ignore, both when indexing entries for searching and when retrieving them as the result of a search query. These kinds of words will be removed.

####  5.6) Sequence Padding
The sequence padding helps input data contains the same length according to the deep learning model requirement.

### 6. Pre-trained Embedding

The word embeddings, also called word vectors, is one of the powerful ways to associate a vector with a word. The word embeddings are learned from data. Sometimes, we have an inadequate number of samples in training data that could not learn an appropriate task-specific embedding of your vocabulary. Instead of learning word embeddings from our data, we could be loading embedding vectors from a pre-trained embedding. In this study, the GloVe (Global Vectors for Word Representation), the popular pre-trained embedding is used to vectorize word in dataset.

### 7. Model Experiment

The model experiment consists of three components, firstly, create a list of hyperparameter combination, secondly, create the model for the experiment, lastly, execute the model.

####   7.1) Hyperparameter Combination
The list of hyperparameter combination is created in order to perform fine-tune hyperparameters.

####  7.2) Model Building
The sequencing model, such as GRU and LSTM, will be used to build a model structure.

####  7.3) Model Compile
Run the models then prepare to the evaluation phase.

### 8. Model Evaluation and Visualization

The model evaluation and visualization are used several matrices to assess model performance, such as accuracy, ROC curve, PR curve. Moreover, the performance of two models (GRU and LSTM models) will be shown in several visualizations, including confusion matric, and line graph.

### 9. Analysis of Errors

The misclassification cases will be explored further in order to get the trail of errors by comparing y-predict with y-true of the test set for each model.

### 10. Word Cloud

The top ten most frequent word appear in dataset of each hospitals will be represent in word cloud.

### 11. Discussions & Suggestions & Limitations

### Contributors
https://github.com/patratorn
<p>
https://github.com/petchpanu
<p>
https://github.com/perlestot
<p>
https://github.com/jitsamaK
