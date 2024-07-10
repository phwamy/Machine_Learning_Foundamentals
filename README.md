# AWS-Udacity Machine Learning Engineer Nanodegree - Machine Learning Foundamentals

Here are projects for AWS-Udacity Machine Learning Engineer Nanodegree - Machine Learning Foundamentals. 

## Project 1 Overview
This project involves using AWS SageMaker and the AutoGluon library to build a forecasting model for the [Bike Sharing Demand Competition](https://www.kaggle.com/c/bike-sharing-demand). The project includes the construction of three distinct models using AutoGluon, with predictions submitted to Kaggle for evaluation:
1. Model using raw features
2. Model with exploratory data analysis (EDA) and feature engineering
3. Model with hyperparameter tuning
    
I have provided a report on exploratory data analysis and reflections on the experiments conducted throughout the project.

**Project Description and Templates**: [github](git@github.com:udacity/nd009t-c1-intro-to-ml-project-starter.git)

**Skills**: Explorative Data Anlaysis, Supervised/Unsupervised/Reinforcement ML, Regression, Classification, Clustering, Random Forest, XGBoost, AutoGluon, AWS SageMaker


## Project 2 Overview
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


## License
[License](LICENSE.txt)
