NLP Pipeline for Literary Text Analysis using NLTK

This project implements a complete Natural Language Processing (NLP) pipeline for literary texts obtained from Project Gutenberg. The workflow covers data ingestion, text cleaning, preprocessing, vector representation, and semantic analysis using classical NLP techniques.

The goal is to compare different text representation methods and evaluate their ability to capture semantic relationships between chapters and document fragments.

Project Objectives
Build a reproducible NLP pipeline using NLTK.
Clean and preprocess raw literary texts.
Transform text into numerical representations.
Compare Bag of Words, TF-IDF, and Word Embeddings.
Analyze semantic similarity between chapters.
Perform clustering and exploratory semantic analysis.
Dataset

Source:

Project Gutenberg

Suggested books:

Frankenstein — Mary Shelley
Moby Dick — Herman Melville
Pride and Prejudice — Jane Austen

The pipeline can be applied to any public-domain literary text available from Project Gutenberg.

Pipeline Overview
1. Data Ingestion and Segmentation

The raw text is downloaded and cleaned by removing Project Gutenberg headers and footers.

The book is segmented into:

Chapters
Paragraphs
Sentences

Output:

Structured text stored in lists or DataFrames.
2. Text Preprocessing

Using NLTK, the following preprocessing stages are applied:

Word tokenization
Lowercase conversion
Stopword removal
Punctuation removal
Number removal
Lemmatization (or stemming)

Example:

Original Text:

"It was a bright cold day in April, and the clocks were striking thirteen."

Processed Text:

bright cold day april clock strike thirteen

3. Vector Representations

Three classical approaches are implemented:

Bag of Words (BoW)

Represents documents through word occurrence counts.

Advantages:

Easy to interpret
Simple implementation

Disadvantages:

High dimensionality
Sparse representation
No semantic information
TF-IDF

Weights words according to their importance within the corpus.

Advantages:

Reduces impact of frequent terms
More informative than BoW

Disadvantages:

Still sparse
Limited semantic understanding
Word Embeddings

Pretrained dense vector representations.

Advantages:

Capture semantic relationships
Low-dimensional dense vectors
Better generalization

Disadvantages:

Less interpretable
4. Semantic Analysis

The generated vectors are used to perform:

Cosine Similarity

Measure semantic similarity between chapters.

Applications:

Finding related chapters
Comparing beginning and ending sections
Tracking thematic evolution
Clustering

Grouping semantically similar chapters using clustering algorithms.

Possible methods:

K-Means
Hierarchical Clustering
Dimensionality Reduction

Visualization techniques:

PCA
t-SNE

These methods allow exploration of semantic relationships in lower-dimensional spaces.

Comparative Analysis

The project evaluates:

Property	Bag of Words	TF-IDF	Embeddings
Interpretability	High	Medium	Low
Semantic Information	Low	Medium	High
Sparsity	High	High	Low
Dimensionality	Very High	Very High	Low
Computational Cost	Low	Medium	Medium
Technologies
Python
NLTK
NumPy
Pandas
Scikit-learn
Matplotlib
Seaborn
Gensim
Expected Outputs
Cleaned literary corpus
Processed datasets
BoW matrices
TF-IDF matrices
Embedding representations
Similarity matrices
Clustering results
PCA/t-SNE visualizations
Possible Extensions
Compare lemmatization versus stemming.
Analyze early versus late chapters.
Store processed results in JSON or SQLite.
Measure memory usage and computational costs.
Compare multiple books from different authors.
Learning Outcomes

This project provides practical experience in:

Text preprocessing
Information retrieval
Feature engineering for NLP
Semantic similarity analysis
Vector space models
Exploratory text mining
