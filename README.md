# Fingerprint-Template-security

The transformation is designed to balance security and usability in biometric systems. By preserving the inherent distinctiveness of each user’s biometric traits, it ensures accurate recognition and matching. At the same time, the transformation secures the template representations such that any attempt to reconstruct the original biometric data from the transformed templates becomes computationally infeasible. This dual property guarantees that the system remains robust against attacks aimed at stealing or reverse-engineering sensitive biometric information, while maintaining reliable authentication performance.

# The following work flow 

# classifying and Verifying Genuine and Imposter Samples:

After applying the Phase-Keyed Biometric Transformation (PKBT), the transformed biometric templates are used both for verification and classification. Verification involves comparing a query template with a stored template to confirm the claimed identity, while classification determines whether a sample belongs to a genuine user or an imposter. A fully connected Dense Neural Network is employed for this purpose, leveraging the discriminative features of the transformed templates to accurately classify inputs as genuine or imposter. This approach ensures robust authentication by simultaneously maintaining high verification accuracy and effective rejection of unauthorized access attempts.

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

# Methodology

The proposed method employs a Hilbert transform-based phase encoding to embed a secret phase key, ensuring non-invertibility, revocability, and unlinkability.
Experiments on FVC2002 and FVC2004 datasets confirm that PKBT maintains high recognition accuracy while securing templates.
Security and adversarial analyses further demonstrate PKBT’s robustness against biometric guessing and reconstruction attacks.

# Results

The results of the experiments are documented in the respective notebooks. They include performance metrics such as accuracy, ROC, EER. 

