# Malaria-Computer-Vision-Problem---CNN-Keras
Solving Computer Vision problem with National Library of Medicine dataset containing images of malaria infected/uninfected sets

https://lhncbc.nlm.nih.gov/publication/pub9932

ORIGINAL DATA SOURCE:

The dataset contains 2 folders - Infected - Uninfected

And a total of 27,558 images.

Acknowledgements
This Dataset is taken from the official NIH Website: https://ceb.nlm.nih.gov/repositories/malaria-datasets/ 

**Note: We will be dealing with real image files, NOT numpy arrays. Which means a large part of this process will be learning how to work with and deal with large groups of image files. This is too much data to fit in memory as a numpy array, so we'll need to feed it into our model in batches. **

Generating many manipulated images from a directory
In order to use .flow_from_directory, you must organize the images in sub-directories. This is an absolute requirement, otherwise the method won't work. The directories should only contain images of one class, so one folder per class of images.

Structure Needed:

Image Data Folder
Class 1
0.jpg
1.jpg
...
Class 2
0.jpg
1.jpg
...
...
Class n
![mamal](https://user-images.githubusercontent.com/57037068/83851992-2fc01480-a724-11ea-82e7-3c6b168126b6.png)

Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 128, 128, 32)      896       
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 64, 64, 32)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 62, 62, 64)        18496     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 31, 31, 64)        0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 29, 29, 64)        36928     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 14, 14, 64)        0         
_________________________________________________________________
flatten (Flatten)            (None, 12544)             0         
_________________________________________________________________
dense (Dense)                (None, 128)               1605760   
_________________________________________________________________
activation (Activation)      (None, 128)               0         
_________________________________________________________________
dropout (Dropout)            (None, 128)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 129       
_________________________________________________________________
activation_1 (Activation)    (None, 1)                 0         
=================================================================
Total params: 1,662,209
Trainable params: 1,662,209
Non-trainable params: 0
_________________________
![mala](https://user-images.githubusercontent.com/57037068/83851995-30f14180-a724-11ea-9263-fa5fff316a02.png)
