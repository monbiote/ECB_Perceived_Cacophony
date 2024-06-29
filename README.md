# One Day at a Time Cacophony Index

This repository contains the code and data for creating a Cacophony Index of Discordance for European Central Bank (ECB) council members. This index is part of a master's thesis project for a data science program.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Labeling Process](#labeling-process)
- [Model Training](#model-training)
- [Cacophony Index](#cacophony-index)
- [Usage](#usage)
- [Results](#results)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)

## Introduction

The aim of this project is to develop a Cacophony Index that measures the level of discordance among ECB council members based on their public statements. By analyzing news articles related to the ECB and its members, we classify these statements as hawkish, dovish, or neutral. This classification is used to calculate the Cacophony Index, which provides insights into the level of agreement or disagreement within the ECB council.

## Dataset

The dataset consists of news articles related to the ECB and its members. These articles were collected from various sources and cover a wide range of topics related to monetary policy and economic outlooks.

### Data Structure

- `data/raw`: Contains the raw news articles.
- `data/processed`: Contains the processed and labeled data.

## Labeling Process

We manually labeled a subset of the news articles with the following categories:

- **Hawkish**: Statements that suggest a preference for higher interest rates to curb inflation.
- **Dovish**: Statements that suggest a preference for lower interest rates to stimulate the economy.
- **Neutral**: Statements that do not clearly lean towards being hawkish or dovish.

## Model Training

We fine-tuned a pre-trained BERT model using the labeled dataset to classify the rest of the articles. The training process involved the following steps:

1. Data Preprocessing: Cleaning and preparing the text data.
2. Model Fine-Tuning: Using the labeled data to fine-tune the BERT model.
3. Evaluation: Assessing the model's performance on a validation set.

## Cacophony Index

The Cacophony Index is calculated based on the classification results of the news articles. The index measures the level of discordance among the ECB council members by considering the proportion of hawkish, dovish, and neutral statements.

## Usage

To use the code in this repository, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repository.git
    ```

2. Install the required dependencies:
    Conda environment can be set up using the ``` environment.yml ``` file
    ```bash
    conda env create --file environment.yml
    ```

3. Folders structure
```
ECB_Perceived_Cacophony
└─────ECB_Governors_Analysis
│       └─ECB_Governor_Analysis.ipynb (stores a dataset with the predicted values)
│       └─ECB_Interest_Rate_Data.ipynb (stores a dataset with the predicted values)
│       └─ECB_Members.ipynb (stores a dataset with the predicted values)
│       └─EDA_Dataset.ipynb (stores a dataset with the predicted values)
└─────Models_Notebook
│       └─bert_model.ipynb (stores a dataset with the predicted values)
│       └─dictionary_classification_model.ipynb (stores a dataset with the predicted values)
└─────OpenAI_Classification
│       └─3000_OpenAI_API_Classification_Articles.ipynb (stores a dataset with the predicted values)
│       └─ECB_Statement_Manual_Classification.ipynb (stores a dataset with the predicted values)
│       └─Manual_Classification_Scores.ipynb (stores a dataset with the predicted values)
│       └─OpenAI_API_Classification_Articles.ipynb (stores a dataset with the predicted values)
│       └─Randomised_Articles_100.ipynb (stores a dataset with the predicted values)
│       └─Randomised_Articles_3000.ipynb (stores a dataset with the predicted values)
└─────Prediction_Results
└─────Results_analysis
│       └─index.ipynb (stores a dataset with the predicted values)
│       └─merging_for_index.ipynb (stores a dataset with the predicted values)
│       └─roberta_model_application.ipynb (stores a dataset with the predicted values)
└─────roberta_model
└─────Scraping
│       └─articles_scraping_translating.ipynb (stores a dataset with the predicted values)
│       └─ECB_releases_scraping.ipynb (stores a dataset with the predicted values)
│       └─Predictions.ipynb (stores a dataset with the predicted values)
```

## Results

The results of the model training and the calculated Cacophony Index are documented in the `results` folder. This includes:

- Model performance metrics
- Visualizations of the Cacophony Index over time

## Conclusion

This project demonstrates the use of natural language processing and machine learning techniques to analyze public statements and measure discordance within the ECB council. The Cacophony Index provides valuable insights for economists and policymakers.

## Contact Information

Please raise issue on GitHub or contact either one of our members:
- Rui Maciel (rui.maciel@bse.eu)
- Edward Monbiot (edward.monbiot@bse.eu)
- Joaquin Ossa (joaquin.ossa@bse.eu)