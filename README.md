# Lead Conversion Prediction for X Education

This project aims to develop a **lead conversion prediction model** for **X Education**, an online education company, using **Logistic Regression**. The goal is to identify "Hot Leads" – those most likely to convert into paying customers – to optimize the sales team’s efforts and improve the company's conversion rate.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Approach](#approach)
- [Model](#model)
- [Evaluation](#evaluation)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview
X Education experiences a low conversion rate (typically around 30%) for leads generated through various marketing channels. The company wants to improve this conversion rate by targeting the most promising leads, known as **Hot Leads**. This project uses a **Logistic Regression model** to predict the likelihood of leads converting into customers based on various attributes such as lead source, time spent on the website, and past activity.

## Data Description
The dataset provided by X Education contains **9000+ records** of past leads, with various features such as:
- **Lead Source**
- **Total Time Spent on Website**
- **Total Visits**
- **Last Activity**
- **Converted** (Target variable: 1 if converted, 0 if not)

Additionally, some categorical variables contain a level called ‘Select,’ which acts as a placeholder for missing data. These need to be handled appropriately before model training.

## Approach
1. **Data Preprocessing**:
   - Handle missing values (especially the 'Select' level in categorical variables).
   - Convert categorical variables into numerical format using **One-Hot Encoding**.
   - Feature scaling for continuous variables.
   
2. **Model Building**:
   - Train a **Logistic Regression** model using the processed data.
   - Evaluate model performance using metrics like **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **AUC-ROC**.

3. **Lead Scoring**:
   - Assign a lead score between 0 and 100 based on the model’s predicted probabilities.
   - Identify the top leads (those with the highest scores) to optimize the sales funnel.

## Model
- The **Logistic Regression** model is built to predict whether a lead will be converted based on the available features.
- The model is evaluated using:
   - **Confusion Matrix**
   - **Precision, Recall, F1-Score**
   - **ROC-AUC Curve**
   
- The **lead scores** are calculated as probabilities that the model assigns to each lead being converted.

## Evaluation
- The model’s performance is assessed based on how well it predicts conversion probabilities and differentiates between leads that are likely to convert and those that are not.
- The company’s target lead conversion rate is approximately 80%. The model will be evaluated to ensure that it aligns with this target conversion rate while minimizing false positives (wasting resources on cold leads).

## Installation
To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Debyvypth1862/Logistic-Regression-Lead-Conversion-Project.git
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure you have the necessary data files (provided in the zip folder) and place them in the appropriate directories.

## Usage
1. Run the `Leading Score Case Study Group.ipynb` Jupyter notebook.
2. The notebook contains detailed steps for:
   - Data loading
   - Preprocessing and cleaning
   - Model training and evaluation
   - Generating predictions and lead scores
3. The model’s performance can be visualized, and the leads with the highest probability of conversion will be identified for further action by the sales team.
