# AI-Assisted Flower Classification for Conservation

**Course:** Applied Machine Learning (DATASCI 207) — UC Berkeley MIDS  
**Team:** Emily Lieske, Samantha Townsend, Elaine Chan, David Diaz

## Overview

This project develops and compares deep learning models for automated flower species 
classification to support conservation efforts. By leveraging computer vision, the goal 
is to provide conservationists and researchers with a scalable tool to identify flower 
species from images — reducing the time and expertise required for manual identification 
in the field.

We trained and evaluated multiple CNN architectures, comparing a custom baseline model 
against state-of-the-art pretrained networks to determine the most effective approach 
for this classification task.

## Models Compared

| Model | Type |
|---|---|
| Baseline CNN | Custom-built from scratch |
| DenseNet121 | Pretrained, fine-tuned |
| EfficientNet | Pretrained, fine-tuned |
| ResNet | Pretrained, fine-tuned |

## Dataset

This project uses the [Petals to the Metal — Flower Classification on TPU](https://www.kaggle.com/competitions/tpu-getting-started) 
dataset from Kaggle, containing 104 flower species across ~12,000 training images 
stored in TFRecord format.

To download the dataset:
1. Create a [Kaggle account](https://www.kaggle.com) if you don't have one
2. Accept the competition rules at the link above
3. Download the data via the Kaggle API:
```bash
pip install kaggle
kaggle competitions download -c tpu-getting-started
```
## Project Structure
```
├── Preprocessing.ipynb                         <- Data loading, augmentation pipeline,
│                                                  and TFRecord parsing
├── Townsend207EDA.ipynb                        <- Exploratory data analysis and
│                                                  class distribution visualizations
├── Townsend209EDA.ipynb                        <- Extended EDA
├── baseline_cnn_training.ipynb                 <- Custom CNN trained from scratch
├── samantha-townsend-pretrained-densenet121    <- DenseNet121 transfer learning
├── EfficientNet.ipynb                          <- EfficientNet transfer learning
└── ResNet.ipynb                                <- ResNet transfer learning
```
## Disclaimer
This repository is for academic purposes only. While the dataset and methods are real, the project is exploratory in nature and should not be interpreted as definitive scientific research or policy guidance.
