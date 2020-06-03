# Detecting and labeling objects from a Video using DarkNet

Saves an annotated video containing bounding boxes as well as class predictions of detected objects with their confidences from a video.

## Approach

Darknet provides the tinyYOLO model which is capable of working with high frame rates(60-70 FPS) and real time object detection and labelling on limited hardware resources. The bigger YOLOv3 model is more efficient, but works with lower frame rates. In this project, we have used the tinyYOLO model. Since darknet's detector doesn't save the annoted video, we used a CLI to annotate the video based on the outputs of the CNN and save the video as output.mp4.

## Annotating

We took the outputs of the Darknet CNN trained on the Coco dataset, which contains bounding box locations and size, class labels for each anchor box corresponding to the grid boxes. Based on whether the confidence of prediction is higher than a given threshold, we performed Non-Max Suppression (based on IOU) to get rid of all but the most accurate bounding box, and we labelled and displayed the bounding box using OpenCV with the predicted class label among 80 predefined classes.

## Packages needed

- OpenCV
- Darknet (for installation: `git clone https://github.com/pjreddie/darknet`)
- Numpy
- Argparse

This was tested on 3 videos containing various objects like buses, cars, traffic signals, people etc. It was able to detect the objects with their locations and class labels with decent accuracy.
 


