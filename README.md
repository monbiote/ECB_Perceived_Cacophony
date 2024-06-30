# Unified Voice or Cacophony? A Discordance Index of the European Central Bank Governing Council Members

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

The aim of this project is to develop a Cacophony Index that measures the level of discordance among ECB council members based on their public statements and how the media perceives it. By analyzing news articles related to the ECB and its members, we classify these statements as hawkish, dovish, or neutral. This classification is then used to build the Cacophony Index, which provides insights into the level of agreement or disagreement within the ECB council.

## Dataset

The dataset consists of news articles related to the ECB and its members. These articles were provided by the Strategic Communications Team of European Central Bank and cover a wide range of topics related to monetary policy and economic outlooks.

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

The Cacophony Index is calculated based on the classification results of the news articles. The index measures the level of discordance among the ECB council members by considering the proportion of hawkish, dovish, and neutral statements as well as their discordance with ECB public statements on monetary policy.

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
└─────ECB_Governors_Analysis (analysis notebooks)
│       └─ECB_Governor_Analysis.ipynb (EDA on the on the Governing Council dataset)
│       └─ECB_Interest_Rate_Data.ipynb (create a plot of ECB interest rates over the specified time period)
│       └─ECB_Members.ipynb (loads the ECB Governing Council members into a dataframe)
│       └─EDA_Dataset.ipynb (exploratory data analysis on the complete dataset)
└─────Models_Notebook (models notebooks)
│       └─bert_model.ipynb (bert model for classification)
│       └─dictionary_classification_model.ipynb (dictionary rule based model for classification)
└─────OpenAI_Classification (openai notebooks)
│       └─3000_OpenAI_API_Classification_Articles.ipynb (applies Chat GPT to 10% of articles)
│       └─ECB_Statement_Manual_Classification.ipynb (creates dataframe with the manual classification of ECB statements)
│       └─Manual_Classification_Scores.ipynb (statistics of outcome of the human labelling)
│       └─OpenAI_API_Classification_Articles.ipynb (select the best ChatGPT prompt)
│       └─Randomised_Articles_100.ipynb (randomly select 100 articles to test the best prompts)
│       └─Randomised_Articles_3000.ipynb (randomly select 3000 articles to test the best prompts)
└─────Prediction_Results
└─────Results_analysis (results analysis notebooks)
│       └─index.ipynb (contains the building of the cacophony index)
│       └─merging_for_index.ipynb (merges our dataset with articles in the dataset of the monetary policy statements)
│       └─roberta_model_application.ipynb (runs the fine tuned BertModel on the whole database)
└─────roberta_model (stores various outputs and artifacts of the model)
└─────Scraping (webscraping notebooks)
│       └─articles_scraping_translating.ipynb (scrapes and translates full articles from websites)
│       └─ECB_releases_scraping.ipynb (scrapes ECB statements on monetary policy)
```

## Results

The results of the model training and the calculated Cacophony Index are all documented in the presented paper. This includes:

- Model performance metrics
- Visualizations of the Cacophony Index over time

## Conclusion

This project demonstrates the use of natural language processing and machine learning techniques to analyze public statements and measure discordance within the ECB council. Tools like Chat-GPT4 proved to be among the most effective for this type of text analysis. A cacophony index was created to quantify discordance, with sentiment aggregated around the release dates of ECB monetary policy statements, providing valuable insights for economists and policymakers.

## Contact Information

Please raise issue on GitHub or contact either one of our members:
- Rui Maciel (rui.maciel@bse.eu)
- Edward Monbiot (edward.monbiot@bse.eu)
- Joaquin Ossa (joaquin.ossa@bse.eu)