
# Sentiment Classification with Embeddings and Classical ML

This project demonstrates how to perform sentiment classification on text reviews using pre-trained word embeddings and classical machine learning models (Logistic Regression and Random Forest).

## Pipeline Overview

1. **Dataset Preparation**  
   Combines three sentiment datasets (`amazon5.txt`, `imdb5.txt`, and `yelp5.txt`), each containing short reviews and binary labels (positive/negative).

2. **Text Cleaning and Preprocessing**  
   - Lowercasing, punctuation removal, stopword filtering  
   - Tokenization and lemmatization using NLTK and WordNet  

3. **Vocabulary Construction**  
   Builds a vocabulary of words appearing at least twice in the training set.

4. **Word Embeddings**  
   - Embeddings for each word in the vocabulary are obtained using the `all-mpnet-base-v2` model from `sentence-transformers`.  
   - Each review is embedded as the average of its word vectors.

5. **Model Training and Evaluation**  
   - Trains Logistic Regression and Random Forest classifiers on the embeddings.  
   - Evaluates them on validation and test splits using accuracy, precision, recall, and F1-score.

6. **Comparison with Sentence-Level Embeddings**  
   - Evaluates a baseline using sentence-level embeddings from `sentence-transformers` directly.

## Required Files

Place the following files in the same directory as this notebook:

- `amazon5.txt`
- `imdb5.txt`
- `yelp5.txt`

These are small TSV files containing reviews and sentiment labels.

## Installation

Run the following commands at the beginning of your notebook or script to install all required dependencies:

```bash
!pip install openai
!pip install -q sentence-transformers
!pip install -q spacy
!python -m spacy download es_core_news_md
!pip install -q nltk
```

You may also need to run the following downloads for NLTK:

```python
import nltk
nltk.download('all')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('punkt')
nltk.download('stopwords')
```

## File

- `sentiment_classification_embeddings_classical_ml.ipynb`: Main notebook with all code, comments, and output.

## Reflections

This project helped reinforce practical NLP skills like:
- Custom preprocessing and token cleaning
- Using pre-trained embeddings
- Training and tuning traditional classifiers
- Understanding the tradeoffs of average word embeddings vs full sentence embeddings

