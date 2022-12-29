# Autoencoders
Reconstructing image after encoding and decoding to denoise the image
An autoencoder is a type of neural network that is used to learn a compressed representation of an input data. It consists of two parts: an encoder and a decoder. The encoder maps the input data to a lower-dimensional representation, or latent space, and the decoder maps this latent representation back to the original data space.

The goal of training an autoencoder is to learn a function that can reconstruct the input data as accurately as possible, given the reduced dimensionality of the latent space. This can be useful for dimensionality reduction, denoising, or feature extraction.

Here is a brief overview of how an autoencoder works:

The input data is passed through the encoder network, which consists of a series of layers with decreasing dimensions.
The encoder produces a latent representation of the input data in the lower-dimensional space.
The latent representation is then passed through the decoder network, which consists of a series of layers with increasing dimensions.
The decoder produces a reconstruction of the input data.
The reconstruction is compared to the original input data, and the difference between the two is used to compute a loss value.
The model is trained to minimize this loss value by adjusting the weights of the encoder and decoder networks.

This code defines a custom model class called Autoencoder that represents an autoencoder. The Autoencoder class has a constructor that takes a single argument, latent_dim, which is the size of the latent space.

The Autoencoder class has two sub-models: an encoder and a decoder. The encoder is a sequential model consisting of a Flatten layer and a Dense layer with latent_dim units and a ReLU activation function. The decoder is also a sequential model consisting of a Dense layer with 784 units and a sigmoid activation function, followed by a Reshape layer that reshapes the output to the original image shape (28x28).

The call method of the Autoencoder class takes an input tensor x and passes it through the encoder and decoder to produce a reconstruction of the input.

Finally, an instance of the Autoencoder class is created with the specified latent_dim and stored in the autoencoder variable. This instance can then be used to fit the autoencoder to the training data and make predictions on new data.
