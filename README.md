# hotelid
Hotel ID classification to prevent human trafficking
Uses the 2022 dataset with 49,703 images from 3116 classes. Following is the visualisation of a few samples from the dataset

![Screenshot (529)](https://user-images.githubusercontent.com/76121652/203395133-ebfae5f7-2aa7-4680-9e2a-3b70b82b434a.png)

First used pretrained VGG19 as base network in deep metric loss (triplet loss model). For this training, removed images from classes that contained less than 2 pictures.

![image](https://user-images.githubusercontent.com/76121652/203395663-4561ce80-5c85-45a8-be8e-0ef0273df1ba.png)

After this training, removed final layer and added softmax to classify images. To decrease overfitting, data augmentation applied. Code in Tensorflow, Keras 

Future changes to be made:
Using softmax scores, output 5 possible predictions. Evaluate using Mean average precision.
Try more techniques to prevent overfitting like dropout regularization
Using softmax temperature activation function in final model, instead of softmax 
Pre-training network on hotels50K dataset or arcface dataset 
Need to collect more real world data 

Credits for model ideation: Stanford University Yuyu Lin, Peng Chen, Chi On Ho
