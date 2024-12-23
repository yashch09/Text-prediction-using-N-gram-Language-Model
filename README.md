# Text-prediction-using-N-gram-Language-Model
This Python project implements a text prediction system using the Laplace smoothing model with bigrams. The goal is to predict the next word in a given sentence based on the provided prefix. The project utilizes the Natural Language Toolkit (NLTK) library for processing and modeling natural language data.

How It Works
Data Preprocessing:

The project starts by reading a CSV file (train.csv) containing text data.
HTML tags are removed from the 'Body' column of the dataset using a function called remove_html_tags.
The text is tokenized using the WordPunctTokenizer from NLTK.
N-gram Model Building:

The corpus is then processed further by padding both ends of each sentence with special symbols ("" and "") using the pad_both_ends function.
Bigrams are extracted from the padded sentences using the bigrams function.
The vocabulary is constructed using the Vocabulary class from NLTK.
Laplace Smoothing Model:

The Laplace smoothing model is implemented using the Laplace class from NLTK's language modeling module.
The model is trained on the bigram data.
Next-word Prediction:

User input is taken to provide a prefix for next-word prediction.
The Laplace model scores each word in the vocabulary based on its likelihood to follow the given prefix.
The top three predictions with their respective scores are displayed.
