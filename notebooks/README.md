# Amharic Named Entity Recognition (NER) Dataset Labeling

This project focuses on creating a manually labeled dataset in CoNLL format for Named Entity Recognition (NER) in Amharic sales messages. The goal is to identify and tag specific entities such as **Products**, **Prices**, and **Locations** within the text.

## Project Structure (So Far)

This repository contains the scripts used for:
* **Task 1:** Initial dataset loading and setup for text processing.
* **Task 2:** Interactive manual labeling of a subset of the Amharic messages into the CoNLL format.

## Tasks Completed

### Task 1: Data Preparation and NLTK Setup

**Objective:** To load the raw dataset (assumed to be a CSV file with a 'Message' column) and prepare the environment for text processing, specifically tokenization using NLTK.

**Details:**
* The project expects a CSV file containing Amharic messages, with at least two columns: 'Message ID' and 'Message'.
* The `nltk` library is utilized for word tokenization. Crucially, the `punkt` and `punkt_tab` tokenizers are downloaded to ensure proper functioning of `word_tokenize` for Amharic text. This step is handled programmatically at the start of the labeling script.

### Task 2: Manual CoNLL Labeling

**Objective:** To manually label a subset (30-50) of the Amharic messages in the CoNLL format, a standard format for NER tasks.

**CoNLL Format:**
Each token (word) is placed on a new line, followed by its corresponding entity label, separated by a tab. Blank lines are used to separate individual sentences or messages.

**Entity Types Used:**
* **B-Product**: Beginning of a product entity.
* **I-Product**: Inside a product entity.
* **B-LOC**: Beginning of a location entity.
* **I-LOC**: Inside a location entity.
* **B-PRICE**: Beginning of a price entity.
* **I-PRICE**: Inside a price entity.
* **O**: Outside of any defined entity.
### Task 3: Fine Tune NER Model 
  **Objective: Fine-Tune a Named Entity Recognition (NER) model to extract key entities (e.g., products, prices, and location) from Amharic Telegram messages.
### Task 4: Model Comparison & Selection
  **Objective:Compare different models and select the best-performing one for the entity extraction task.
