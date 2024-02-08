# Semantic Segmentation from small training set using Transfer Learning for Feature Extraction
This is an example of Transfer Learning to extract features for a Semantic Segmentation problem.

Labeling is a process that is hard, and expensive (in time, money, resources). The problem I'm trying to solve here is to use the smallest amount of training data possible to come up is a model that can segment the images correctly.

In order to do this, I'm using a technique called *Transfer Learning*. I dissected a previously fully train model used in image classification (VGG16) and using it to extract features from the images. Then, I built a standard Random Forest Classifier to classify these features using as target classes, the classes of the masks in the training set.

The inferece is done in a similar way, using the trimmed VGG16 model to extract the features of the image, and then classifying the features using the RF fitted model.

I'm using the [EPFL Electron Microscopy Dataset](https://www.epfl.ch/labs/cvlab/data/data-em/) and training using only 10 images.

Spoiler alert: the results are 💩💩💩💩

<img src=images/predicted.png/> <img src=images/ground_truth.png/>
