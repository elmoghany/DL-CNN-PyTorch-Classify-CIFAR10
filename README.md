# Introduction
For the cifar dataset, we want to classify the numbers

# Illustration
1) Training: We train a CNN model on cifar input images
2) Input features: 3*32*32 (RGB channels, width, heigth)
3) Output targets: ['airplane', 'automobile', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck']

# Model & Architecture
1) CNN DL Model
2) 3 convolution layers + batchnorm + leaky_relu
3) CNN img size 32 -> 16 ->  7  -> 2
4) CNN Kernels  3  -> 64 -> 128 -> 256
5) Linear layer + leaky_relu + dropout 0.5
6) inChans  = 3 # RGB => should be changed to 1
7) outChans = 64 # of feature maps / kernels
8) krnSize  = 3x3 # odd number
9) padding  = 0 # No padding
10) stride   = 1 # used stride
11) batchnorm = 1
12) Use of CrossEntropyLoss for classification of 10 targets
13) Minibatches = 32
14) Adam Optimizer with weight decay of 1e-5

# Results
1) Accuracy: Got 97.5% train accuracy and 76% test accuracy for the prediction of the digits of the dataset, which is not goot enough "Overfitting for training data"

# Conclusions:
1) Need to finetune the metaparameters and see what can increase the results
2) Can also read papers about different techniques applied on similar datasets
