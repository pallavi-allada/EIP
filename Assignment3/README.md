# EIP

# Session 3
Validation Accuracy for Base Network after 50 epochs - 0.8240


Model Definition -

model = Sequential()

model.add(SeparableConv2D(48,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False, padding='same',input_shape=(32,32,3))) #(32,32,48) 3
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(96,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (32,32,96) 5
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(192,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (32,32,192) 7
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(MaxPooling2D(2,2)) # (16,16,192) 8
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(48,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (16,16,48) 12
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(96,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (16,16,96) 14
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(192,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (16,16,192) 24
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(MaxPooling2D(2,2)) # (8,8,192) 27
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(48,kernel_size=(3,3), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (8,8,48) 31
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(num_classes,kernel_size=(1,1), activation='relu', dilation_rate=(1, 1), use_bias =False,padding='same')) # (8,8,10) 38

model.add(GlobalAveragePooling2D()) # 10
model.add(Dense(64, activation='relu', use_bias =False)) 
model.add(Dense(num_classes, activation='softmax', use_bias =False)) #10



Logs - Epoch 1/50
390/390 [==============================] - 25s 64ms/step - loss: 1.5959 - acc: 0.4015 - val_loss: 1.5530 - val_acc: 0.4515
Epoch 2/50
390/390 [==============================] - 18s 47ms/step - loss: 1.1589 - acc: 0.5755 - val_loss: 1.2458 - val_acc: 0.5639
Epoch 3/50
390/390 [==============================] - 18s 47ms/step - loss: 0.9727 - acc: 0.6503 - val_loss: 0.9766 - val_acc: 0.6521
Epoch 4/50
390/390 [==============================] - 19s 47ms/step - loss: 0.8674 - acc: 0.6900 - val_loss: 0.9841 - val_acc: 0.6575
Epoch 5/50
390/390 [==============================] - 18s 47ms/step - loss: 0.7925 - acc: 0.7171 - val_loss: 0.8722 - val_acc: 0.6957
Epoch 6/50
390/390 [==============================] - 18s 47ms/step - loss: 0.7322 - acc: 0.7401 - val_loss: 0.8306 - val_acc: 0.7141
Epoch 7/50
390/390 [==============================] - 18s 47ms/step - loss: 0.6912 - acc: 0.7555 - val_loss: 0.8013 - val_acc: 0.7203
Epoch 8/50
390/390 [==============================] - 18s 47ms/step - loss: 0.6513 - acc: 0.7705 - val_loss: 0.7526 - val_acc: 0.7483
Epoch 9/50
390/390 [==============================] - 19s 47ms/step - loss: 0.6154 - acc: 0.7827 - val_loss: 0.7908 - val_acc: 0.7363
Epoch 10/50
390/390 [==============================] - 19s 48ms/step - loss: 0.5881 - acc: 0.7938 - val_loss: 0.7632 - val_acc: 0.7399
Epoch 11/50
390/390 [==============================] - 18s 47ms/step - loss: 0.5665 - acc: 0.8001 - val_loss: 0.6667 - val_acc: 0.7754
Epoch 12/50
390/390 [==============================] - 18s 47ms/step - loss: 0.5460 - acc: 0.8069 - val_loss: 0.7003 - val_acc: 0.7730
Epoch 13/50
390/390 [==============================] - 18s 47ms/step - loss: 0.5277 - acc: 0.8150 - val_loss: 0.7044 - val_acc: 0.7659
Epoch 14/50
390/390 [==============================] - 19s 48ms/step - loss: 0.5100 - acc: 0.8206 - val_loss: 0.6385 - val_acc: 0.7841
Epoch 15/50
390/390 [==============================] - 18s 47ms/step - loss: 0.5008 - acc: 0.8243 - val_loss: 0.6187 - val_acc: 0.7946
Epoch 16/50
390/390 [==============================] - 18s 47ms/step - loss: 0.4803 - acc: 0.8307 - val_loss: 0.6577 - val_acc: 0.7841
Epoch 17/50
390/390 [==============================] - 19s 48ms/step - loss: 0.4668 - acc: 0.8349 - val_loss: 0.6499 - val_acc: 0.7873
Epoch 18/50
390/390 [==============================] - 18s 47ms/step - loss: 0.4599 - acc: 0.8374 - val_loss: 0.5679 - val_acc: 0.8101
Epoch 19/50
390/390 [==============================] - 19s 48ms/step - loss: 0.4477 - acc: 0.8435 - val_loss: 0.6420 - val_acc: 0.7887
Epoch 20/50
390/390 [==============================] - 19s 47ms/step - loss: 0.4395 - acc: 0.8434 - val_loss: 0.5868 - val_acc: 0.8028
Epoch 21/50
390/390 [==============================] - 18s 47ms/step - loss: 0.4267 - acc: 0.8501 - val_loss: 0.5999 - val_acc: 0.8019
Epoch 22/50
390/390 [==============================] - 19s 48ms/step - loss: 0.4125 - acc: 0.8556 - val_loss: 0.6055 - val_acc: 0.8075
Epoch 23/50
390/390 [==============================] - 19s 47ms/step - loss: 0.4081 - acc: 0.8559 - val_loss: 0.5579 - val_acc: 0.8183
Epoch 24/50
390/390 [==============================] - 18s 47ms/step - loss: 0.4046 - acc: 0.8576 - val_loss: 0.5278 - val_acc: 0.8246
Epoch 25/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3964 - acc: 0.8598 - val_loss: 0.5514 - val_acc: 0.8197
Epoch 26/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3866 - acc: 0.8638 - val_loss: 0.5614 - val_acc: 0.8192
Epoch 27/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3834 - acc: 0.8654 - val_loss: 0.5891 - val_acc: 0.8104
Epoch 28/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3709 - acc: 0.8694 - val_loss: 0.5619 - val_acc: 0.8179
Epoch 29/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3695 - acc: 0.8692 - val_loss: 0.6127 - val_acc: 0.8007
Epoch 30/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3654 - acc: 0.8708 - val_loss: 0.5399 - val_acc: 0.8288
Epoch 31/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3569 - acc: 0.8739 - val_loss: 0.6251 - val_acc: 0.8053
Epoch 32/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3512 - acc: 0.8767 - val_loss: 0.5845 - val_acc: 0.8155
Epoch 33/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3434 - acc: 0.8789 - val_loss: 0.5367 - val_acc: 0.8226
Epoch 34/50
390/390 [==============================] - 19s 47ms/step - loss: 0.3465 - acc: 0.8777 - val_loss: 0.5746 - val_acc: 0.8161
Epoch 35/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3338 - acc: 0.8812 - val_loss: 0.5266 - val_acc: 0.8284
Epoch 36/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3377 - acc: 0.8806 - val_loss: 0.5238 - val_acc: 0.8338
Epoch 37/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3293 - acc: 0.8835 - val_loss: 0.5254 - val_acc: 0.8337
Epoch 38/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3235 - acc: 0.8846 - val_loss: 0.5248 - val_acc: 0.8336
Epoch 39/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3211 - acc: 0.8851 - val_loss: 0.5309 - val_acc: 0.8319
Epoch 40/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3155 - acc: 0.8864 - val_loss: 0.5433 - val_acc: 0.8288
Epoch 41/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3141 - acc: 0.8881 - val_loss: 0.5385 - val_acc: 0.8274
Epoch 42/50
390/390 [==============================] - 19s 47ms/step - loss: 0.3066 - acc: 0.8916 - val_loss: 0.5260 - val_acc: 0.8318
Epoch 43/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3094 - acc: 0.8905 - val_loss: 0.5196 - val_acc: 0.8348
Epoch 44/50
390/390 [==============================] - 18s 47ms/step - loss: 0.2998 - acc: 0.8940 - val_loss: 0.5140 - val_acc: 0.8345
Epoch 45/50
390/390 [==============================] - 18s 47ms/step - loss: 0.3051 - acc: 0.8923 - val_loss: 0.5217 - val_acc: 0.8356
Epoch 46/50
390/390 [==============================] - 18s 47ms/step - loss: 0.2934 - acc: 0.8946 - val_loss: 0.5590 - val_acc: 0.8212
Epoch 47/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3003 - acc: 0.8926 - val_loss: 0.5686 - val_acc: 0.8220
Epoch 48/50
390/390 [==============================] - 19s 47ms/step - loss: 0.2849 - acc: 0.8990 - val_loss: 0.5417 - val_acc: 0.8310
Epoch 49/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2875 - acc: 0.8965 - val_loss: 0.5111 - val_acc: 0.8406
Epoch 50/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2896 - acc: 0.8968 - val_loss: 0.5383 - val_acc: 0.8272
Model took 933.56 seconds to train

Accuracy on test data is: 82.72



