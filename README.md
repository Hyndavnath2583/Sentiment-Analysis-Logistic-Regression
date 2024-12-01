# Sentiment-Analysis-Logistic-RegressionSentiment Analysis
Sentiment Analysis is a process of determining the emotional tone (positive, negative, or neutral) of a piece of text. It is widely used to analyze customer feedback, social media posts, and reviews. Text data is preprocessed (tokenization, removing stopwords) and then transformed into a numerical format, followed by classification using machine learning models.

Logistic Regression
Logistic Regression is a statistical model used for binary classification. It predicts the probability of an outcome (e.g., positive or negative sentiment) based on input features. The model uses a logistic function (sigmoid) to output values between 0 and 1, representing probabilities.

Why Logistic Regression?
Simplicity: It is easy to implement and interpret.
Efficiency: Works well with smaller datasets and is computationally fast.
Probabilistic Output: Provides probability estimates, which are useful in sentiment analysis.

Challenges Faced:
Column Name Mismatch:
Issue: Initially, the dataset had inconsistencies in column names, which led to a KeyError. The column names such as 'Sentiment' or 'Text' might differ in case or spelling.
Solution: I added a dynamic check to ensure the code identifies the correct column names ('Sentiment' or 'sentiment', and 'Text' or 'text') based on the dataset, preventing any mismatch errors.
2. Data Preprocessing Challenges
Issue: Text data often includes noise such as URLs, mentions, special characters, and varying letter cases, which could affect the model's accuracy.
Solution: I implemented a custom preprocessing function to clean the text by:
Removing URLs.
Removing mentions (e.g., @username).
Removing non-alphabetic characters.
Converting text to lowercase to standardize inputs for the model.
