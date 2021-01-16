# Mask RCNN for Brick Kiln Detection

Mask R-CNN has been the new state of art in terms of instance segmentation. Mask R-CNN is a deep neural network aimed to solve instance segmentation problem in machine learning or computer vision. In other words, it can separate different objects in a image or a video. We give an image, it gives us the object bounding boxes, classes and masks.

There are two stages of Mask R-CNN.
  * First, it generates proposals about the regions where there might be an object based on the input image.
  * Second, it predicts the class of the object, refines the bounding box and generates a mask in pixel level of the object based on the first stage proposal. Both stages are connected to the backbone structure.
  
In this project I have trained my own Mask RCNN model for detecting Brick Kilns in satellite images
