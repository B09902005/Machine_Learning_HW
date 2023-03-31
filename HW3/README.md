# Unsupervised Learning - Image Clustering

## Description

This code is about image clustering. Given 9000 RGB pictures (32\*32\*3), we have to divide them into two parts: scenery photos and others.

All the pictures are unlabelled, so we don't know the ground truth. What we have to do is to do unsupervised learning and then cluster the pictures into two groups.

**PCA** (or TSNE or other dimension reduction methods) can make the performance better because it can prevent from being affected by redundant information.

To do clustering, I used **K-means clustering**.

## Files

* **trainX.npy.zip** : The .zip file of the training dataset
* **visualization_X.npy.zip** : Also the .zip file of the training dataset
* **hw3.ipynb** : The code I train, test, and evaluate
* **predict.csv** : my prediction to the training data
* **report.pdf** : My report        

## Usage

Run **hw3.ipynb** on Google Colab. It will automatically download the training dataset **trainX.npy.zip** and **visualization_X.npy.zip** and then unzip them into **trainX.npy** and **visualization_X.npy**. After training, **model.pth** will be generated. This way, we can predict whether the pictures are scene images and record them in **predict.csv**.

## Performance

The accuracy is 0.79044, which is ranked 28-th among 69 students.
