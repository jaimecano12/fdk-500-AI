# Robust Environmental Sound Recognition on FSD50K

This repository contains the code and notebooks for our final project on robust multi-label environmental sound classification using the FSD50K dataset. The goal of the project is to detect multiple sound events that may appear in the same audio clip and to compare different modeling approaches under both clean and noisy conditions.

The project compares three levels of modeling complexity:

1. A baseline MLP model using handcrafted audio features.
2. A CNN model based on spectrogram inputs.
3. An Audio Spectrogram Transformer (AST) model using pre-trained transformer-based audio representations.

In addition to standard evaluation, we also perform robustness testing by adding controlled noise to the evaluation audio and measuring how model performance changes.

## Team Members

- Jaime Cano Morano
- Ilias Mahfoud Benhaddou

## Repository Structure

The main project notebooks are:

```text
01_data_loading_eda.ipynb
02_baseline.ipynb
03_label_correlation_analysis.ipynb
04_cnn.ipynb
05_ast.ipynb
06_robutness.ipynb


Dataset

This project uses the FSD50K dataset:

FSD50K: an open dataset of human-labeled sound events

The dataset is not included in this repository because of its size. It must be downloaded separately from the official FSD50K source.

After downloading the dataset, place the audio files and metadata in the expected directory structure used by the notebooks. Depending on your local setup or Google Drive structure, you may need to update the dataset paths at the beginning of each notebook.

A typical structure is:

FSD50K/
│
├── FSD50K.dev_audio/
├── FSD50K.eval_audio/
├── FSD50K.ground_truth/
│   ├── dev.csv
│   ├── eval.csv
│   └── vocabulary.csv

