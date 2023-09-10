# Gender Recognition by Voice
![Gender](https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/Images/image%201.png)

Voice-Based Gender User Tracking for Telecom Company XYZ is an innovative solution designed to automate the process of tracking and categorizing the gender of Telecom Company XYZ based on their voice samples. As the user count continues to grow, manually categorizing users has become a tedious and time-consuming task. To streamline this process, we've developed a machine learning model that leverages 
### Random Forest with Principal Component Analysis (PCA) achieved the highest accuracy in gender recognition.

## Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Installing & Importing Libraries](#installing--importing-libraries)
- [Data Acquisition & Description](#data-acquisition--description)
- [Data Pre-Processing](#data-pre-processing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Preparation](#data-preparation)
- [Model Development & Evaluation](#model-development--evaluation)
- [Acknowledgments](#acknowledgments)
- [Contact Information](#contact-information)

## Introduction
- Company XYZ is a leading telecom company with 5 million users.
- They want to keep track of the number of male and female users, but as the user count increases, the task becomes more tedious.
- They want to automate the process of keeping track of male and female users using their voice.
- Their research and development teams are trying to understand the acoustic properties of the voice and speech so that they can use it to enhance the customer experience in their new product.


## Problem Statement


### Current Challenges:

- The current process is a manual classification of gender using their voice.
- This is very tedious and time-consuming as it needs to be repeated every time a new customer joins.
- We will try to automate the process of predicting the male or female voice using acoustic properties of the voice or speech rather than doing this manual work.

### Project Deliverables

- Deliverable: Gender prediction using voice.
- Machine Learning Task: Classification
- Target Variable: label

## Installing & Importing Libraries

We have used several libraries in our project, including:

- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- pydotplus

## Data Acquisition & Description

### Dataset Details

The dataset is divided into two parts: Train and Test sets.

**Train Set:**

- The train dataset contains 2851 rows and 22 columns.
- The last column `label` is the target variable.
- The training dataset can be downloaded from [here](https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/DataSets/voice_train.csv).

**Test Set:**

- The test dataset contains 317 rows and 21 columns.
- The test set doesn’t contain the `label` column.
- It needs to be predicted for the test set.
- The test dataset can be downloaded from [here](https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/DataSets/voice_test.csv).

### Dataset Feature Description

The following acoustic properties of each voice are measured and included in the dataset:

| Column Name | Description                                          |
|-------------|------------------------------------------------------|
| Id          | Unique Id                                            |
| meanfreq    | Mean frequency (in kHz) for the voice sample        |
| sd          | Standard deviation of the frequency                 |
| median      | Median frequency (in kHz) for the voice sample      |
| Q25         | First quantile (in kHz)                             |
| Q75         | Third quantile (in kHz)                             |
| IQR         | Interquartile range (in kHz)                        |
| skew        | Skewness of the voice sample                        |
| kurt        | Kurtosis of the voice sample                        |
| sp.ent      | Spectral entropy                                    |
| sfm         | Spectral flatness of the voice sample               |
| mode        | Mode frequency                                      |
| centroid    | Frequency centroid                                  |
| peakf       | Peak frequency (the frequency with the highest energy) |
| meanfun     | Average of fundamental frequency measured across the acoustic signal |
| minfun      | Minimum fundamental frequency measured across the acoustic signal |
| maxfun      | Maximum fundamental frequency measured across the acoustic signal |
| meandom     | Average of dominant frequency measured across the acoustic signal |
| mindom      | Minimum of dominant frequency measured across the acoustic signal |
| maxdom      | Maximum of dominant frequency measured across the acoustic signal |
| dfrange     | Range of dominant frequency measured across the acoustic signal |
| modindx     | Modulation index. Calculated as the accumulated absolute difference between adjacent measurements of fundamental frequencies divided by the frequency range |
| label       | The label for the voice sample (male or female)     |

## Data Pre-Processing

- We don't have any Null values in our Dataset.
- The average mean frequency for both males and females is 0.18 with a standard deviation of 0.02.
- The minimum mean frequency is 0.039363, and the maximum is 0.251124.
- The `skew` column looks highly skewed with a minimum skewness of 0.14 and a maximum of 34.
- The `kurt` column also looks highly skewed with a mean of 35, median of 8.25, and a maximum of 1309.61.
- `maxdom` and `dfrange` are also highly skewed. We will explore their distributions in the EDA section.

## Exploratory Data Analysis

- `skew` and `kurt` are highly correlated, with a correlation coefficient of 0.98 (almost 1).
- `meanfreq` and `median` are positively correlated.
- `meanfreq` is also highly correlated with feature `Q25`.
- `Q25` and `IQR` are highly negatively correlated.
- `Q25` and `sd` are highly negatively correlated.

![Distribution of Target Feature](https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/Images/Distribution%20of%20Target%20feature.png)

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/Images/kurt.png" alt="Image 1" width="400" height="250" style="margin-right: 20px;">
  <img src="https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/Images/meanfreq.png" alt="Image 2" width="400" height="250">
</div>

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/Images/sd.png" alt="Image 1" width="400" height="250" style="margin-right: 20px;">
  <img src="https://github.com/AnmolArora15/Gender-Recognition-by-Voice/blob/main/Images/skew.png" alt="Image 2" width="400" height="250">
</div>

## Data Preparation

We have used **StandardScaler** to scale our data to bring all the features to the same scale.

## Model Development & Evaluation

We have deployed the following models:

| Model Name             | Train Acc. | Test Acc. |
| ---------------------- | ---------- | --------- |
| Logistic Regression    | 0.972      | 0.980     |
| Decision Tree          | 1.0        | 0.977     |
| Random Forest          | 1.0        | 0.984     |
| Random Forest with PCA | 1.0        | 0.992     |

## Acknowledgments
Special thanks to @Accredian for helping me in the Code.

### Contact Information 
**Open for questions and suggestions.**
- You can contact me on Email - anmol.1591@outlook.com
- LinkedIn - www.linkedin.com/in/anmol-arora-71371318
## Thank You
