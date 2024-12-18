# News-Popularity-by-NER

This project analyzes news articles using Named Entity Recognition (NER) and builds a predictive model to determine the popularity of news articles. The task involves extracting named entities from news article titles, performing feature engineering, and training a model to predict article popularity based on engagement metrics. The model also showcases the correlation between popular news and fake/real news.

## Project Overview
This project aims to:
• Analyze news articles to extract relevant named entities (e.g., organizations, locations, persons) using open-source NER models (SpaCy).
• Engineer numerical features based on these entities and other characteristics (e.g., sentiment, article length).
• Build a machine learning model to predict article popularity.
• Analyze the correlation between popular news and fake/real news.

## Dataset
The following datasets were used in this project:

• Politifact Real
• Politifact Fake
• GossipCop Real
• GossipCop Fake

Each dataset contains articles with metadata, including:
• id: Unique identifier for the article
• news_url: URL of the article
• title: Title of the article
• tweet_ids: List of tweet IDs sharing the article
• source: The source of the article (e.g., Politifact, GossipCop)
• label: Binary classification label (0 for real news, 1 for fake news)

### Preprocessing
The preprocessing steps include:

1. Cleaning the text:
• Removed unnecessary whitespace, HTML tags, and special characters.
• Converted text to lowercase.

2. Tokenization:
• Tokenized the text into words.
• Removed stop words to ensure important terms are preserved.

## NER and Feature Engineering
Named Entity Recognition (NER)
We used the SpaCy library for Named Entity Recognition (NER) to extract the following entity types:

• ORG (Organizations)
• PERSON (Persons)
• GPE (Geopolitical Entities, such as countries, cities)

### Features Engineered
Based on the NER output, we created the following features:
• Entity Counts: Count of each entity type (ORG, PERSON, GPE).
• Article Length: The number of words in the article title.

Additional features were created to capture more insights about the articles.

## Predictive Modeling
We built a Random Forest Classifier to predict the popularity of news articles based on the engineered features.

## Model Training and Evaluation
1. Split the data into training and testing sets.
2. Trained a Random Forest Classifier using the training data.
3. Evaluated the model using accuracy, precision, recall, F1-score, and confusion matrix.

### Performance Metrics:
• Accuracy: 78%
• F1-Score for Fake News: 52%

## Results and Evaluation
The model was able to predict the popularity of news articles with a reasonably high accuracy of 78%. However, there is room for improvement in the classification of fake news articles, where the model's F1-score was lower.

## Model Evaluation
A confusion matrix was used to analyze the model's performance, showing how well the model differentiated between fake and real news.

## Visualizations
Several visualizations were created to help understand the relationship between features and article popularity:
Bar Charts: Frequency of named entities in the dataset.
Scatter Plots: Correlation between engagement metrics and predicted popularity.
Heatmaps: Show the relationship between entity counts and engagement.

## Conclusion
This project demonstrates the effectiveness of using Named Entity Recognition (NER) in analyzing and predicting news article popularity. While the model performs reasonably well, further improvements can be made, especially in distinguishing fake news from real news.


## Acknowledgments
• SpaCy for NER functionality.
• The datasets (Politifact, GossipCop) for providing real and fake news articles.
