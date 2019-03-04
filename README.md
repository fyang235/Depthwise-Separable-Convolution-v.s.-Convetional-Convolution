# Depthwise-Separable-Convolution-v.s.-Convetional-Convolution
This repository compares the performance of Depthwise Separable Convolution and Convetional Convolution.

## As the building block of [Xception](https://arxiv.org/abs/1610.02357), depthwise separable convolution (SCNN) is, as its  author Francois Chollet said, lighter, faster and better. It outperforms the conventional CNN from many aspects and may replace it in the future.  
Is that true? I constructed 3 models to test:
1.  Model_1: Convtional CNN classifier with 7800 parameters.  
2.  Model_2: A SCNN model obtain by replacing the CNN layers in Model_1 with SCNN layers. Its number of parameters is only 1457.
3.  Model_3: Another SCNN model with almost the same number of parameters as Model_1. Its number of parameters is 7841.  

## Let's take a look at the results:  

### Model_1 with 7800 paramters, reach an accuracy of 97.5% after 15 epochs before overfitting  
![](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/cnn-same-layers-para.png)  
![](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/cnn-same-layers-acc.png)  

### Model_2 with only 1457 paramters, reach an accuracy of ~96% after 40 epochs and no sign of overfitting is obversed. We believer its performance can be improved further if more epochs are added. Note that Model_2 only possesses 1/5 the number of paramters of Model_1.       
![](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/scnn-same-layers-para.png)  
![](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/scnn-same-layers-acc.png)    

### Model_3 with 7841 paramters (almost the same as Model_1), reach an accuracy of over 99% after 40 epochs without overfitting. We believer its performance can be improved further if more epochs are added.   
![](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/scnn-same-weights-para.png)  
![](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/scnn-same-weights-acc.png)  

## Conslutions: 
### Francois Chollet is right! The depthwise separable convolution is lighter, faster and better. What's more it mitigates overfitting significantly.  


Checkout [mnist-CNN-FC.ipynb](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/mnist-CNN-FC.ipynb) and 
[mnist-SCNN-FC.ipynb](https://github.com/fyang235/Depthwise-Separable-Convolution-v.s.-Convetional-Convolution/blob/master/mnist-SCNN-FC-Copy1.ipynb) for information.

Enjoy!
