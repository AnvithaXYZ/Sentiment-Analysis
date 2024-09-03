# Real vs. Fake News Analysis and Sentiment-Based Classification

## Introduction

This project combines the tasks of real vs. fake news analysis with sentiment-based text classification. In today's digital age, it's crucial to distinguish between trustworthy news sources and understand the sentiment within text data. The project begins by analyzing real and fake news articles using Natural Language Processing (NLP) techniques, followed by building a sentiment classifier trained on a Twitter Airline Sentiment dataset to assist in detecting fake news.

## Real vs. Fake News Analysis

### Data

The analysis begins with the ISOT Fake News Dataset, which contains over 12,600 articles categorized into real and fake news, saved in two CSV files: `True.csv` and `Fake.csv`. The articles are sourced from reputable outlets like Reuters, along with articles flagged by fact-checking organizations.

### Data Preprocessing

Data preprocessing is a crucial step to prepare the text data for analysis. This includes:
- Extracting the data.
- Tokenization.
- Converting text to lowercase.
- Removing stop words.
- Lemmatization.

### Data Analysis

We conduct extensive analysis on the preprocessed data, including:
- Identifying the top 50 stop words and content words by frequency in real and fake news articles.
- Discovering the top 50 bigrams (two-word phrases) by frequency.
- Calculating the top 50 bigrams by Mutual Information scores.
- Analyzing the usage of adjective words.
- Collecting additional statistics for each article, such as total words, content words, capitalized words, exclamation marks, and punctuation marks.

### Interpretation of Analysis Results

The analysis highlights key findings that differentiate real and fake news articles, focusing on linguistic differences, writing styles, and content structures.

## Sentiment-Based Classification

### Data Preprocessing

For the sentiment analysis, we use the Twitter Airline Sentiment dataset. Data preprocessing steps include:
- Converting text to lowercase.
- Removing stop words.
- Splitting the data into training and testing sets.

### Experiments

We conduct a series of experiments to build a sentiment classifier:
- Experimenting with unigram features using `CountVectorizer` and a Multinomial Naive Bayes classifier.
- Incorporating bigram features by adjusting `ngram_range`.
- Introducing negation handling to improve model accuracy.
- Creating a sentiment lexicon using `VADER SentimentIntensityAnalyzer` and training a Logistic Regression model.

### Final Model

The final model is a Multinomial Naive Bayes classifier trained on unigram features from the Twitter Airline Sentiment dataset.

## Detecting Fake vs. Real News

With the trained sentiment classifier, we apply it to the task of detecting fake vs. real news. The process involves:
- Preprocessing and tokenizing news articles into sentences.
- Using the classifier to determine the sentiment of each sentence.
- Calculating the average number of positive and negative sentences for both fake and real news articles.

## Conclusion

This project demonstrates a comprehensive approach to analyzing real vs. fake news and building a sentiment-based classification model. The experiments showed that feature selection significantly impacts model performance, with the sentiment lexicon model outperforming others. The models developed have practical applications, such as distinguishing between fake and real news based on sentiment analysis.

With a strong foundation in NLP and sentiment analysis, this project offers valuable insights into the classification of digital information and the distinction between real and fake news.

