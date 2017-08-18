# Overall
## Deep Learning with S-shaped Rectified Linear Activation Units
This paper proposes a new rectified linear activation unit named SRelu. 
Just a piecewise funciton(three parts). Seems boring.

## Densely Connected Convolutional Networks
This paper extend ResNet and make network more densely connected.
It proposes that each layer has inputs of all the outputs of its previous layers,
all the outputs are concatenated instead of adding together. 

## Xceptions: Deep Learning with DepthWise Separable Convolutions
This papetr is an extention of Inception, it rethinks the Inception module.
We konw **regular conv attempts to learn filters in 3D space, 2D spatial dimensions and a channel dimension**, thus
a single convolution kernel is **tasked with simulataneously mapping cross-channel correlations and spatial correlations.**
Here the author thinks that corss-channel correlations and spatial correlations can be decoupled!

So the depthwise separable convolution is first using 1x1x(high dimension number) conv to get high dimension and then do regular
conv operations each channel(each channel a separable conv kernel, 3x3x1, for example.) Finally, concat the outputs of each conv kernel. Overall, **it does regular conv operations in each channel**