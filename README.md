# Computational Linguistics — Natural Language Processing

A hands-on collection of ten Computational Linguistics / NLP laboratory experiments. The work progresses from data exploration and text cleaning to classical NLP, embeddings, deep learning, multilingual summarization, document classification, and English-to-Hindi neural machine translation.

Each experiment is self-contained: its folder holds the Jupyter notebook together with the input data, generated outputs, and/or report used for that exercise.

## Experiments at a glance

| # | Experiment | What it covers |
| --- | --- | --- |
| 1 | [Exploratory Data Analysis](Experiment-1/experiment_1.ipynb) | Profiles a 100-record employee dataset with Pandas and Matplotlib. Includes descriptive statistics, departmental aggregations, salary analysis, and visualizations. |
| 2 | [Text Preprocessing & Tokenization](Experiment-2/Experiment_2.ipynb) | Cleans raw English text, compares sentence/word tokenization in NLTK, spaCy, and pure Python, and examines stopword removal. |
| 3 | [Stemming, Lemmatization & Regex](Experiment-3/Experiment_3.ipynb) | Compares Porter stemming with WordNet lemmatization, including POS-aware lemmatization. Uses regular expressions to extract emails, URLs, phone numbers, hashtags, and mentions. |
| 4 | [Term Frequency, NER & TF-IDF](Experiment-4/Experiment_4.ipynb) | Computes term frequencies and named entities with spaCy, validates frequency counts in pure Python, and builds TF-IDF scores from scratch over multiple documents. |
| 5 | [Subword Tokenization & POS Tagging](Experiment-5/Experiment_5.ipynb) | Explores BPE and SentencePiece tokenizers—pretrained and custom-trained—and contrasts NLTK and spaCy part-of-speech tags. |
| 6 | [GloVe Embeddings & N-Gram Models](Experiment-6/Experiment_6.ipynb) | Implements GloVe-style word embeddings and cosine-similarity analysis, then builds smoothed bigram and trigram language models for next-word prediction. |
| 7 | [Sentiment Analysis](Experiment-7/Experiment_7_v2.ipynb) | Benchmarks TF-IDF + Logistic Regression, LSTM, a vanilla Transformer, and fine-tuned BERT on the IMDB movie-review sentiment dataset. |
| 8 | [Hindi Abstractive Summarization](Experiment-8/experiment-8.ipynb) | Compares mT5 and mBART for Hindi abstractive summarization, evaluated with ROUGE and multilingual BERTScore. |
| 9 | [AG News Topic Classification](Experiment-9/Experiment_9.ipynb) | Classifies news into four AG News categories using a TF-IDF/LinearSVC baseline, Bi-LSTM, and fine-tuned DistilBERT. |
| 10 | [English-to-Hindi Neural Machine Translation](Experiment-10/Experiment_10.ipynb) | Evaluates low-resource English-to-Hindi translation with recurrent/Transformer approaches and pretrained multilingual MarianMT. |

Experiments 9 and 10 form a supplementary mini-project: classifying incoming English text and translating it into Hindi as part of a broader multilingual NLP pipeline.

## Repository layout

```text
.
├── Experiment-1/ … Experiment-10/   # Notebooks, data, results, and reports
├── report.tex                        # Consolidated LaTeX report source
├── report.pdf                        # Generated consolidated report (if present locally)
├── report_assets/                    # Figures used by the consolidated report
└── latex-assets/                     # LaTeX sections and report-generation helpers
```

Notable supporting files include:

- `Experiment-1/employee_information_100.csv` — employee data for EDA.
- `Experiment-2/*.txt` — text-cleaning, tokenization, and stopword inputs.
- `Experiment-4/tf_idf_outputs/` — exported TF, DF, IDF, and TF-IDF results.
- `Experiment-6/glove_corpus.txt` — corpus used for embedding and language-model exercises.
- `Experiment-7/IMDB-Dataset.csv` — IMDB sentiment dataset.
- `Experiment-8/*comparison.png` — summarization metric comparisons.

## Getting started

1. Create and activate a Python virtual environment (Python 3.10+ is recommended).
2. Install Jupyter plus the libraries required by the notebook you intend to run. The earlier experiments primarily use `pandas`, `matplotlib`, `nltk`, and `spacy`; later experiments also use PyTorch, Hugging Face `transformers`/`datasets`, `sentencepiece`, and evaluation libraries such as `rouge-score` and `bert-score`.
3. Download the required NLTK resources and spaCy language model when prompted by the relevant notebook.
4. Start Jupyter from the repository root and open the desired experiment:

```bash
jupyter notebook
```

Run each notebook from its own experiment directory when it reads local files with relative paths. The transformer-based experiments may download pretrained models or datasets and are best run with sufficient memory and, where available, GPU acceleration.

## Reports and results

Individual experiment folders contain their associated notebooks and available `.docx`/`.pdf` reports. The root-level `report.tex` brings the work together in one consolidated report; its supporting sections and assets live in `latex-assets/` and `report_assets/`.

## Scope

This repository is an educational NLP portfolio. It is designed to make the progression of techniques inspectable and reproducible rather than to provide a single deployable application.
