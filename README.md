# EVA


<b>What are Channels and Kernels (according to EVA)?</b>

## Filters/Kernels 

In CNN terminology the 3*3 matrix which is the subset/ traning set of the image is called 'Filter' or 'Kernal'.It is the Feature Extractor which extracts the subject of the image. As shown above in the diagram the blue rectangles in the MRI act as filters which form the subset of image recognition. 

Filters are not defined. The value of each filter is learned during the training process.
Convolutional layer learn to detect abstract concepts, like edges ,outlines or cortex of eyes etc. 
By stacking layers of convolutions on top of each other, we can get more abstract and in-depth information 

A second layer of convolution might help to detect the shapes of eyes ,characteristics of the face and so on. 
This also allows CNNs to perform hierarchical feature learning which is how our brains are thought to identify objects.One of the most important one is edge detection. Edge detection aims to identify pixels of an image at which the brightness changes drasticall

In the image, we can see how the different filters in each CNN layer subpooling layer , interpret the alcohol pattern of the brain.Depending on the kind of problem we are solving and the types of features we are trying to learn, the number of filters used varies . For a larger image , if the number of filters is less the resulting Feature Map would not reveal the inner findings of the image in which case either we increase the number of filters if in permissible range or we use pooling techniques to concentrate the most important part of the image which has to be focussed .

##### <b>Channels</b>

Channels are SIMILAR_FEATURE_BAGS . They are composed of kernels and relate to a single feature within a n image . Likewise Fully-Connected layers, a Convolutional layer has a weight, which is its kernel (filter), and a bias. But in contrast to the fully-connected layers, in convolutional layers each pixel (or neuron) of the output is connected to the input pixels (neurons) locally instead of being connected to all input pixels (neurons). Hence, we use the term of **receptive field** for the size of convolutional layer's filter.

Collection of kernels. you can think of it as a molecule(Every combination of atoms is a molecule).



<b>Why should we only (well mostly) use 3x3 Kernels?</b>

A common choice **is** to keep the **kernel size** at **3x3** . The first convolutional layer **is** often kept larger. Its **size is** less important as there **is** only one first layer, and it has fewer input channels: 3, 1 by color.

The last edges of the matrix are always covered in a **3x3** convolution and hence all the significant features are taken care with **3x3**  kernels.Less filter less computation

<b>How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)</b>

We need to perform 100 iterations to reach 1x1

Input			Iteration			Output			

199x199			2				197x197

197x197			3				195x195

195x195			4				 193x193

193x193			5				 191x191

That is 199, 197, 195, 193, 191

The next 10 like above will 5 iterations 189, 187, 185, 183, 181,

Likewise for 179, 177, 175, 173, 171

​		      169, 167, 165, 163, 161

to reach 1x1 , there are 10 sets of 10 numbers[1-10,10-20,20-30 ……...191-199] like this so 10  x 10 = 100


















