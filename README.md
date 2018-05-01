# Weight-dynamics-in-Convolutional-Neural-Network

In this study we visualize in which order the weights in a convolutional neural network CNN converge to their final values. 

The model used for this experiment is composed by three convolutional layers alternated by two max pooling. A flatten layer used to transform the 3D tensor in a 1D output. The vector obtained will fit the densely-connected classifier network composed by a stack of dense layers.

![alt text](https://github.com/ladisasimoneJADS/Weight-dynamics-in-Convolutional-Neural-Network/blob/master/modelSummery.png)

We use a CNN that can classify MNIST digits with an accuracy of 0.9976. Each layer consist of a convolution of the previous layer output (or, in the case of the 1st layer, the input image) with a set of learned weights; passing the response through a rectified linear function (relu(x) = max(x, 0)), max pooling over local neighborhoods. Figure 1. Shows the model used in the experiment. 

We train the model on the 60,000 handwritten digits from the MNIST database. A single training involves 10 epochs, and for the full experiment the training is repeated 30 times. The weights for each layer is collected at the end of every epoch. Normalizing the values obtained allow us to compare the weights and to visualize in which order the three layers converge to their optimal values.

In the experiment we employ Keras deep learning library in python. Keras is a high-level neural network API, written in Python which runs on top of Tensorflow (or Theano).

Results shows that:

-	Layer 1 converge faster at the beginning, but drastically decreases the speed during the training.
-	Layer 2 and 3 converge to their optimal values steadily and gradually.  


![alt text](https://github.com/ladisasimoneJADS/Weight-dynamics-in-Convolutional-Neural-Network/blob/master/weights%20of%20each%20layer%20converging%20to%20the%20optimal%20values..png)
