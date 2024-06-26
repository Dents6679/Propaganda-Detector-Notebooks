# Propaganda Detection and Classification

This repository contains code and data for detecting and classifying propaganda techniques in text using two models: a Multi-N-gram model and a GPT-2 based model.

These two tasks are based off of Task 11 of the 2020 International Workshop on Semantic Evaluation (SemEval). 

The report for this project can be found in the file `Accompanying Report.pdf`.

## Overview

### Dataset

The dataset includes 2994 text spans labeled with one of nine propaganda techniques extracted from news articles, split into 80:20 train/test sets.

### Tasks

1. **Span Identification**: Binary classification to detect the presence of propaganda.
2. **Technique Classification**: Multi-class classification to identify specific propaganda techniques.




### Models

- **Multi-N-gram Model**: Uses N-grams to classify text based on language patterns.
  
  ![image](https://github.com/Dents6679/Propaganda-Detector-Notebooks/assets/36710174/fd4e933c-4dfa-4d01-814e-1e8c13d4a5b0)

- **GPT-2 Model**: Uses the GPT-2 transformer model for contextual information logits to feed into a regression head for classification.
  
  ![image](https://github.com/Dents6679/Propaganda-Detector-Notebooks/assets/36710174/a425c731-3aa3-4b52-9d3a-89eeded22ddf)
### Results

| Model              | Task 1 F1-Score | Task 2 F1-Score |
|--------------------|-----------------|-----------------|
| Unigram Model      | 0.672           | 0.368           |
| Bigram Model       | 0.639           | 0.163           |
| GPT-2 Model        | 0.890           | 0.590           |

### Further Work

- **Multi-N-gram**: Enhance smoothing techniques and reduce sparsity.
- **GPT-2**: Improve classification head, add dropout layers, and weigh span length more.
