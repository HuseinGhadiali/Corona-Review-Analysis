# Corona Industrial - Columbia

Corona Industrial (Corona) is a Colombian multinational company with 140 years of expertise in the manufacturing and distribution of products and solutions for the home & home improvement, construction, industry, agriculture, and energy sectors. It consists of four Business Divisions – Kitchen & Bath; Surfaces, Materials & Paints; Tableware; and Industrial Minerals & Energy – two Commercial (sales) Units that are Almacenes Corona and Corona Commercial Colombia – and Transversal Support Functions. It is also the parent company for the well-renowned company Mansfield - https://www.mansfieldplumbing.com/why-mansfield/about-mansfield/corona/

# Goal

This project involves analyzing customer reviews from https://www.lowes.com/ for various Mansfield toilets using NLTK's VADER sentiment analysis tool and a pre-trained sentiment analysis transformer model from Hugging Face, which is trained on an Amazon review dataset.

# Data Preprocessing

The data preprocessing step involves merging multiple CSV files into one master CSV file, checking for null values, dropping unnecessary columns, fixing encoding issues, mapping treebank part of speech tags to WordNet part of speech tags, and preprocessing text by removing punctuation, stop words, and lemmatizing.

# Data Exploration

The data exploration step involves checking the duration of the dataset, checking the distribution of total stars, checking if all models have the same price, finding dates when most reviews were written, finding the top-selling product, finding phrases in reviews with 4 or 5 stars, creating bi-grams and tri-grams for both positive and negative reviews. Additionally, isolated the most negative review with the highest like count and the most positive review with the highest like count to understand what customers dislike and like the most about the toilets respectively. Also, identified competitors using NLTK's proper noun and named entity recognition.

## Data Exploration
![Alt text](DataExploration.png)

## Most liked postivie comment
![Alt text](LikedPos.png)

## Most liked negative comment
![Alt text](LikedNeg.png)

## Identifying customer preferences over Mansfield
![Alt text](Competitors.png)

# Sentiment Analysis

The sentiment analysis step involves initializing a sentiment analyzer and defining a function to extract positive and negative phrases from a review. The function is applied to each review to create new columns for positive and negative phrases. The data is then grouped by model to extract the most common positive and negative phrases. Word clouds are created for the most common positive and negative phrases.

In addition to using NLTK's VADER sentiment analyzer, this project also uses a pre-trained transformer model from the Hugging Face library to perform sentiment analysis on customer reviews. The model is used to classify each review as either positive or negative, and the results are used to analyze positive aspects in negative reviews and negative aspects in positive reviews.

## Positive Aspects in Negative Reviews
![Alt text](PosinNeg.png)

## Negative Aspects in Positive Reviews
![Alt text](NeginPos.png)

