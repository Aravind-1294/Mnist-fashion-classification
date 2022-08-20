# Mnist-fashion-classification
This is the classification project on Minist fashion data set using CNN. 
Project:
The project started with importing some of the importatn libraries like numpy ,pandas , tensorflow and keras.
for this project i used keras tuner for the hyperparameter tuning of the number of neurons.

so firstly i created a function for the hyperparameters.I used 2 convolution layers then flatten a flatten layer and lastly 2 Dense layers given with different values.Then compiled the process with adam optimizer.

After creating a function now its time to see which parameters perform well for the training dataset, for this process i used RandomSearch. The summary of the model with best parameters :
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 26, 26, 120)       1200      
                                                                 
 conv2d_1 (Conv2D)           (None, 24, 24, 40)        43240     
                                                                 
 flatten (Flatten)           (None, 23040)             0         
                                                                 
 dense (Dense)               (None, 62)                1428542   
                                                                 
 dense_1 (Dense)             (None, 10)                630       
                                                                 
=================================================================
Total params: 1,473,612
Trainable params: 1,473,612
Non-trainable params: 0

Then used the best model on training data, at epoch 1 it reached a accuracy of 94.46%. i took 9 epoch and the accuracy was 99.35%.


