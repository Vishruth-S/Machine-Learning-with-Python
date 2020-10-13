# ***Convolutional Neural Networks***
*Convolutional Neural Networks* (**CNNs**) are a class of deep neural networks, most commonly used in computer vision applications.
Convolutional refers the network pre-processing data for you - traditionally this pre-processing was performed by data scientists. 
The neural network can learn how to do pre-processing itself by applying filters for things such as edge detection.

In consequence **CNNs** are particularly useful for finding patterns in images to recognize objects, faces, and scenes. 
They learn directly from image data, using patterns to classify images and eliminating the need for manual feature extraction.

<img src="https://miro.medium.com/max/2510/1*vkQ0hXDaQv57sALXAJquxA.jpeg" height="340" width="980"/>

These layers perform operations that alter the data with the intent of learning features specific to the data. Three of the most common layers are: convolution, activation or ReLU, and pooling.

- **Convolution** puts the input images through a set of convolutional filters, each of which activates certain features from the images.
- **Rectified linear unit** (ReLU) allows for faster and more effective training by mapping negative values to zero and maintaining positive values. This is sometimes referred to as activation, because only the activated features are carried forward into the next layer.
- **Pooling** simplifies the output by performing nonlinear downsampling, reducing the number of parameters that the network needs to learn.
These operations are repeated over tens or hundreds of layers, with each layer learning to identify different features.

*Convolutional Networks* are very similar to ordinary ***Artificial Neural Networks*** from the previous chapter: they are made up of neurons that have learnable weights and biases.
Each neuron receives some inputs, performs a dot product and optionally follows it with a non-linearity. The whole network still expresses a single differentiable score function:
from the raw image pixels on one end to class scores at the other. And they still have a loss function (e.g. SVM/Softmax) on the last (fully-connected) layer.

### Using CNNs for deep learning for three important factors:

- CNNs eliminate the need for manual feature extraction—the features are learned directly by the CNN.
- CNNs produce state-of-the-art recognition results.
- CNNs can be retrained for new recognition tasks, enabling you to build on pre-existing networks.

Creating a network from scratch means you determine the network configuration. This approach gives you the most control over the network and can produce impressive results,
but it requires an understanding of the structure of a neural network and the many options for layer types and configuration.
