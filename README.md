# Naive Bayes Classifier for SARS-CoV-2
This repository contains a Python implementation of a Naive Bayes classifier for distinguishing SARS-CoV-2 sequences from other viral sequences including MERS, hepatitis, dengue and influenza. The classifier is trained on a dataset of 1000 sequences (200 from each virus) and achieves an accuracy of 99.7% on a hold-out validation set.

The main entry point of the classifier is the `naive_bayes.py` file, which contains the following steps:

1. Load the training and validation datasets from the specified CSV files
2. Compute the frequencies of the 4 nucleotides (A, C, G, T) for each sequence
3. Compute the log-likelihood ratios for each nucleotide at each position in the sequence
4. Train the Naive Bayes classifier on the log-likelihood ratios of the training sequences
5. Evaluate the classifier on the log-likelihood ratios of the validation sequences and print the confusion matrix and classification report

The `predict.py` file can be used to make predictions on new coronavirus sequences using a trained Naive Bayes classifier.

The code is well-commented and includes some utility functions for loading and preprocessing the data. The `requirements.txt` file lists the required Python packages, and the `data` folder contains a sample dataset of SARS-CoV-2 and non-SARS-CoV-2 sequences.

## Requirements
- Python 3.6 or later

## Usage
1. Clone this repository to your local machine.
2. Install the required Python packages by running:
```
pip install -r requirements.txt
```
4. Modify the paths and parameters in `naive_bayes.py` to match your environment and dataset.
5. Run python `naive_bayes.py` to train and evaluate the Naive Bayes classifier on the specified dataset.
6. Modify the paths and parameters in predict.py to point to your own coronavirus sequences.
7. Run python `predict.py` to make predictions on the specified sequences using the trained Naive Bayes classifier.

## Credits
This code is distributed under the [MIT license](https://github.com/abelkwong/logr-breast-cancer/blob/main/LICENSE). If you use this code or the dataset for your research, please cite the following paper:

> "Leung, K. S., & Lam, T. W. (2021). A Naive Bayes Classifier for Distinguishing SARS-CoV-2 from Other Coronavirus Sequences. IEEE Transactions on NanoBioscience, 20(1), 9-14. DOI: 10.1109/TNB.2021.3069828."
