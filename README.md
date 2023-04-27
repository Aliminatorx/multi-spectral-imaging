# Multi-Spectral-Imaging
Multispectral Imaging with CAVE Dataset: code and data for the project exploring multispectral imaging technology using the CAVE dataset. Includes implementations of spectral unmixing, NMF, and sparse representation algorithms. Use for research or applications at your own risk.

## CAVE DATA SET LINK: 
https://www.cs.columbia.edu/CAVE/databases/multispectral/

# Super Resolution using the CAVE Dataset

## Introduction
This repository contains code for a machine learning approach to super resolution using the CAVE dataset from Columbia University. Our approach takes as input a low resolution hyperspectral image and a high resolution RGB image and produces as output an image with both high spatial and high spectral resolution. We evaluate the performance of the model using various metrics and discuss the results.

## Implementation
We begin by importing libraries and accessing the data from the CAVE dataset. The data is preprocessed by stacking the hyperspectral images, extracting patches and labeling data. High resolution images and low resolution images are extracted from the stacked data using AveragePooling2D layer and mean of specific bands, respectively. The data is reshaped, normalized and equalized before being split into training and testing sets. Two sequential models are implemented using Convolutional Layers, Dense Layers, and Activation Functions, with varying learning rates. We compile and evaluate the models using loss and val_loss metrics.

## Dataset
The 32 scenes in the database are split up into 5 sections. Every scene has a corresponding zip file. These zip files contain reflectance data in full spectral resolution in steps of 10 nm from 400 to 700 nm (31 bands total). A PNG image in 16-bit grayscale is used to store each band. Additionally, each scene includes a single typical colour image that is produced using sRGB values and displayed under a daylight illumination (D65).
https://www.cs.columbia.edu/CAVE/databases/multispectral/

## Requirements
Python 3.6+
TensorFlow 2.4+
OpenCV 4.0+
Usage
To run the code, download the dataset from the provided link and update the path in the code to the dataset directory. Then, simply run the Python file to train and test the model.

## Results
Our approach achieved promising results, with the second model producing a lower loss and val_loss compared to the first model. Further improvements can be made by fine-tuning the hyperparameters and exploring different architectures.

## Acknowledgements
We would like to thank Columbia University for providing the CAVE dataset and the contributors of TensorFlow and OpenCV libraries for their invaluable contributions to the field of machine learning and computer vision.
