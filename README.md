# NLP Task Implementation with HuggingFace Pipelines

## Overview

This repository contains implementations for two distinct NLP tasks:

1. **Fill-Mask Task:** Replicating Tables 3 and 4 from a referenced paper using HuggingFace pipelines and three different models (at least one being BERT).
2. **Translation and Feature Extraction:** Translating paper titles and abstracts between languages, obtaining vector representations using `allenai/specter2_base`, and analyzing cosine similarities to study the effect of translation on vector representations.

## Task Details

### Task 1: Fill-Mask Task

- **Objective:**
  Use HuggingFace pipelines to replicate results presented in Tables 3 and 4 of the referenced paper.

- **Approach:**
  1. Use at least three different pre-trained models, including `bert-base-uncased`.
  2. Extract predictions for masked tokens in the sentences used in Tables 3 and 4.
  3. Compare the performance metrics for each model and document the results.

- **Output:**
  Replicated tables showcasing model performance.

- **Code Location:**
  [fill_mask_task.py](fill_mask_task.py)

### Task 2: Translation and Feature Extraction

- **Objective:**
  Analyze the effect of translation on vector representations of research paper titles and abstracts.

- **Steps:**

  1. **Author Matching:**
      - Input a name (e.g., `Noah Smith`).
      - Retrieve the top three author IDs from Semantic Scholar, sorted by citation count.
  
  2. **Paper Retrieval:**
      - For each author, retrieve their top four papers (sorted by citation count).
      - Extract titles and abstracts of these papers.

  3. **Translation:**
      - Translate titles and abstracts to Chinese and back to English.
      - Repeat with French translations.

  4. **Feature Extraction:**
      - Use `allenai/specter2_base` to extract vector representations of paper titles and abstracts.
      - Obtain vectors for original and translated versions.

  5. **Cosine Similarity Analysis:**
      - Compute cosine similarities of vectors before and after translation.
      - Compare vectors obtained from Chinese and French translations.

  6. **Visualization:**
      - Plot cosine similarities using:
        - `imshow` for heatmaps.
        - `boxplot` for distribution comparisons.

  7. **Analysis Questions:**
      - Does translation affect the vectors?
      - Does translation improve or degrade the vectors?
      - Are French translations better or worse than Chinese translations for comparing papers?
      - Propose metrics to make these questions precise.

## Note

This project was developed as an independent effort in the CS6120 Natural Language Processing course. 
