## Project 2 - Developing a Handwritten Digits Classifier with Pytorch
This project involves training a Convolutional Neural Network(CNN) for classifiying handwritten digits recognition system from the MNIST dataset.

**Network Structure**
1. Two convolutional layers:
- - Conv1: 1 input channel, 10 output channels, 5*5 kernel
- - Conv2: 10 input channes, 20 output channels, 5*5 kernel
2. Two fully connected layers
- - FC1: 320 input features, 50 output features
- - FC2: 50 input features, 10 output features (corresponding to 10 digit classes)
3. Two dropout layers (20% dropout rate) for regularization
4. ReLU activatioin functions and max pooling aftr convolutional layers
5. Log softmax activation for the output layer

**Hyperparameters**
- Optimizer: Adam with learning rate 0.001 and weight decay 1e-5
- Loss function: Negative Log Likelihood Loss (NLLLoss)
- Batch size: 64
- Training duration: 5 epochs with early stopping (patience of 5)

**Performance**
The model achieved excellent performance on the MNIST dataset:
- Final validation accuracy: 98.66%
- Test accuracy: 98.60%
- Test loss: 0.042