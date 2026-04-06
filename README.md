# EEG Frequency Band Analysis and Classification

This project explores EEG signals to classify between open and closed eye states using frequency domain features.

## Overview

The notebook demonstrates a complete pipeline for EEG analysis:
- Data loading and preprocessing
- Signal filtering and artifact removal
- Epoching the continuous data
- Feature extraction using frequency band powers (delta, theta, alpha, beta)
- Machine learning classification using multiple algorithms
- Model evaluation and comparison

## Dataset

- **Source**: UCI Machine Learning Repository - EEG Eye State Data Set
- **Channels**: 14 EEG electrodes
- **Sampling Rate**: ~128 Hz
- **Duration**: 117 seconds
- **Classes**: 
  - 0: Eyes closed
  - 1: Eyes open

## Methodology

1. **Preprocessing**:
   - Bandpass filtering (0.5-40 Hz)
   - Artifact removal based on statistical thresholds
   - Data normalization

2. **Feature Extraction**:
   - Welch's method for power spectral density
   - Band power calculation for different frequency bands
   - Alpha/beta power ratio computation

3. **Classification**:
   - Support Vector Machine (SVM)
   - K-Nearest Neighbors (KNN)
   - Random Forest
   - Logistic Regression
   - Hyperparameter tuning with GridSearchCV

4. **Evaluation**:
   - Accuracy, precision, recall, F1-score
   - Confusion matrix analysis

## Results

Due to the small dataset size, model performance is limited. Accuracy varies between 50% and 65% depending on the random train-test split. This highlights the challenges of working with small EEG datasets and the need for more data or advanced techniques for better classification.

- Python 3.7+
- Jupyter Notebook
- Libraries:
  - numpy
  - pandas
  - scipy
  - scikit-learn
  - matplotlib
  - mne (optional, for advanced EEG processing)

## Usage

1. Ensure the dataset file `EEG Eye State.arff` is in the same directory
2. Open `eeg-eye-state.ipynb` in Jupyter Notebook
3. Run all cells in order to reproduce the analysis

## Files

- `eeg-eye-state.ipynb`: Main analysis notebook
- `EEG Eye State.arff`: Dataset file
- `README.md`: This file

## Notes

This project serves as an educational exploration of EEG signal processing and machine learning for brain-computer interfaces. The focus is on understanding the signal processing pipeline and interpreting results in the context of neurophysiology.