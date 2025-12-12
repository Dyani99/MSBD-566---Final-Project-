# MSBD-566---Final-Project-
Predicting Autism Spectrum Disorder Using PCA + Neural Network
Project Overview

This project applies Principal Component Analysis (PCA) and a Neural Network classifier to predict Autism Spectrum Disorder (ASD) using behavioral, demographic, and clinical screening data. The goal is to build an efficient, accurate machine learning pipeline that supports early ASD risk identification.

This project was developed for MSBD566 – Predictive Modeling and Analysis.
Dataset Description

Dataset Name: Autistic Spectrum Disorder Screening Data for Adults

Records: 704

Features: 21 (behavioral AQ-10 items, demographic variables, clinical indicators)

Target variable: ASD_Class (1 = ASD, 0 = Non-ASD)

Source: Fadi Fayez Thabtah, Manukau Institute of Technology

Data type: Categorical, binary, and numerical

The dataset captures screening responses from adults who completed the AQ-10 questionnaire, along with demographic and clinical attributes.

Full description provided in dataset documentation.
Data Preprocessing

The raw dataset contained byte-encoded values (e.g., b'YES', b'1'), which were converted to strings and mapped to appropriate numeric/categorical formats.

Preprocessing steps:

Decode byte strings

Convert binary values to 0/1

One-hot encode categorical features

Standardize numerical features
Methods Used
1. Principal Component Analysis (PCA)

Reduced the dimensionality of the dataset while retaining 95% of total variance

Removed multicollinearity

Generated ~12–16 orthogonal PCA components

Enabled faster and more stable model training

2. Neural Network (MLPClassifier)

Two hidden layers: (32 → 16 neurons)

Activation: ReLU

Optimizer: Adam

Max iterations: 400

Input: PCA-transformed components

Output: ASD vs. Non-ASD classification

Prepare all features for PCA
