# Cryptographic Fingerprint Template Protection Using Phase-Keyed Biometric Transformation
# Manuscript ID: IEEE LAT AM T Submission ID: Paper ID: 9724


Authors:
• Archana Pallakonda
• R Padmavathy

# Included Scripts
This repository contains all scripts required to reproduce the simulation and numerical results presented in the article.
| Source code | Figure/Table | description |
| --- | --- |
| FVC200220024-classification.ipynb| Figs. Accuracy, Loss, EER are the resultant plots |Interactive python notebook having python code developed for the Classification Task |

| FVC-Verification.ipynb | Figs. ROC, DET are the resultant plots| Interactive python notebook having python code developed for the Verification Task |

| genuine and imposter.ipynb | Figs. Genuine and Imposter Score distribution, FRR/FAR, ROC are the resultant plots| Interactive python notebook having python code developed for Calculating Genuine and Imposter Scores |

| hill climbing attack.ipynb | Figs. ROC,Scorce Oracle, Binary Oracle are the resultant plots | Interactive python notebook having python code developed for the Hill climbing ttack testing  |


# Requirements:
• Python / Jupyter notebook
• gitbash terminal
# Installation Prerequisites:

Ensure that you have the following installed:
Python 3.x

Jupyter Notebook

TensorFlow 2.x

Keras

NumPy

Matplotlib

Scikit-learn

You can install the required packages via pip:

pip install tensorflow numpy matplotlib scikit-learn

Running the Code

Clone this repository to your local machine.

Navigate to the directory containing the Jupyter notebooks.

Open the desired notebook (e.g.,Fingerprint-Template-security.ipynb).

Execute the notebook cells to run the model training and evaluation.

# The following work flow 

# Description of proposed work
The proposed methodology, Phase-Keyed Biometric Transformation (PKBT), is a novel fingerprint template protection technique that enhances biometric security. It integrates a Hilbert transform-based phase encoding method to embed a secret phase key into extracted fingerprint features. This transformation ensures non-invertibility by altering the phase of the biometric features while preserving their magnitude, which maintains their distinctiveness for recognition.The PKBT technique introduces a secret key modulation that prevents unauthorized reconstruction of the original fingerprint data. Additionally, the framework supports revocability and unlinkability.

# Dataset

The datasets used in the experiments are publicly available and can be accessed via the following link:

FVC2002,FVC2004:http://bias.csr.unibo.it/fvc2002/databases.asp

FVC2002 DB1 Optical Sensor 
FVC2002 DB2 Optical Sensor 
FVC2002 DB3 Capacitive Sensor 
FVC2002 DB4 SFinGe v2.51 
FVC2004 DB1 Optical Sensor 
FVC2004 DB2 Optical Sensor 
FVC2004 DB3 Thermal sensor 
FVC2004 DB4 SFinGe v3.0 

# Feature Extraction Using MobileNet:

A lightweight deep learning model, MobileNet, is used for extracting biometric features from fingerprint images. These features are then used for transformation and classification. The extracted features represent critical fingerprint patterns like ridges and minutiae.

# Hilbert Transform for Analytic Feature Space:

The Hilbert transform is applied to the extracted fingerprint features to generate an analytic feature space. This transform creates a complex representation of the original features by separating magnitude and phase components.

# Phase Modulation with a Secret Key:

The phase component of the analytic features is modulated using a secret phase key. This key-dependent modulation ensures that the transformation is non-invertible, making it computationally infeasible to recover the original fingerprint features without the key.The transformed features are reconstructed by combining the original magnitude with the modulated phase. The final transformed feature, a real-valued vector, incorporates both the original biometric information (via magnitude) and enhanced security (via phase modulation).

# Classification and Verification
Task:1- A Dense Neural Network classifier is employed to classify both original and transformed features. The network consists of multiple fully connected layers with batch normalization, dropout, and L2 regularization to prevent overfitting and improve classification accuracy.Mahalanobis Distance for verification purpose

Task:2- Verification using Mahalobis Distance for Real and Query fingerprint

# HillClimbing Attack testing
*Score-Oracle :  It provides a continuous similarity score (higher values indicate a closer match) between the target feature and a generated feature during an attack. The goal is to find a synthetic feature that is as similar as possible to the original target template.
*Binary-Oracle : It gives a binary decision — match or no-match — based on whether the generated feature is accepted as matching the target feature.

# Results

The results of the experiments are documented in the respective notebooks. They include performance metrics such as accuracy, ROC, EER. 

