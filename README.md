# S6 - Backpropagation and Advanced Architectures

## Part 1

As part of this, we need to do forward propagation for the nneural network below to compute values of the neurons and then do backpropagation to minimise the loss between actual value and predicted value.

<img width="607" alt="image" src="https://github.com/das91t70/S6/assets/161017685/6e375c1f-cce1-4a00-a8d0-6f1d62efe199">


### Forward Propagation

All the parameters involved and its description is provided below.

<img width="1052" alt="image" src="https://github.com/das91t70/S6/assets/161017685/78db7d6d-bd44-40b0-8639-639262440895">

### As part of backward propagation, initially we compute partial derivatives and then update the weights with new value 

* updated weight will be w = w - (learning_rate) * ( partial_derivate (output, w))

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/905bb03e-a287-4674-b712-9fd62883dd9f">


### After backpropagation, weights and neurons are changed as below

![image](https://github.com/das91t70/S6/assets/161017685/76648035-00f1-47ca-ab6c-8677ad0340eb)

### Find how the error graph is changing with the learning rates

for the learning rate *0.1*,

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/b86d8a72-87df-45f7-9a04-1d759588c9e6">


for the learning rate *0.2*

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/7fc6065b-9556-4192-af58-030e9494a342">

for the learning rate *0.5*

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/05e0e5f9-4c85-417b-937c-2e44f584186d">

for the learning rate *0.8*

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/06403f20-2c62-4d66-a9a7-7c269379dda2">

for the learning rate *1.0*

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/0a12c9b8-216a-4210-aa11-fc03828bf5b2">


for the learning rate *2.0*

<img width="361" alt="image" src="https://github.com/das91t70/S6/assets/161017685/5765d1dd-6f31-495b-b3f2-dd733eb6845f">



## Part 2

As part of this project,

* ***README.md*** will describe what this project comprises and how it is organized and what are we trying to achieve
* ***S6.ipynb*** - It includes code for building model for MNIST dataset, loading dataset and training and evaluating model with data. 

* We have built a model for MNIST dataset which has
   * 5 convolution layers with kernel size 3, padding 1 and with channel sizes ( 4, 8, 16, 24, 32 )
   * Each layer has batch normalization being applied
   * Max pooling layer and dropout layer where dropout is applied for every max pooling layer
   * A Global Average pooling layer which reduces x * y * channels to 1 * 1* channels
   * A Fully connected layer which converts the channels/features obtained from GAP to desired number of class (i.e 10)

<img width="1052" alt="image" src="https://github.com/das91t70/S6/assets/161017685/ef19b16a-3c1f-40c2-a8f8-472f7e4f5ad0">

 
* We have trained the model with learning rate as 0.01 and momentum as 0.9 and used optimizer as SGD with scheduler as StepLR. Upon testing the model, we achieved accuracy of 99.40% at 17th epoch.

<img width="1052" alt="image" src="https://github.com/das91t70/S6/assets/161017685/c36bbadf-05fb-4c8d-9cd0-889d40f2fb81">
