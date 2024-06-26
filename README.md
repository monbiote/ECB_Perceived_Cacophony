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
- [Contributing](#contributing)
- [License](#license)

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

3. Run the data preprocessing and analyze the data script:
    ```bash
    python ECB_Governors_Analysis/preprocess_data.ipynb
    ```

4. Classify the articles
    ```bash
    python OpenAI_Classification/3000_OpenAI_API_Classification_Articles.ipynb
    ```

5. Train the model:
    ```bash
    python Models_Notebook/bert_model.ipynb
    ```

6. Calculate the Cacophony Index:
    ```bash
    python scripts/calculate_index.py
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