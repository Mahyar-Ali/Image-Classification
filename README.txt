# Image-Classification

Image Classification using CIFAR Dataset
-The model is built in Keras [a high-level deep learning library built on top of tensorflow].

The model has a total of 308,394 trainable Parameters.
If you want to build your own model using this architecture then I would recommend you to train the model on google colab, if you do not have access to GPU.
Initially the model was trained only for 40 epochs to test the initial evaluation.
Then I implemented Data Augmentation to increase the performance.
For convenience the notebook is divided into two parts.First without Augmentation and then with Agmentation.
author:m.mahyar.ali --- April 16,2020


Model Architecture:-

Model: "sequential_4"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_19 (Conv2D)           (None, 32, 32, 32)        896       
_________________________________________________________________
batch_normalization_19 (Batc (None, 32, 32, 32)        128       
_________________________________________________________________
conv2d_20 (Conv2D)           (None, 32, 32, 32)        9248      
_________________________________________________________________
batch_normalization_20 (Batc (None, 32, 32, 32)        128       
_________________________________________________________________
max_pooling2d_10 (MaxPooling (None, 16, 16, 32)        0         
_________________________________________________________________
dropout_11 (Dropout)         (None, 16, 16, 32)        0         
_________________________________________________________________
conv2d_21 (Conv2D)           (None, 16, 16, 64)        18496     
_________________________________________________________________
batch_normalization_21 (Batc (None, 16, 16, 64)        256       
_________________________________________________________________
conv2d_22 (Conv2D)           (None, 16, 16, 64)        36928     
_________________________________________________________________
batch_normalization_22 (Batc (None, 16, 16, 64)        256       
_________________________________________________________________
max_pooling2d_11 (MaxPooling (None, 8, 8, 64)          0         
_________________________________________________________________
dropout_12 (Dropout)         (None, 8, 8, 64)          0         
_________________________________________________________________
conv2d_23 (Conv2D)           (None, 8, 8, 128)         73856     
_________________________________________________________________
batch_normalization_23 (Batc (None, 8, 8, 128)         512       
_________________________________________________________________
conv2d_24 (Conv2D)           (None, 8, 8, 128)         147584    
_________________________________________________________________
batch_normalization_24 (Batc (None, 8, 8, 128)         512       
_________________________________________________________________
max_pooling2d_12 (MaxPooling (None, 4, 4, 128)         0         
_________________________________________________________________
dropout_13 (Dropout)         (None, 4, 4, 128)         0         
_________________________________________________________________
flatten_4 (Flatten)          (None, 2048)              0         
_________________________________________________________________
dense_6 (Dense)              (None, 1024)              2098176   
_________________________________________________________________
batch_normalization_25 (Batc (None, 1024)              4096      
_________________________________________________________________
dropout_14 (Dropout)         (None, 1024)              0         
_________________________________________________________________
dense_7 (Dense)              (None, 100)               102500    
_________________________________________________________________
batch_normalization_26 (Batc (None, 100)               400       
_________________________________________________________________
dense_8 (Dense)              (None, 10)                1010      
=================================================================
Total params: 2,494,982
Trainable params: 2,491,838
Non-trainable params: 3,144

Model achieved about 83% accuracy on Test set after training for about 150 epochs.

