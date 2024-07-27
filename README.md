This project performs sentiment analysis on a dataset of women's clothing reviews.
Here's a detailed summary:

1. Data Preparation:

Imports necessary libraries (pandas, numpy, matplotlib, seaborn).
Loads the dataset from a GitHub repository.
Handles missing values in the 'Review' column by replacing them with "No Review".
Defines the 'Review' column as the feature set (X) and the 'Rating' column as the target variable (y).

2. Initial Model Training and Evaluation:

Splits the dataset into training and testing sets (70/30 split) using stratified sampling to maintain class distribution.
Converts text reviews in the training and testing sets into numerical feature vectors using CountVectorizer with bigrams and trigrams, removing stop words, and limiting the vocabulary to 5000 words.
Trains a Multinomial Naive Bayes classifier on the training data.
Predicts ratings for the test set and evaluates the model's performance using a confusion matrix and classification report.

3. Recategorization and Re-evaluation:

Recategorizes ratings into binary classes: "poor" (ratings 1, 2, 3) and "good" (ratings 4, 5).
Repeats the train-test split, feature extraction, model training, prediction, and evaluation steps using the binary rating categories.

In essence, the project aims to build a model that can predict sentiment (positive or negative) from women's clothing reviews, first with a multi-class rating system and then with a simplified binary classification.
