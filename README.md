# Drowsiness-Detection-
Drowsiness detection is a safety technology that can prevent accidents that are caused by drivers who fell asleep while driving. The objective of this project is to build a drowsiness detection system that will detect drowsiness through the implementation of computer vision system that automatically detects drowsiness in real-time from a live video stream and then alert the user with an alarm sound.

# Motivation
According to the National Highway Traffic Safety Administration, every year about 100,000 police-reported crashes involve drowsy driving. These crashes result in more than 1,550 fatalities and 71,000 injuries. The real number may be much higher, however, as it is difficult to determine whether a driver was drowsy at the time of a crash. So, we tried to build a system, that detects whether a person is drowsy and alert him.

# Built With
-OpenCV Library - Most used computer vision library. Highly efficient. Facilitates real-time image processing.
-imutils library - A collection of helper functions and utilities to make working with OpenCV easier.
-Dlib library - Implementations of state-of-the-art CV and ML algorithms (including face recognition).
-scikit-learn library - Machine learning in Python. Simple. Efficient. Beautiful, easy to use API.
-Numpy - NumPy is the fundamental package for scientific computing with Python.

# Alogorithm
-Capture the image of the driver from the camera.
-Send the captured image to haarcascade file for face detection.
-If the face is detected then crop the image consisting of the face only. If the driver is distracted then a face might not be detected, so play the buzzer.
-Send the face image to haarcascade file for eye detection.
-If the eyes are detected then crop only the eyes and extract the left and right eye from that image. If both eyes are not found, then the driver is looking sideways, so sound the buzzer.
-The cropped eye images are sent to the hough transformations for detecting pupils, which will determine whether they are open or closed.
-If they are found to be closed for five continuous frames, then the driver should be alerted by playing the buzzer.

# Testing and Results in Real-World Scenario:
The tests were conducted in various conditions including:

Different lighting conditions.
Drivers posture and position of the automobile drivers face.
Drivers with spectacles.
