# Part 1: backpropagation_excelsheet_wk6_era
Backpropagation calculations on excel sheet. 

The excel file has a simple neural network along with various mathematical formulas related to backpropagation and weight updates.

![main_image](images/network_formulae.png "main screenshot")

## Overview of the Neural Network:

- Input Layer: There are two input features, labeled as i1 and i2 nodes.
- Hidden Layer: The hidden layer has two neurons labeled as h1 and h2. The connections between the input and hidden layers have associated weights w1, w2, w3 and w4.
- Output Layer: Two output nodes are o1 and o2, showing the predicted values. The weights from the hidden layer to the output layer are labeled w5, w6, w7 and w8.
- Activation Functions: The hidden and output layers use sigmoid as activation function, as indicated by the sigma symbol.
- Errors: The outputs have errors E1 and E2 which are calculated with the help of predicted (o1, o2) and target (t1, t2) values, which are part of the total error E_Total.

## Neural Network Formulae
The image above shows colored blocks numbered from 1 to 6. 
- Block 1: It gives association of different parameters from input layer to the final error.
- Block 2: Relations for the partial derivative of final error and associated parameters. 
- Block 3: The partial derivative of the final error wrt the weights w5, w6, w7 and w8. These are useful in update of the weights and in block-4.
- Block 4: Intermediate partial derivatives of the error wrt parameters a_h1 and a_h2 to be used in block-5.
- Block 5: Partial derivatives of the final error wrt weights w1, w2, w3 and w4.
- Block 6: Expansion of block-5 formulae by using block-4.

#### Gradient descent weight update rule for all weight `i`:

w_i(new) = w_i(old) - LearningRate * ∂E_Total/∂w_i

## Loss plots for different learning rates
Following images show that the network learns very quick (i.e. loss decreases fast) as the learning rate increases.

#### Learning rate = 0.1 
![loss1_image](images/loss_with_rate_0.1.png "loss1 screenshot")


#### Learning rate = 0.2
![loss1_image](images/loss_with_rate_0.2.png "loss1 screenshot")

#### Learning rate = 0.5
![loss1_image](images/loss_with_rate_0.5.png "loss1 screenshot")

#### Learning rate = 0.8
![loss1_image](images/loss_with_rate_0.8.png "loss1 screenshot")

#### Learning rate = 1.0
![loss1_image](images/loss_with_rate_1.0.png "loss1 screenshot")

#### Learning rate = 2.0
![loss1_image](images/loss_with_rate_2.0.png "loss1 screenshot")


# Part 2: Neural Network for Image Classification

## Overview (S6/assignment_week6.ipynb)

This project contains a PyTorch script for training and evaluating neural network models. Here the parameters within the script have been finalized to satisfy the requirement of having minimum accuracy of 99.4% in validation. Following list of parameters underwent variations:
- Total number of blocks/layers (`conv1`, `conv2`, `conv3`, `gap`, `conv4`)
- Number of parameters (`size1`, `size2`, `size3`) within each layer
- Number of maxpooling layers and location
- Dropout value `drop_value`
- Average pooling and convolution with 1x1 kernel
- Scaling of learning rate with `lr_scheduler`
- Pytorch manual seed value
- Training dataset: resize, random rotation and crop

## Features

- Neural network model definitions using PyTorch.
- Data loading and preprocessing with torchvision.
- Configurable network parameters and training settings.

## Requirements

- PyTorch
- torchvision


