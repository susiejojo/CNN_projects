# Traffic Signs Classifier built using CNN

Classifies images of traffic signs from a dataset of 34799 images into 43 classes of signs.

## Packages needed

- sklearn
- seaborn
- matplotlib
- pickle
- numpy
- tensorflow
- pandas
- keras

## Input description

34799 colored images of size 32 x 32 x 3 each. Consists of close-cropped images of traffic-signals corresponding to 43 different classes.

## Model description

```Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_13 (Conv2D)           (None, 28, 28, 6)         156       
_________________________________________________________________
average_pooling2d_11 (Averag (None, 14, 14, 6)         0         
_________________________________________________________________
dropout_3 (Dropout)          (None, 14, 14, 6)         0         
_________________________________________________________________
conv2d_14 (Conv2D)           (None, 10, 10, 16)        2416      
_________________________________________________________________
average_pooling2d_12 (Averag (None, 5, 5, 16)          0         
_________________________________________________________________
flatten_4 (Flatten)          (None, 400)               0         
_________________________________________________________________
dense_12 (Dense)             (None, 120)               48120     
_________________________________________________________________
dense_13 (Dense)             (None, 84)                10164     
_________________________________________________________________
dense_14 (Dense)             (None, 43)                3655      
=================================================================
Total params: 64,511
Trainable params: 64,511
Non-trainable params: 0
```
## Training parameters
- Epochs: 50
- Optimizer: Adam
- Loss: sparse_categorical_crossentropy
- Batch_size: 500

## Results

- Training accuracy: 98.46%
- Validation accuracy: 90.20%
- Test-set accuracy: 89.51%

Plotted confusion matrix and displayed labels and predictions from a random set of 25 images chosen from testset.