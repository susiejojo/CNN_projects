# Siamese Network and Triplet Loss

In this project, we have implemented a Siamese network from scratch, trained on the MNIST dataset to optimise the Triplet Loss function which has also been implemented from scratch.

## Theory and approach

The theory being Siamese network and the Triplet loss function has been described in these [notes](https://iiitaphyd-my.sharepoint.com/:o:/g/personal/dipanwita_g_research_iiit_ac_in/Es6SXBA5SmJNrkdJWrpORBkBGO6nRqdJyN7AWL-dZDKu7Q?e=Ddl2YG)

## Model description

```
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense (Dense)                (None, 64)                50240     
_________________________________________________________________
dense_1 (Dense)              (None, 64)                4160      
=================================================================
Total params: 54,400
Trainable params: 54,400
Non-trainable params: 0
```

## Packages Needed

- tensorflow
- matplotlib
- numpy

We have plotted the 2-Dimensional projection of the output encoding for the first 1000 test samples and the loss vs epochs.
