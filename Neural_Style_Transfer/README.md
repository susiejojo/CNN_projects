# Neural Style Transfer to generate Artwork

THe task is to combine a content image(C) with a Style image(S) to create Generated Image(G). 

## Approach

We define a total cost function which is a linear combination of content cost function and style cost function which have been written from scratch. We optimise this total cost function using AdamOptimiser from Tensorflow and return the generated image.

## Implementation

We take a pretrained VGG model and forward propagate the Content and Style images through it to generate their activations. Content cost function is basically the L2-norm of the difference of activations between Content and Generated Images, while style cost function is the L2-norm of Gram matrices of style and generated images. We then added the two cost functions in a linear combination depending on which between content and style images we want to give higher priority to while generating G.

## Packages needed

- scipy
- matplotlib
- numpy
- tensorflow
- PIL

We tested this on a picture of the Louvre Museum as Content and a picture by Monet as Style. After around 200 iterations the algorithm produced visually appealing images.