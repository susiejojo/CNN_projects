# Face recognition and verification using Siamese network

Find implementation of Siamese network and Triplet loss function (trained on MNIST dataset) from scratch at [Siamese net](https://github.com/susiejojo/CNN_projects/tree/master/Siamese_net_MNIST).

## Approach

#### For face verification:

We have used one-shot learning on a Siamese net with the Triplet Loss function which we have written from scratch. By comparing the encoding obtained on a forward pass of the CNN with an input image and comparing the distance of the encoding of the anchor from the encoding of a positive image and that of a negative image, we can find out which image in the database the input image is most similar to.

#### For face recognition:

We compare the encoding of the input(test) image with that of the images in the database. We return the name of the person whose image has the minimum distance to the input image. If the minimum distance is greater than a certain threshold then the input image doesn't belong to anyone in the database.

## Model used

We have used a pre-defined model with a total of 3743280 parameters that inputs (96 x 96) RGB images and outputs a 128-dimensional encoding. This pre-trained model has been compiled with Adam optimizer and optimises the Triplet Loss function during training.
