# Bioinformatics Project - Computational Drug Discovery
This repository contains the complete workflow for a bioinformatics project focused on computational drug discovery. The project involves data preprocessing, exploratory data analysis, descriptor calculation, and machine learning model building to predict bioactivity. The steps are divided into three main parts, detailed below.

# Table of Contents
Part 1: Data Preprocessing and Exploratory Data Analysis
Part 2: Descriptor Calculation and Dataset Preparation
Part 3: Building and Evaluating Machine Learning Models
# Requirements
Usage
Acknowledgements
## Part 1: Data Preprocessing and Exploratory Data Analysis
Steps
Loading Bioactivity Data

Load the bioactivity data from a CSV file.
Calculating Lipinski Descriptors

Calculate Lipinski descriptors: Molecular weight (MW), Octanol-water partition coefficient (LogP), Number of hydrogen bond donors (NumHDonors), and Number of hydrogen bond acceptors (NumHAcceptors).
Converting IC50 to pIC50

Normalize IC50 values and convert them to pIC50.
Removing Intermediate Bioactivity Class

Remove compounds labeled as 'intermediate'.
Combining DataFrames

Combine the original data with Lipinski descriptors and pIC50 values.
Exploratory Data Analysis

Generate frequency plots and scatter plots.
Perform Mann-Whitney U Test to identify significant differences.
Saving the Processed Data

Save the processed dataset to a CSV file.
## Part 2: Descriptor Calculation and Dataset Preparation
Steps
Downloading and Setting Up PaDEL-Descriptor

Download and unzip PaDEL-Descriptor.
Preparing Input Data for PaDEL-Descriptor

Select relevant columns and save the data in SMILES format.
Calculating Fingerprint Descriptors

Use PaDEL-Descriptor to calculate fingerprint descriptors.
Preparing X and Y Data Matrices

Load descriptors output and split the data into input (X) and output (Y) matrices.
Combining X and Y Data

Combine input features (X) with the output variable (pIC50) and save the dataset.
## Part 3: Building and Evaluating Machine Learning Models
Steps
Importing Libraries

Install and import necessary libraries.
Loading the Dataset

Load the combined dataset from a CSV file and split into X and Y.
Data Preprocessing

Remove low variance features.
Splitting the Data

Split data into training and testing sets using an 80/20 ratio.
Building a Regression Model

Build a Random Forest Regressor model and evaluate its performance.
Visualizing Model Performance

Generate scatter plots and use LazyPredict to compare multiple algorithms.
Visualize model performance with bar plots.
Requirements
Python 3.7
pandas
numpy
seaborn
matplotlib
rdkit
sklearn
LazyPredict
