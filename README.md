# neural-network-challenge-1


## Overview
This project aims to predict the likelihood of successful loan repayment using a deep learning neural network. The dataset includes various features related to student loans, such as payment history, degree scores, GPA rankings, and more. The model classifies students into two categories based on their credit ranking, indicating whether they are likely to repay their loans successfully.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Data Description](#data-description)
- [Model Architecture](#model-architecture)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Future Work](#future-work)


## Installation
To run this project, you need to have the following libraries installed:
- `pandas`
- `tensorflow`
- `scikit-learn`
- `numpy`


## Usage

    Download the student-loans.csv dataset.
    Update the file path in the script to point to the location of the dataset.
    Run the Python script to train the neural network model and evaluate its performance.
## Data Description

    The dataset consists of the following columns:

    payment_history: The payment history of the loan.
    location_parameter: Geographical data related to the borrower.
    stem_degree_score: Score related to STEM degree attainment.
    gpa_ranking: The GPA ranking of the student.
    alumni_success: Measure of alumni success.
    study_major_code: Code representing the student's major.
    time_to_completion: Time taken to complete the degree.
    finance_workshop_score: Score from financial workshops attended.
    cohort_ranking: Ranking within the cohort.
    total_loan_score: Overall score for loans taken.
    financial_aid_score: Score based on financial aid received.
    credit_ranking: Target variable indicating repayment success (1: Successful, 0: Not Successful).

## Model Architecture

    The model is a deep neural network with the following architecture:

    Input layer with features derived from the dataset.
    Two hidden layers with ReLU activation functions.
    Output layer with a single neuron using the sigmoid activation function to output probabilities for binary classification.

Model Summary

    Model: "sequential"
    _________________________________________________________________
    Layer (type)                Output Shape              Param #
    =================================================================
    dense (Dense)               (None, 10)                120
    dense_1 (Dense)             (None, 5)                 55
    dense_2 (Dense)             (None, 1)                 6
    =================================================================
    Total params: 181
    Trainable params: 181
    Non-trainable params: 0
    _________________________________________________________________


## Evaluation Metrics

    The model's performance was evaluated using:

    Loss: Binary Crossentropy
    Accuracy: Overall accuracy of predictions on the test dataset

## Results

    The model achieved the following metrics on the test data:

    Loss: 0.5266
    Accuracy: 0.7594

    A classification report is generated to show precision, recall, and F1-score for each class.


## Future Work:

    Experimenting with different neural network architectures.
    Fine-tuning hyperparameters to enhance model performance.
    Incorporating more features or external data sources for better predictions.
