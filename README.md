# Ethereum-Fraud-Detection

Detecting Fraudulent Blockchain Accounts on Ethereum with Supervised Machine Learning

---

## Introduction

> Since 2021, more than 46,000 people lost over $1 billion to cryptocurrency scams, nearly 60 times more compared to 2018.1 The Federal Trade Commission (FTC) found that the top cryptocurrencies used to pay scammers were Bitcoin (70%), Tether (10%) and Ethereum (9%).1 Especially, with the most recent incident with FTX, a crypto exchange which misused more than $1 billion of client’s funds, it becomes ever more important to stay vigilant when navigating through the cryptocurrency world.2 To enforce deterrence against fraudulent scams, we used supervised machine learning techniques such as Logistic Regression, Naive Bayes, SVM, XGboost, LightGBM, MLP, Tabnet and Stacking to detect and predict fraudulent Ethereum accounts. This would add business value by enhancing fraudulent account detection features on crypto exchanges and crypto wallets, enabling people to navigate confidently through the cryptocurrency world and safeguard their personal assets. We set an objective to achieve more than 90% F1 score for machine learning models in predicting fraudulent accounts on the Ethereum blockchain.

---

## Data

There are 2 data sources : `Kaggle` and `Etherscan`

### `Kaggle`

> The Kaggle dataset is downloaded from https://www.kaggle.com/datasets/vagifa/ethereum-frauddetection-dataset and can be found in `./Data/address_data_k.csv`

### `Etherscan`

> Data are mined from etherscan from https://etherscan.io/accounts/label/phish-hack (Currently data has been taken off Etherscan, but we have saved our data) and can be found in `./Data/address_data_e.csv`

### `Combined`

> Data from Kaggle and Etherscan are combined and can be found in `./Data/address_data_combined.csv`

### Data Description

> We started with a Kaggle dataset of 9841 observations. Each observation is a unique Ethereum account, with each variable being an aggregate statistic over all transactions performed by that unique account, such as total Ether value received or average time between transactions. The data also distinguishes between account-to-account transactions and account-to-smart contract transactions. However, the dataset was highly imbalanced, with only 2179 out of 9841 (22.14%) being marked as fraud. To address the imbalance, we leveraged an API provided by Etherscan, a “Block Explorer and Analytics Platform for Ethereum”. This allowed us to retrieve transactions made by any given account address on the Ethereum blockchain. As a result, the number of fraudulent accounts in our dataset climbed to 4339 observations, making the combined dataset less imbalanced (45.97% fraud).

---

## Machine Learning Models

### Random Foest

`./Models/Random Forest Model.ipynb`

### Logistic Regression

`/Models/LightGBM Model.ipynb`

### Naive Bayes

`/Models/Naive Bayes Model.ipynb`

### Support Vector Machine (SVM)

`/Models/Support Vector Machine Model.ipynb`

### Multi-Layer Perceptron (MLP)

`/Models/Multi-Layer Perceptron Model.ipynb`

### eXtreme Gradient Boosting (XGBoost)

`/Models/XGBoost Model.ipynb`

### TabNet

`/Models/TabNet Model.ipynb`

### LightGBM

`/Models/LightGBM Model.ipynb`

### Stacked Ensemble Model

`/Models/Final Stacking Model.ipynb`
