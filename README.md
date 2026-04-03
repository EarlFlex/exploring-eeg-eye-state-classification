# Exploring EEG Eye State Classification

This project explores EEG data for eye state classification (open/closed eyes) using machine learning.

## Dataset

The dataset is from the UCI Machine Learning Repository: EEG Eye State Data Set.
- 14 EEG channels
- Sampling rate: ~128 Hz
- Duration: 117 seconds
- Classes: 0 (eyes closed), 1 (eyes open)

## Features

- Band power features (delta, theta, alpha, beta) computed using Welch's method
- Alpha/beta power ratio

## Model

Random Forest classifier trained on the extracted features.

## Usage

Run the Jupyter notebook `exploring-eeg-eye-state-classification.ipynb` to reproduce the analysis.

## Requirements

- Python 3
- Libraries: numpy, pandas, scipy, scikit-learn, matplotlib