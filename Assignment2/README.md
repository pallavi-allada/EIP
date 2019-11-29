# EIP

# Session 2
Logs - 

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 8s 132us/step - loss: 0.2139 - acc: 0.9312 - val_loss: 0.0610 - val_acc: 0.9794
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0609 - acc: 0.9810 - val_loss: 0.0570 - val_acc: 0.9826
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0489 - acc: 0.9847 - val_loss: 0.0337 - val_acc: 0.9892
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0389 - acc: 0.9880 - val_loss: 0.0262 - val_acc: 0.9917
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 6s 97us/step - loss: 0.0363 - acc: 0.9885 - val_loss: 0.0318 - val_acc: 0.9907
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0326 - acc: 0.9892 - val_loss: 0.0246 - val_acc: 0.9925
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0302 - acc: 0.9904 - val_loss: 0.0288 - val_acc: 0.9909
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 6s 95us/step - loss: 0.0274 - acc: 0.9911 - val_loss: 0.0214 - val_acc: 0.9931
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 6s 95us/step - loss: 0.0257 - acc: 0.9913 - val_loss: 0.0296 - val_acc: 0.9914
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0238 - acc: 0.9921 - val_loss: 0.0247 - val_acc: 0.9911
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0227 - acc: 0.9928 - val_loss: 0.0211 - val_acc: 0.9938
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 6s 95us/step - loss: 0.0215 - acc: 0.9937 - val_loss: 0.0237 - val_acc: 0.9921
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 6s 97us/step - loss: 0.0208 - acc: 0.9932 - val_loss: 0.0195 - val_acc: 0.9940
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0194 - acc: 0.9939 - val_loss: 0.0253 - val_acc: 0.9912
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0195 - acc: 0.9937 - val_loss: 0.0181 - val_acc: 0.9948
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0176 - acc: 0.9943 - val_loss: 0.0199 - val_acc: 0.9935
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 6s 95us/step - loss: 0.0176 - acc: 0.9941 - val_loss: 0.0178 - val_acc: 0.9936
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 6s 97us/step - loss: 0.0177 - acc: 0.9941 - val_loss: 0.0254 - val_acc: 0.9915
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0174 - acc: 0.9941 - val_loss: 0.0191 - val_acc: 0.9943
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 6s 96us/step - loss: 0.0161 - acc: 0.9946 - val_loss: 0.0192 - val_acc: 0.9942

Model Evaluation Score - 
score = model.evaluate(X_test, Y_test, verbose=0)
print(score)
[0.01916026868662593, 0.9942]

Strategy -
Reduction of kernels in 2nd block from 32 to 16 helped reduce the number of parameters. Removed biases at each Conv layer and BatchNorm and Dropouts at last layer.
