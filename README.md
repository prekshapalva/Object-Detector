## "Object Detector" - Real time object detector and identifier

The "Oject Detector" is an OpenCV project that detects and identifies the objects placed infront of the camera and displays the output on a webpage.

### :one: Introduction
This project focuses on building a object detection model. It is a form of computer vision, image processing, and deep learning amalgam that detects instances of objects in images and videos. This project uses the YOLO object detector to detect objects in images and video streams. The data set from [yolo-coco-data](https://www.kaggle.com/datasets/valentynsichkar/yolo-coco-data).

### :two: Prerequisites
Python, OpenCV and Deep learning knowledge

### :three: What is YOLO?
In May 2016, Joseph Redmon introduced the YOLO algorithm, which stands for "You only look once". The algorithm's name may sound strange, but it describes it perfectly as it predicts classes and bounding boxes for the entire image in just one run. In terms of speed and accuracy, YOLO performed much better than other single-shot detectors at the time. This algorithm may not be the most accurate when it comes to object detection, but it certainly makes up for this with its impressive speed.

### :four: Overwiew of YOLO object detection algorithm
In the YOLO network, the input image is split into a grid of S×S cells. An object's existence can be detected if the center of the ground truth box falls into a cell. A grid cell predicts the number of bounding boxes, their objectness score, and their class as the following:
1. B bounding box coordinates -YOLO predicts four coordinates for each bounding box (bx,by,bw,bh) with respect to the corresponding grid cell. In this case, bx, by are the x and y coordinates of the midpoint of the object on this grid. As a result, bh is the ratio of the bounding box height to the grid cell height, and bw is the ratio of the bounding box width to the grid cell width. 
2. Objectness score (P0) - indicates whether or not a cell contains an object. By passing the objectness score through a sigmoid function, it is converted into a probability range between 0 and 1. 
3. Class prediction – if the bounding box contains an object, the network predicts the probability of K number of classes. The total number of classes in your problem is K.

Then, the bounding box confidence score and class prediction are combined into one final score that tells us whether or not the bounding box contains a specific type of object.

### :five: Conclusion
In this project, OpenCV module with pre-trained YOLO model is used to detect objects. Remember, this is just the tip of the iceberg., because there is alot more than this in Object detection. Thank you!
