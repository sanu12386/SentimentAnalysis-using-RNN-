iPhone Users' Review Sentiment Analysis using RNN
Overview
This project aims to perform Sentiment Analysis on reviews given by iPhone users using a Recurrent Neural Network (RNN). By analyzing user-generated content, such as review titles and descriptions, the project seeks to classify each review as positive or negative based on the sentiment expressed by the user. The dataset used in this project contains various features like rating score, country, review date, and more, providing additional insights into the sentiment trends across different iPhone variants and countries.

Table of Contents
Project Features
Dataset
Model Architecture
Setup and Installation
Data Preprocessing
Training the RNN Model
Evaluation and Results
Visualizations
Potential Improvements
Technologies Used
Conclusion
Project Features
Sentiment Classification: Classifies reviews into positive and negative sentiment categories.
Aspect-Based Sentiment Analysis: Extracts key features of the iPhone (like camera, battery) from reviews and analyzes the sentiment specific to those features.
Sentiment Trends Over Time: Shows how user sentiment has evolved over time, especially around new product releases.
Comparison of Verified vs Non-Verified Reviews: Analyzes sentiment differences between reviews from verified and non-verified purchases.
Variant Sentiment Analysis: Analyzes sentiment for different iPhone models or variants.
Word Clouds: Visualizes commonly used words in positive and negative reviews.
Dataset
The dataset consists of various columns that provide detailed information about each review:

productAsin: Unique product identifier for the iPhone model.
country: The country from where the review was submitted.
date: Date on which the review was posted.
isVerified: A Boolean indicating whether the purchase was verified.
ratingScore: The rating provided by the user (usually a value from 1 to 5).
reviewTitle: The title of the review, summarizing the user's experience.
reviewDescription: The full review text that details the user’s experience.
variant: The specific iPhone model or variant.
Model Architecture
The model architecture is designed to capture the context and sequence of words in reviews, making use of an RNN with LSTM layers:

Embedding Layer: Converts input words into vector representations.
LSTM Layer: Captures temporal dependencies and remembers long-term context in the reviews.
Dropout Layer: Prevents overfitting by randomly dropping units during training.
Fully Connected Dense Layer: Connects the features learned from LSTM to the final output.
Sigmoid Output Layer: Outputs the probability of the review being positive or negative.
Loss Function and Optimizer
Binary Cross-Entropy Loss: Used to measure the error between predicted and actual sentiment labels.
Adam Optimizer: Chosen for its adaptive learning rate, helping the model converge faster.
