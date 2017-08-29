# Overall
## Deep Learning with S-shaped Rectified Linear Activation Units
This paper proposes a new rectified linear activation unit named SRelu. 
Just a piecewise funciton(three parts). Seems boring.

## Densely Connected Convolutional Networks
This paper extends ResNet and makes network more densely connected.
It proposes that each layer has inputs of all the outputs of its previous layers,
all the outputs are concatenated instead of adding together. 

## Xceptions: Deep Learning with DepthWise Separable Convolutions
This papetr is an extention of Inception, it rethinks the Inception module.
We know **regular conv attempts to learn filters in 3D space, 2D spatial dimensions and a channel dimension**, thus
a single convolution kernel is **tasked with simulataneously mapping cross-channel correlations and spatial correlations.**
Here the author thinks that corss-channel correlations and spatial correlations can be decoupled!

So the depthwise separable convolution is first using 1x1x(high dimension number) conv to get high dimension and then do regular
conv operations each channel(each channel a separable conv kernel, 3x3x1, for example.) Finally, concat the outputs of each conv kernel. Overall, **it does regular conv operations in each channel**

## Create Anime Characters with A.I.!
Results are astonishing, yet method is nothing special. It just adopts a type of existing variant of GAN, and using a clean dataset.
The approach of gathering the dataset deserves learning.

## Real-time single image and video super-resolution using an efficient sub-pixel convolutional neural network. (sub-pixel CNN)
It is quite interesting. As usual, a SR task inputs the LR image and outputs the HR image. Mention: the LR image has the same size as HR one. This paper proposes a
sub-pixel conv which upscale the HR\_little to HR. HR\_little has the size of 1/r(r>1)
size of HR. We just add the sub-pixel conv to the last of the model.

This means the layer takes the input of H\*W\*(r\*r\*C) and outputs (r\*H)\*(r\*W)\*C.
It periodically takes the pixel across the channel to construct the small path of r*r.

## Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network.
Seems the first paper in SR using GAN.

## Instance Normalization:The Missing Ingredient for Fast Stylization
We all know that BN is that we take the whole batch to calcute the mean and variance of the whole batch. However, Instance Norm calculate means and variances(the same number) of the batch.