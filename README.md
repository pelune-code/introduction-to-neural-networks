# introduction-to-neural-networks

# Missing Letter Classification using LSTM

## Project Overview

This project implements a **Long Short-Term Memory (LSTM)** neural network to predict a missing letter class within a word or character sequence. The model learns contextual relationships between surrounding characters and determines the most likely missing character class, making it applicable to spelling correction, text restoration, OCR post-processing, and natural language processing tasks.

---

## Objectives

- Build a character-level sequence classification model.
- Learn contextual patterns in words using an LSTM network.
- Predict the missing letter class from surrounding characters.
- Evaluate the model using classification metrics.
- Demonstrate the effectiveness of recurrent neural networks for sequence-based tasks.

---

## Technologies Used

- Python 3.x
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## Problem Description

The task is formulated as a **multi-class classification problem**.

Given a word with one character removed, the model predicts the missing letter.

### Examples

| Input | Target |
|--------|--------|
| hxllo | e |
| compxter | u |
| machxne | i |
| progxamming | r |
| netwxrk | o |

Each English alphabet letter represents one possible output class.
(our problem is applied to Slovak words)
---

## Dataset Preparation

The dataset consists of correctly spelled words.

For each word:

1. A random character is removed.
2. The removed character class becomes the target label.
3. The remaining word (with a placeholder) becomes the input sequence.

## Data Preprocessing

The preprocessing pipeline includes:

- Filtering correct words consisting of letters of slovak alphabet
- Getting rid of duplicate words
- Character tokenization
- Sequence padding (pad (filling) is zero vector)
- Train-validation-test split (with class weights)


## Training

The model is trained using:

- Adam optimizer
- Sparse Categorical Crossentropy loss

## Model Evaluation

Performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Training and validation loss curves

## Future Improvements

- Bidirectional LSTM architecture
- GRU-based models
- Transformer-based sequence models
- Attention mechanism
- Beam search decoding
- Support for multiple missing letters
- Multilingual character prediction
- Web application deployment using Flask or FastAPI
