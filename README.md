Artificial Intelligence — Text Cleaning and Corpus Alignment

This repository contains the AI coursework and NLP cleaning tasks performed in Google Colab.
The focus is on text preprocessing, corpus alignment, and data preparation for downstream AI and NLP models.


Project Overview

This project demonstrates how multiple text datasets were cleaned, aligned, and analyzed using Python-based data preprocessing techniques.
It combines datasets like TURK Corpus, Amazon Reading-Level Texts, and simplification corpora to prepare them for AI and language modeling tasks.


Files in this Repository

File Name:                    Description
--------------------------------------------------------------------
cleaned_tune.8turkers.organized.csv   Cleaned dataset containing simplified and complex sentence pairs (TURK Corpus)
cleaned_test.8turkers.organized.csv   Validation/test data for sentence simplification
cleaned_amazon.csv                    Cleaned Amazon Reading-Level corpus (Elementary vs. Intermediate)
Links Google Collab                   Reference links to Google Colab notebooks used for data cleaning
README.md                             Documentation explaining datasets and methodology


Data Cleaning Workflow

All preprocessing was performed in Google Colab using Python (pandas, regex, tqdm).

Steps Performed:
1. Removed HTML tags, punctuation, and URLs
2. Converted text to lowercase and normalized spaces
3. Removed empty or duplicate rows
4. Detected source and target language columns automatically
5. Saved cleaned data as CSV files for later analysis or machine learning input


Exploratory Data Analysis (EDA)

Each dataset was analyzed for:
- Sentence length distributions
- Duplicate and null entries
- Random before/after text samples for manual verification
- Histograms showing text complexity and vocabulary variation


Output Datasets

After cleaning, the following CSV files were generated:

Dataset Name         Records   Columns   Output File
-------------------------------------------------------------------
TURK Corpus          1,999     2         cleaned_tune.8turkers.organized.csv
TURK Test Corpus       358     2         cleaned_test.8turkers.organized.csv
Amazon Corpus           14     2         cleaned_amazon.csv


Key Insights

- TURK Corpus contains parallel complex-simple sentence pairs, suitable for text simplification models.
- Amazon Corpus represents text written at different reading levels for readability classification.
- All datasets are cleaned, normalized, and ready for NLP tasks such as text simplification, classification, or language modeling.


Tools and Libraries Used

Python 3.10+
Pandas - data manipulation
Regex (re) - text normalization
Matplotlib - basic EDA plots
tqdm - progress tracking
Google Colab - execution environment


Example Colab Snippet

import pandas as pd, re

df = pd.read_csv("/content/cleaned_tune.8turkers.organized.csv")
df['text'] = df['text'].str.lower()
df = df.drop_duplicates().dropna()
print("Shape after cleaning:", df.shape)
df.to_csv("/content/cleaned_tune_final.csv", index=False)


Google Colab Links

All notebooks used in this project are linked in the file named: Links Google Collab


Author

Zakariya2627
Artificial Intelligence Coursework
October 2025
Tools: Google Colab, Python, GitHub


License

This repository is created for educational and research purposes only.
All datasets belong to their respective original sources (TURK Corpus, Amazon, etc.).
