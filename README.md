# Natural-Language-Processing-with-Disaster-Tweets
## Overview
This project is part of a Kaggle competition that aims to classify tweets as either related to a disaster or not. The goal is to build a deep learning model that can accurately predict whether a given tweet describes a real disaster.
## Steps and Approach
1.Data Preprocessing:

  Cleaned the text data by removing special characters, URLs, and extra spaces.
  Filled missing values in the keyword and location columns.
  Performed tokenization and padding to ensure uniform input length for the models.
  Created embeddings using pre-trained GloVe vectors to capture semantic meaning.

2.Model Selection and Tuning:

  Built and tuned two different deep learning models:
  LSTM model: Tuned hyperparameters including learning_rate, batch_size, dropout_rate, and LSTM units. Achieved an F1 score of 0.6011.
  GRU model: Tuned hyperparameters including learning_rate, batch_size, dropout_rate, and GRU units. Achieved an F1 score of 0.6011.
  Used EarlyStopping to prevent overfitting by monitoring validation loss during training.
  Handled class imbalance by applying class weights, giving more importance to disaster-related tweets.

3.Evaluation:

  The models were evaluated using the F1 score, which balances precision and recall, making it a suitable metric for imbalanced datasets.
  Both models achieved a final F1 score of 0.6011 on the validation set.

4.Submission:

  Generated predictions for the test set using the best-performing model (based on hyperparameter tuning).
  Submitted the predictions in the required CSV format (id, target).
