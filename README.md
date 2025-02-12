# Kaggle-NLP_with_Disaster_Tweets


## Table of Contents
- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Dataset EDA](#dataset-eda)
- [Data Preprocessing](#data-preprocessing)
- [Pipeline](#pipeline)
- [Models Implemented](#models-implemented)
- [Evaluation](#evaluation)
- [Experimental Record](#experimental-record)
- [License](#license)
- [Contributors](#contributors)

## Introduction
The **Kaggle-NLP_with_Disaster_Tweets** project is aimed to build a machine learning model that predicts which Tweets are about real disasters and which one's aren't. 
Key characteristics of the dataset include:  
- id: a unique identifier for each tweet
- text: the text of the tweet
- location: the location the tweet was sent from (may be blank)
- keyword: a particular keyword from the tweet (may be blank)
- target: in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)

## Dataset Overview
### Files
- train.csv: the training set
- test.csv: the test set
- sample_submission.csv: a sample submission file in the correct format

## Dataset EDA
### Text Length and Word Count Analysis

#### Hisplot
<div align="center">
  <img src="https://github.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/blob/main/img/EDA_hisplot.png" alt="Hisplot"/>
</div>

#### Scatterplot
<div align="center">
  <img src="https://github.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/blob/main/img/EDA_scatterplot.png" alt="Scatterplot"/>
</div>

#### Boxplot and Violin Plot
<div align="center">
  <img src="https://github.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/blob/main/img/EDA_boxplot.png" alt="Boxplot"/>
</div>

### Text Conent Analysis

#### Word Cloud
<div align="center">
  <img src="https://github.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/blob/main/img/EDA_wordcloud.png" alt="Wordcloud"/>
</div>

## Data Preprocessing  
1. **Step 1: Text Cleaning** 
    - Removed all URLs, HTML, and acronyms.
    - Converted all text to lowercase.
    - Removed punctuation.

2. **Step 2: Handling Missing Values**
    - Applied `dropna` to ensure data completeness.
    
3. **Step 3: Text Vectorization**
    - Applied `CountVectorizer` or `TfidfVectorizer` to convert the cleaned text data into numerical representations suitable for machine learning models.

## Pipeline

```mermaid
flowchart TD
    A[Dataset] --> B[Handeling data]
    B --> C[Data Preprocessing Completed]
    C --> D[Deep Learning Models]
    C --> E[Machine Learning Models 1]
    C --> F[Machine Learning Models 2]

    D --> G{Validation Dataset}
    E --> G
    F --> G
    
    G --> H[Test Dataset]
    H --> I[Final Evaluation]
```
## Models Implemented  

### Machine Learning Models 1
- **Linear Models**:  
  - Ridge Classifier   
  - Logistic Regression  

- **Decision Trees and Ensemble Models**:  
  - Decision Tree  
  - Random Forest  
  - XGBoost  
  - Voting Classifier

### Machine Learning Models 2

- **Decision Trees and Ensemble Models**:  
  - XGBoost  
  - Random Forest  
  - LightBGM
  - Stacking Classifier  
  - Voting Classifier (soft, hard)

### Deep Learning Models
  - RNN

## Evaluation
We use F1 score as our performance metric.
<div align="center">
  <img src="https://raw.githubusercontent.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/refs/heads/main/img/f1score%20formula.avif" alt="Hisplot"/>
</div>

## Experimental Record
<div align="center">
  <img src="https://github.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/blob/main/img/ML1_evaluation.png" alt="Hisplot"/>
</div>

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributors

<div align="center">
  <a href="https://github.com/andrew76214/Kaggle-NLP_with_Disaster_Tweets/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=andrew76214/Kaggle-NLP_with_Disaster_Tweets" alt="Contributors"/>
  </a>
</div>
