# Face recognition and verification using One-Shot Learning

## Approach

#### For face verification:

We have used one-shot learning with the Triplet Loss function which we have written from scratch. By comparing the encoding obtained on a forward pass of the CNN with an input image and calculating if the distance of the encoding with that of the actual image of the person is less than a threshold, we can perform face verification.

#### For face recognition:

We compare the encoding of the input(test) image with that of the images in the database. We return the name of the person whose image has the minimum distance to the input image. If the minimum distance is greater than a certain threshold then the input image doesn't belong to anyone in the database.

## Model used

We have used a pre-trained model with a total of 3743280 parameters that inputs (96 x 96) RGB images and outputs a 128-dimensional encoding. This pre-trained model has been compiled with Adam optimizer and optimises the Triplet Loss function.