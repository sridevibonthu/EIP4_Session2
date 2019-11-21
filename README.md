# EIP4_Session2
Assignment 2
# 1. Log
Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 9s 151us/step - loss: 0.2319 - acc: 0.9265 - val_loss: 0.0718 - val_acc: 0.9761
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0649 - acc: 0.9793 - val_loss: 0.0324 - val_acc: 0.9894
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0491 - acc: 0.9843 - val_loss: 0.0329 - val_acc: 0.9894
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0445 - acc: 0.9857 - val_loss: 0.0255 - val_acc: 0.9917
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 7s 109us/step - loss: 0.0385 - acc: 0.9877 - val_loss: 0.0245 - val_acc: 0.9914
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 7s 109us/step - loss: 0.0355 - acc: 0.9888 - val_loss: 0.0238 - val_acc: 0.9930
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 7s 109us/step - loss: 0.0320 - acc: 0.9895 - val_loss: 0.0228 - val_acc: 0.9927
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 7s 109us/step - loss: 0.0315 - acc: 0.9899 - val_loss: 0.0223 - val_acc: 0.9915
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 7s 109us/step - loss: 0.0296 - acc: 0.9906 - val_loss: 0.0233 - val_acc: 0.9925
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0286 - acc: 0.9909 - val_loss: 0.0186 - val_acc: 0.9932
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0259 - acc: 0.9919 - val_loss: 0.0204 - val_acc: 0.9929
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 7s 108us/step - loss: 0.0256 - acc: 0.9923 - val_loss: 0.0211 - val_acc: 0.9931
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0245 - acc: 0.9923 - val_loss: 0.0180 - val_acc: 0.9937
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 7s 109us/step - loss: 0.0248 - acc: 0.9919 - val_loss: 0.0191 - val_acc: 0.9934
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0223 - acc: 0.9928 - val_loss: 0.0202 - val_acc: 0.9933
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0206 - acc: 0.9934 - val_loss: 0.0204 - val_acc: 0.9940
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0221 - acc: 0.9929 - val_loss: 0.0177 - val_acc: 0.9946
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0217 - acc: 0.9931 - val_loss: 0.0177 - val_acc: 0.9941
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 7s 108us/step - loss: 0.0190 - acc: 0.9939 - val_loss: 0.0186 - val_acc: 0.9943
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0204 - acc: 0.9934 - val_loss: 0.0173 - val_acc: 0.9944
<keras.callbacks.History at 0x7fd2d319fc18>


# 2. result of model.evaluate
score = model.evaluate(X_test, Y_test, verbose=0)
print(score)

[0.01733853554037414, 0.9944]

# 3. strategy followed

I have gone through all the eight models one by one. In code 2, max pooling was introduced after receptive field of 9X9 as it should not be introduced so early, but the number of parameters were too high and they were reduced by reducing number of filters, but accuracy also dropped. Batch normalization standaradizes the inputs, and its impact is observed in the code 4 and the regularization using dropout in code 6. How learning rate is controlled with the help of scheduler in code7 and addition of dropout after every convolution layer at last code.

I have used 140,682 parameters to train my model in my first assignment. By doing assignment 2, I understood with few parameters also we can achieve accuracy.

* I have not much changed the structure of the code which is evolved from code 2 to code 8. I have managed to control the number of filters so that the total number of parameters will be around 15K. 

* I have added BatchNormalization and dropout after every convolution layer except the last one.

* I have added a dropout of 15% at the early convolution layers (before maxpooling) and 12% at the last layers.

* Tried several models and checked the logs.


