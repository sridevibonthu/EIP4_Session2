# EIP4_Session2
Assignment 2
# 1. Log


Total params: 14,436
Trainable params: 14,236
Non-trainable params: 200


Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 13s 217us/step - loss: 0.2317 - acc: 0.9264 - val_loss: 0.0680 - val_acc: 0.9781
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 8s 131us/step - loss: 0.0766 - acc: 0.9767 - val_loss: 0.0374 - val_acc: 0.9871
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 8s 129us/step - loss: 0.0557 - acc: 0.9829 - val_loss: 0.0271 - val_acc: 0.9903
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0493 - acc: 0.9845 - val_loss: 0.0289 - val_acc: 0.9895
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 8s 136us/step - loss: 0.0417 - acc: 0.9869 - val_loss: 0.0265 - val_acc: 0.9908
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 8s 131us/step - loss: 0.0370 - acc: 0.9883 - val_loss: 0.0250 - val_acc: 0.9912
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0356 - acc: 0.9885 - val_loss: 0.0225 - val_acc: 0.9920
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 8s 129us/step - loss: 0.0337 - acc: 0.9897 - val_loss: 0.0200 - val_acc: 0.9935
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 8s 126us/step - loss: 0.0301 - acc: 0.9908 - val_loss: 0.0193 - val_acc: 0.9941
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0292 - acc: 0.9905 - val_loss: 0.0202 - val_acc: 0.9937
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0269 - acc: 0.9913 - val_loss: 0.0196 - val_acc: 0.9930
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0256 - acc: 0.9915 - val_loss: 0.0169 - val_acc: 0.9944
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 8s 128us/step - loss: 0.0250 - acc: 0.9918 - val_loss: 0.0187 - val_acc: 0.9931
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 8s 129us/step - loss: 0.0248 - acc: 0.9919 - val_loss: 0.0176 - val_acc: 0.9945
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 8s 130us/step - loss: 0.0251 - acc: 0.9919 - val_loss: 0.0157 - val_acc: 0.9948
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 8s 129us/step - loss: 0.0226 - acc: 0.9928 - val_loss: 0.0169 - val_acc: 0.9945
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 8s 134us/step - loss: 0.0236 - acc: 0.9924 - val_loss: 0.0182 - val_acc: 0.9938
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 8s 134us/step - loss: 0.0221 - acc: 0.9931 - val_loss: 0.0167 - val_acc: 0.9943
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 8s 135us/step - loss: 0.0210 - acc: 0.9933 - val_loss: 0.0160 - val_acc: 0.9945
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 8s 130us/step - loss: 0.0205 - acc: 0.9934 - val_loss: 0.0163 - val_acc: 0.9944
<keras.callbacks.History at 0x7f9be2b016d8>

# 2. result of model.evaluate
score = model.evaluate(X_test, Y_test, verbose=0)
print(score)

[0.016273592712286337, 0.9944]

# 3. strategy followed

I have gone through all the eight models one by one. In code 2, max pooling was introduced after receptive field of 9X9 as it should not be introduced so early, but the number of parameters were too high and they were reduced by reducing number of filters, but accuracy also dropped. Batch normalization standaradizes the inputs, and its impact is observed in the code 4 and the regularization using dropout in code 6. How learning rate is controlled with the help of scheduler in code7 and addition of dropout after every convolution layer at last code.

I have used 140,682 parameters to train my model in my first assignment. By doing assignment 2, I understood with few parameters also we can achieve accuracy.

* I have not much changed the structure of the code which is evolved from code 2 to code 8. I have managed to control the number of filters so that the total number of parameters will be around 15K. 

* I have added BatchNormalization and dropout after every convolution layer except the last one.

* I have added a dropout of 15% at the early convolution layers (before maxpooling) and 12% at the last layers.

* Tried several models and checked the logs.


