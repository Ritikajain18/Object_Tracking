# Object_Tracking 👀

## Tracks the objects using bounding boxes  

## Key Takeaways:
1. Steps involved:
    1. Detect the objects in the image and calculate their centroids.
    2. Find out the previous occurrence of that all those objects using euclidean distance. Some objects might be new and some might have gone out of frame.
    3. Track the objecs as it moves around in the video and print the associated id with them.
 
2. This approach is based on Centroid tracking.
3. Euclidean distance is used to calculate the distance between new objects detections and previous ones.
4. The smaller the euclidean distance of new object to the old object, the more are the chances of it being the same old object.
5. The bounding boxes can be produced by any type of object detector like (color thresholding + contour extraction, Haar Cascades, HOG + Linear SVM, Faster RCNNs, etc.)
6. Video stream from webcam is used in this project to do object tracking.
7. Masking is used to ignore smaller and unnecessary objects.

## Requirments: 
1. python (3.7.3)
2. opencv (4.1.0)
3. numpy (1.61.4)
4. imutils (0.5.2)

## Limitations:
1. This project requires the object detection to be run on every frame of the video. This could be slow for heavy deep learning based detector, but can work for fast detectors (like color thresholding and Haar cascades) that don't do heavy computations.
2. The centroid tacking algorithm requires that the centroids must lie close together between subsequent frames.
3. There could be object id switching if the objects overlap each other.




