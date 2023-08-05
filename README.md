# Deep-Learning-Anomaly-Detection
Using an Autoencoder for Anomaly Detection

## Introduction 
Anomaly detection is a technique that uses AI to identify abnormal behavior as compared to an established pattern. A common way to implement this is to train a neural network to learn some characteristic about a dataset of only normal examples,
and to detect abnormal data when that characteristic differs from normality.

## Goal
Train a reconstruction autoencoder to perform anomaly detection and localization. Implement different metrics for anomaly detection
and localization

## Project Outline

* Train an autoencoder on one class (the normal class) of a simple dataset like CIFAR-10.
* Figure out how to use this autoencoder to detect when a test image is either (1) normal (from the training set class) or (2) anomalous
(from some other class). Implement metrics of (1) area under the RO curve (image level AUC) and (2) maximum possible accuracy.
Repeat the previous steps but for the more realistic, commonly used industrial anomaly detection benchmark of MVTec-AD (see
here https://paperswithcode.com/sota/anomaly-detection-on-mvtec-ad). Can you train a model to work for this more challenging
dataset?
* Figure out how to use your model to localize/segment anomalies in known anomalous images. Measure this by using your model to
predict MVTec-AD’s provided anomaly segmentation masks for it’s anomalous datapoints (again, while only training your network on
non-anomalous data!).
* Test anomaly localization by implementing different metrics for it, and compare and contrast their utility:
  1. Pixel AUC
  2. Pixel average precision
  3. Best possible Dice score (I.e, over all possible thresholds)
  4. best possible IoU
  5. best possible PRO (see https://arxiv.org/abs/2106.08265)
