# Bayesian-Classifier-and-Gaussian-Mixture-Model-for-Pattern-Recognition
This project involves the implementation of **Bayesian Classifiers** and **Gaussian Mixture Models (GMM)** for statistical pattern recognition.

**1. Problem Statement :**
This project involves the implementation of **Bayesian Classifiers** and **Gaussian Mixture Models** (GMM) for statistical pattern recognition. The primary objective is to classify datasets with varying degrees of **linearity and nonlinearity**, using different covariance assumptions. The datasets are provided with predefined class labels, and the task is to apply probabilistic models for classification and image segmentation.

**The assignment consists of:**\
  **Classification Task:** Bayesian classification using Gaussian Mixture Models (GMM) for various datasets.\
  **Image Segmentation Task:** Clustering-based segmentation using **K-means** and **Modified K-means**.\
This project must be implemented from scratch in Python or MATLAB without using existing libraries for GMM, Bayesian classifiers, multivariate Gaussian distributions, likelihood calculations, or K-means clustering.

**2. Datasets :** 
The following datasets are provided for experimentation:\
  **Dataset 1: Nonlinearly Separable Classes**\
      • **A 2D dataset with 2 or 3 classes that are not linearly separable.**\
      • **Each class is represented by a set of points.**\
      • **Data must be divided into 70% training and 30% test set**.\

  **Dataset 2: Real-World Data**\
    (a) **Vowel Data: A 2D dataset representing vowel speech data** (formant frequencies F1 & F2).\
    (b) **Scene Image Dataset:** A 3-class dataset consisting of natural images.\
    (c) **Cervical Cytology Dataset:** Images of cervical cells used for medical image classification.\
  For Dataset 1 and Dataset 2(a), **70% of data is used for training and 30% for testing.**\
  For Dataset 2(b) and Dataset 2(c), **predefined training and test splits are provided.**

**3. Image Segmentation using Clustering**\
For **cervical cell image segmentatio**n, clustering is used to segment different regions of the images:\
•  **K-means Clustering**\
•  Clusters local feature vectors extracted from cell images.\
•  Uses **Euclidean distance** as a similarity measure.\
•  Modified K-means (**Mahalanobis Distance**)\
•  Uses **Mahalanobis distance** instead of Euclidean distance for better cluster separation.\
•  Accounts for variance and covariance of the features.\
Both clustering methods are initialized with the same initial centers.

**4. Feature Extraction :**\ 
Feature extraction techniques vary based on dataset type.\
**4.1 Feature Extraction for Scene Image Dataset** (Dataset 2b)\
Two types of feature vectors are extracted:
• **Color Histogram Feature Extraction** (24-Dimensional Vector)\
• Image is divided into 32×32 non-overlapping patches.\
• An **8-bin histogram** is computed for each color channel (Red, Green, Blue).\
• The final **24-dimensional feature vector** is obtained by concatenating histograms from the three color channels.\
• Each image is represented as a set of 24D feature vectors.\
• **Bag-of-Visual-Words (BoVW)** Representation (32-Dimensional Vector)\

• K-means clustering is applied to all **24D color histogram** feature vectors across training images.\
• Clusters are grouped into 32 visual words.\
• Each image is represented as a **32-dimensional histogram** showing how many local features belong to each cluster.\
• The final feature vector is normalized.\

**4.2 Feature Extraction for Cervical Cytology Dataset (Dataset 2c)**
• **7×7 overlapping patches** are extracted from cell images.
• **Mean and standard deviation** of pixel intensities are computed for each patch.
• Each patch is represented as a **2D feature vector**.
• The entire image is stored as a **set of 2D feature vectors**.
