**Gender-Recognition-by-Voice**
Gender Recognition by Voice and Speech Analysis by Implementing Classification Algorithms in Python

**Objective**
To predict gender with corresponding voice and speech features.

**Dataset**
This database was created to identify a voice as male or female, based upon acoustic properties of the voice and speech. The dataset consists of 3,168 recorded voice samples, collected from male and female speakers. The voice samples are pre-processed by acoustic analysis in R using the seewave and tuneR packages, with an analyzed frequency range of 0hz-280hz (human vocal range).

The column label(Target Feature) is also present in the dataset which has two values **Male and female.**

This is the data that we have to predict for future samples.

The dataset is divided into two parts: **Train, and Test sets.**
**Train Set:**
The train set contains 2851 rows and 22 columns.
The last column label is the target variable.
**Test Set:**
The test set contains 317 rows and 21 columns.
The test set doesn’t contain the label column.
It needs to be predicted for the test set.

**Variable Description**
The following acoustic properties of each voice are measured and included within the CSV:

label(Target Variable): male or female
meanfreq: mean frequency (in kHz)
sd: standard deviation of frequency
median: median frequency (in kHz)
Q25: first quantile (in kHz)
Q75: third quantile (in kHz)
IQR: interquantile range (in kHz)
skew: skewness (see note in specprop description)
kurt: kurtosis (see note in specprop description)
sp.ent: spectral entropy
sfm: spectral flatness
mode: mode frequency
centroid: frequency centroid (see specprop)
peakf: peak frequency (frequency with highest energy)
meanfun: average of fundamental frequency measured across the acoustic signal
minfun: minimum fundamental frequency measured across the acoustic signal
maxfun: maximum fundamental frequency measured across the acoustic signal
meandom: average of dominant frequency measured across the acoustic signal
mindom: minimum of dominant frequency measured across the acoustic signal
maxdom: maximum of dominant frequency measured across the acoustic signal
dfrange: range of dominant frequency measured across the acoustic signal
modindx: modulation index. Calculated as the accumulated absolute difference between adjacent measurements of fundamental frequencies divided by the frequency range

I have performed Logistic Regression, Decision Tree, and Random Forest ML Algorithm. 
Since the Dataset has a high number of Features I have performed Principal Component Analysis for better accuracy.

**Results**
**Logistic Regression** :-

Accuracy on training set: 0.9728
Accuracy on test set: 0.9807

**Decision Tree**
Accuracy on training set: 1.00
Accuracy on test set: 0.9789

**Random Forest**
Accuracy on training set: 1.00
Accuracy on test set: 0.9894

**Random Forest with PCA**
Accuracy on training set: 1.00
Accuracy on test set: 0.9929

