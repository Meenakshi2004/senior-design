# EEG Biomarkers for Alzheimer’s Disease

## Project Overview

This project explores whether EEG frequency-band features can be used to distinguish Alzheimer’s Disease (AD) subjects from Healthy Control (HC) subjects using machine learning models and statistical analysis.

The project focuses on EEG slowing, a neurological phenomenon associated with Alzheimer’s disease in which low-frequency activity (delta and theta) increases while higher-frequency activity (alpha and beta) decreases.

Our goal was to determine whether these EEG frequency patterns could serve as useful biomarkers for distinguishing AD and HC subjects.


## Dataset

This project uses the <a href= "https://openneuro.org/datasets/ds004504/versions/1.0.7/metadata"> “A dataset of EEG recordings from: Alzheimer’s disease, Frontotemporal dementia and Healthy subjects” </a> dataset from Kaggle/OpenNeuro. The dataset contains resting-state EEG recordings collected under eyes-closed conditions from subjects diagnosed with Alzheimer’s Disease (AD), Frontotemporal Dementia (FTD), and Healthy Controls (HC).

For this project, we specifically focused on distinguishing:

* Alzheimer’s Disease (AD) subjects
* Healthy Control (HC) subjects

The EEG signals were processed to extract relative bandpower features from four primary EEG frequency bands:

* Delta (1–4 Hz)
* Theta (4–8 Hz)
* Alpha (8–13 Hz)
* Beta (13–30 Hz)

These extracted frequency-band features were then used for statistical analysis and machine learning classification.


## Methodology

### Feature Extraction

* Preprocessed EEG data in Google Colab
* Computed Power Spectral Density (PSD) using Welch’s Method
* Extracted relative EEG bandpower features

### Statistical Analysis

* Compared EEG bandpower differences between AD and HC groups
* Conducted two-sample t-tests to evaluate statistical significance

### Machine Learning Models

The following classification models were evaluated:

* K-Nearest Neighbors (KNN)
* Logistic Regression
* Support Vector Machine (SVM)
* Random Forest
* Gradient Boosting

Validation was performed using Leave-One-Out Cross Validation (LOOCV) due to the small dataset size.


## Key Findings

* AD subjects showed increased delta and theta activity and reduced alpha and beta activity.
* Theta-band activity emerged as one of the strongest distinguishing features between AD and HC groups.
* Theta power produced a statistically significant difference:

  * p = 0.0066
* KNN achieved the highest classification accuracy:

  * 94.4% accuracy
  * 17/18 subjects correctly classified


## Visualizations

### EEG Bandpower Comparison

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/38dbdc7e-102d-41b5-acb6-11f5cdc8ff13" />

### Theta Band Boxplot

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/af326fbf-ea32-414c-bd21-60d06dd0aeaa" />

### Model Accuracy Comparison

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/9957cf86-9459-41ea-b3ed-8d15ef8867eb" />

### KNN Confusion Matrix

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/6716d20f-58e6-4db3-9381-ab4d929318c1" />

## Limitations

* Small dataset size (18 subjects)
* Results may not generalize to larger populations
* More complex models may require substantially more EEG data


## Future Work

* Evaluate larger EEG datasets
* Explore deep learning approaches
* Investigate additional EEG biomarkers
* Test model generalizability across more diverse subjects

