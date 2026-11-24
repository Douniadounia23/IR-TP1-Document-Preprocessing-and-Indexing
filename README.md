# IR-TP1 – Document Preprocessing and Indexing

## 1. Project Description

This project focuses on document preprocessing, representation and indexing using Python. It uses a corpus of 10 English documents.

Three preprocessing versions are implemented:

- **Version A:** Lowercase conversion and punctuation removal.
- **Version B:** Version A + stopword removal.
- **Version C:** Version B + stemming using PorterStemmer.

## 2. Project Structure

- `tp1_preprocessing_indexing.ipynb`: Python notebook containing the implementation and verification tests.
- `requirements.txt`: Required Python packages.
- `results/`: Generated output files.

The results folder contains:
- Processed tokens (JSON)
- Vocabulary files (TXT)
- Binary matrices (CSV)
- Term-frequency matrices (CSV)
- Positional inverted indexes (JSON)
- Preprocessing comparison table (CSV)

## 3. Requirements

- Python 3
- NLTK
- pandas
- Jupyter Notebook

## 4. How to Run

1. Install the required packages:

   `pip install -r requirements.txt`

2. Open `tp1_preprocessing_indexing.ipynb` in Google Colab or Jupyter Notebook.
3. Run all cells in order.
4. The generated results are saved in the `results/` folder.

## 5. Implementation

The project uses:
- `re` for punctuation removal.
- NLTK stopwords for English stopword removal.
- PorterStemmer for stemming.
- Python dictionaries and loops to build the vocabulary, binary matrix, TF matrix and positional inverted index.
- `collections` for index construction.
- pandas to display and export matrices.

## 6. Conclusion

Preprocessing changes the vocabulary and the size of the index. Version A converts words to lowercase and removes punctuation, allowing words with different capitalization to be treated as the same term. Version B removes common English stopwords such as "the" and "and", reducing the number of tokens and usually the vocabulary size. Version C applies stemming to group related word forms under a common stem. This can improve retrieval because different forms of a word can match the same indexed term. However, stemming may sometimes merge words with slightly different meanings. Overall, preprocessing reduces index size and can improve search flexibility, but it may also affect retrieval precision.
