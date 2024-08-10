In this I have used autoencoder for image compression using deep CNN(Convolutional Neural Network) model. 
Image compression is one the applications of autoencoder.
Autoencoder is one of the main concept that needs to be known for various use cases.An autoencoder is a type of unsupervised learning algorithm that aims to reconstruct its input data at the output layer, typically learns efficient data representations (encoding) by training the network to ignore signal “noise”. Autoencoders can be used for image denoising, image compression, data compression, anomaly detection, and feature extraction and, in some cases, even generation of image data.

Flow of Autoencoder

Input Image -> Encoder -> Compressed Representation -> Decoder -> Reconstruct Input Image

The autoencoder takes an input data sample, here we have considered an image, and feeds it into the encoder network
The encoder network consists of several layers, typically including convolutional layers, pooling layers, and fully connected layers. These layers progressively reduce the spatial dimensions and extract meaningful features from the input data
The final layer of the encoder network produces a compressed representation of the input data
The compressed representation from the encoding stage is passed into the decoder network
The decoder network is symmetrical to the encoder network, consisting of fully connected layers, upsampling layers, and sometimes transposed convolutional layers. It takes the compressed representation and gradually increases the spatial dimensions to reconstruct the original input data
The final layer of the decoder network generates the reconstructed output, which aims to closely resemble the original input data

**
Import Modules**

import numpy as np
import matplotlib.pyplot as plt
from keras import Sequential
from keras.layers import Dense, Conv2D, MaxPooling2D, UpSampling2D
from keras.datasets import mnist
numpy - used to perform a wide variety of mathematical operations on arrays
matplotlib - used for data visualization and graphical plotting
keras - used to provide a user-friendly and intuitive interface for designing, training, and evaluating deep learning models
keras.layers - provides a variety of pre-defined layers that can be used to construct neural network models
keras.datasets - provides pre-loaded datasets that can be used for training, testing, and evaluating machine learning models
