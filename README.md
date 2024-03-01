# S6 - Backpropagation and Advanced Architectures

## Part 1


## Part 2

### As part of this project,

* ***README.md*** will describe what this project comprises and how it is organized and what are we trying to achieve
* ***S6.ipynb*** - It includes code for building model for MNIST dataset, loading dataset and training and evaluating model with data. 



* We have built a model for MNIST dataset which has
   * 5 convolution layers with kernel size 3, padding 1 and with channel sizes ( 4, 8, 16, 24, 32 )
   * Each layer has batch normalization being applied
   * Max pooling layer and dropout layer where dropout is applied for every max pooling layer
   * A Global Average pooling layer which reduces x * y * channels to 1 * 1* channels
   * A Fully connected layer which converts the channels/features obtained from GAP to desired number of class (i.e 10)