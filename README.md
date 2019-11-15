# EIP
99.0
Convolution - It is a dot product operation of 2 matrices typically the kernel/filter with an equal sized sliding window crops of the entire image. This helps in shrinking the size of the image. o/p size of the image = [(i/p size - filter size + 2*padding)/stride size] + 1

Filters/Kernels - This is a learnable matrix of values which are used in the dot product with the sliding window crops of the image. They help in edge detection.

Epochs - The total number of times all the data is passed through the entire network for training i.e both forward and backward propagation is called epochs.

1x1 Convolution - This is a convolution operation with a 1X1 matrix which will keep the height and width of the image unchanged but will change the number of channels. It also helps in reducing the computational cost.

3x3 Convolution - This is a convolution operation with a 3X3 matrix which shrinks the size (height and width) of the image by 2 pixels. A 5X5 convolution is equal to 2 3X3 convolutions.

Feature Maps - Feature map is the output of one kernel passed over the entire image. Each of the kernal output results in a different feature maps.

Activation Function - It is a nonlinear function applied to the output of the summation of weighted neurons and is passed to the next layer neurons to learn the complex relationships between input and the output.

Receptive Field - It is the amount of image that is covered by the filter, typically it is size of the filter. It is of 2 types- Local Receptive field and Global Receptive field. 
