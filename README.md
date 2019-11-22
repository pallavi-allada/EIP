# EIP
# Session 1
Score - 99.0

Convolution - It is a dot product operation of 2 matrices typically the kernel/filter with an equal sized sliding window crops of the entire image. This helps in shrinking the size of the image. o/p size of the image = [(i/p size - filter size + 2*padding)/stride size] + 1

Filters/Kernels - This is a learnable matrix of values which are used in the dot product with the sliding window crops of the image. They help in edge detection.

Epochs - The total number of times all the data is passed through the entire network for training i.e both forward and backward propagation is called epochs.

1x1 Convolution - This is a convolution operation with a 1X1 matrix which will keep the height and width of the image unchanged but will change the number of channels. It also helps in reducing the computational cost.

3x3 Convolution - This is a convolution operation with a 3X3 matrix which shrinks the size (height and width) of the image by 2 pixels. A 5X5 convolution is equal to 2 3X3 convolutions.

Feature Maps - Feature map is the output of one kernel passed over the entire image. Each of the kernal output results in a different feature maps.

Activation Function - It is a nonlinear function applied to the output of the summation of weighted neurons and is passed to the next layer neurons to learn the complex relationships between input and the output.

Receptive Field - It is the amount of image that is covered by the filter, typically it is size of the filter. It is of 2 types- Local Receptive field and Global Receptive field. 


# Session 2
Logs - 

Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 9s 147us/step - loss: 0.5216 - acc: 0.8544 - val_loss: 0.0887 - val_acc: 0.9826
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 7s 112us/step - loss: 0.2483 - acc: 0.9275 - val_loss: 0.0561 - val_acc: 0.9877
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1969 - acc: 0.9409 - val_loss: 0.0426 - val_acc: 0.9909
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 7s 112us/step - loss: 0.1686 - acc: 0.9462 - val_loss: 0.0406 - val_acc: 0.9896
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 7s 112us/step - loss: 0.1496 - acc: 0.9505 - val_loss: 0.0379 - val_acc: 0.9897
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 7s 110us/step - loss: 0.1381 - acc: 0.9512 - val_loss: 0.0306 - val_acc: 0.9913
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1292 - acc: 0.9529 - val_loss: 0.0315 - val_acc: 0.9915
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1226 - acc: 0.9525 - val_loss: 0.0270 - val_acc: 0.9929
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1152 - acc: 0.9548 - val_loss: 0.0228 - val_acc: 0.9941
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1123 - acc: 0.9550 - val_loss: 0.0249 - val_acc: 0.9932
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1070 - acc: 0.9558 - val_loss: 0.0224 - val_acc: 0.9937
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 7s 110us/step - loss: 0.1052 - acc: 0.9566 - val_loss: 0.0217 - val_acc: 0.9938
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 7s 111us/step - loss: 0.1047 - acc: 0.9556 - val_loss: 0.0211 - val_acc: 0.9942
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 7s 110us/step - loss: 0.1012 - acc: 0.9564 - val_loss: 0.0199 - val_acc: 0.9944
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0999 - acc: 0.9558 - val_loss: 0.0213 - val_acc: 0.9942
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 7s 114us/step - loss: 0.0968 - acc: 0.9568 - val_loss: 0.0198 - val_acc: 0.9949
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 7s 114us/step - loss: 0.0971 - acc: 0.9568 - val_loss: 0.0215 - val_acc: 0.9942
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0948 - acc: 0.9577 - val_loss: 0.0217 - val_acc: 0.9940
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0948 - acc: 0.9572 - val_loss: 0.0191 - val_acc: 0.9942
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0909 - acc: 0.9584 - val_loss: 0.0192 - val_acc: 0.9944

Model Evaluation Score - 
score = model.evaluate(X_test, Y_test, verbose=0)
print(score)
[0.019158340132655577, 0.9944]

Reduction of kernels in 2nd block helped reduce the number of parameters. No other changes have been done.
