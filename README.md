# Mask RCNN for Brick Kiln Detection

Mask R-CNN is the new state of art model in terms of instance segmentation. Mask R-CNN is a deep neural network aimed to solve the instance segmentation problem in machine learning or computer vision. In other words, it can separate different objects in a image or a video. We give an image, it gives us the object bounding boxes, classes and masks.

There are two stages of Mask R-CNN.
  * First, it generates proposals about the regions where there might be an object based on the input image.
  * Second, it predicts the class of the object, refines the bounding box and generates a mask in pixel level of the object based on the first stage proposal. Both stages are connected to the backbone structure.
  
In this project I have trained my own Mask RCNN model for detecting Brick Kilns in satellite images.

## Image Annotation

Firstly, we need to annotate or select the region we want to see mask in the image. We need to do this for all the training and validation images. This is called annotation of images, through which the model will come to know which object it needs to detect. For this I have used <a href="https://imglab.in/">ImgLab</a> tool. 

After performing annotations for all images we need to download the annotations as a COCO JSON file which we will use to train our model.

## Training the model

<a href="https://github.com/shankhanil007/Mask-RCNN-for-Brick-Kiln/blob/main/Training_and_Testing.ipynb">Training_and_Testing.ipynb</a> file is where the code for training the model is present. For detecting any other object, things that needs to be changed in the file are :
 * Path of training and validation images + annotations
 * Path of testing images directory
 * Number of classes
 * Number of epochs and steps per epoch ( Need to experiment a bit to get the desired accuracy )
 
## Testing the model

If you are using the <a href="https://github.com/shankhanil007/Mask-RCNN-for-Brick-Kiln/blob/main/Training_and_Testing.ipynb">Training_and_Testing.ipynb</a> file, then the testing code is present in it and it uses the last trained model. But if you have already trained the model and you are having the (.h5) weights file, then use <a href="https://github.com/shankhanil007/Mask-RCNN-for-Brick-Kiln/blob/main/Testing_for_any_Downloaded_Model.ipynb">Testing_for_any_Downloaded_Model.ipynb</a> file and make changes in it accordingly.
