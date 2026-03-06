# AI-Assisted Flower Classification for Conservation

**Course:** Applied Machine Learning (DATASCI 207) — UC Berkeley MIDS  
**Team:** Emily Lieske, Samantha Townsend, Elaine Chan, David Diaz

## Overview

This project develops and compares deep learning models for automated flower species 
classification to support conservation efforts. Using the Kaggle Petals to the Metal 
dataset (104 flower species), we built an end-to-end pipeline from data preprocessing 
to a live interactive web app — allowing users to see how four different models perform 
on the same image in real time.

By leveraging computer vision and transfer learning, the goal is to provide 
conservationists and researchers with a scalable tool to identify flower species from 
images, reducing the time and expertise required for manual field identification.

## Results
| Model | F1 Score |
|---|---|
| EfficientNetB0 | **0.90** |
| ResNet-50 | — |
| DenseNet121 | — |
| Baseline CNN | — |

EfficientNetB0 achieved the highest F1 score of 0.90, though all models provided 
unique insights into the trade-offs between accuracy, speed, and complexity.

## Tech Stack
- **Modeling:** TensorFlow, TPUs (Kaggle)
- **Deployment:** Netlify + ngrok
- **LLM Integration:** LLaMA 3.2 via Ollama (dynamic flower descriptions)
- **Frontend:** Interactive web app

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
## Kaggle Publications
1. https://www.kaggle.com/code/emilylieske/efficientnetb0-baseline
2. https://www.kaggle.com/code/emilylieske/efficientnetb1-hyperparameter-tuned

## Access the App
Try the interactive app: https://coruscating-panda-43f8a6.netlify.app/
Upload or select a flower image to see predictions from all four models side by side.

## Disclaimer
This repository is for academic purposes only. While the dataset and methods are real, the project is exploratory in nature and should not be interpreted as definitive scientific research or policy guidance.
