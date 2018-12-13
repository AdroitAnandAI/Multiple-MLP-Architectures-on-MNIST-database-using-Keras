# Multiple MLP Architectures using Keras on MNIST #

To use different MLP architectures having different number of layers on the famous MNIST database. Tweaking methods like dropouts, batch normalization are applied and cross entropy loss is being tracked for analysis and comparison between architectures.

## Purpose ##

The purpose of the study is to try out **3 different MLP architectures on MNIST dataset to compare the performance**. The implementation is done in Keras.

## Steps at a Glance: ##

1. Take the famous **MNIST** dataset as input. http://yann.lecun.com/exdb/mnist/

2. Feed it into **2-layered MLP Architecture: Input(784)-ReLu(512)-ReLu(128)-Sigmoid(output)**

3. Find the accuracy and draw the **Loss vs Epoch Plot**

4. Introduce **Batch Normalization and Dropouts**.

5. Evaluate the model again by estimating accuracy and drawing loss diagram.

6. Feed same input to **3 layered MLP Architecture: Input(784)-ReLu(512)-ReLu(256)-ReLu(64)-Sigmoid(output)**

7. Introduce Batch Normalization and Dropouts & evaluate the model again.

8. Feed same input to **5 layered MLP Architecture: Input(784)-ReLu(512)-ReLu(256)-ReLu(144)-ReLu(96)-ReLu(36)-Sigmoid(output)**

9. Introduce Batch Normalization and Dropouts & evaluate the model again.

10. Analyze the output from the above 3 architectures and draw conclusions .

## Model 1: (2-layered MLP Architecture) ##

### Input(784)-ReLu(512)-ReLu(128)-Softmax(output) ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.1.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.1.1.2.PNG">
</p>

### M1 + Batch-Normalization on hidden Layers ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.1.2.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.1.2.2.PNG">
</p>

### M1 + Batch-Normalization + Dropout ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.1.3.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.1.3.2.PNG">
</p>

## Model 2 (3-layered MLP Architecture) ##

### Input(784)-ReLu(512)-ReLu(256)-ReLu(64)-Softmax(output) ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.2.2.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.2.2.2.PNG">
</p>

### M2 + Batch-Normalization on 3 hidden Layers ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.2.3.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.2.3.2.PNG">
</p>

### M2 + Batch-Normalization + Dropout ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.2.4.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.2.4.2.PNG">
</p>

## Model 3 (5-layered MLP Architecture) ##

### Input(784)-ReLu(512)-ReLu(256)-ReLu(144)-ReLu(96)-ReLu(36)-Softmax(output) ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.3.2.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.3.2.2.PNG">
</p>

### M3 + Batch-Normalization on 5 hidden Layers ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.3.3.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.3.3.2.PNG">
</p>

### M3 + Batch-Normalization + Dropout ###

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.3.4.1.PNG">
</p>

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/3.3.4.2.PNG">
</p>

## Summary Statistics ##

<p align="center">
    <img src="https://github.com/AdroitAnandAI/Multiple-MLP-Architectures-on-MNIST-database-using-Keras/blob/master/images/4.PNG">
</p>

## Conclusions ##

1. The **difference in accuracy between 2, 3 & 5 layered networks is very small**. This could be due to the simplicity and small size of input data.

2. The **’cross entropy loss vs epoch’ plot** for train and test data is found **diverging, when the dropout layer is not added**. This means reduction in training loss but increase in test loss at the same time, **indicative of overfitting**.

3. Thus, **addition of dropout layer is found as a good regularization** in practice.

4. The accuracy is also more when Batch Normalization and dropout layers are added.

5. All distributions of trained weights along all the layers are expectedly found as Gaussian curves.

6. For MNIST problem, **model M1 coupled with Batch Normalizaton and Dropout seems to be the best bet**.
