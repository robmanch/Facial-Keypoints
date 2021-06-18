# Facial-Keypoints
## Introduction
Facial landmark detection is the task of detecting key landmarks on the face. It can be use in various applications such as detection of face part and then changing it with other things etc.
## Dataset Description
Each predicted keypoint is specified by an (x,y) real-valued pair in the space of pixel indices. There are 15 keypoints, which represent the following elements of the face:

left_eye_center, right_eye_center, left_eye_inner_corner, left_eye_outer_corner, right_eye_inner_corner, right_eye_outer_corner, left_eyebrow_inner_end, left_eyebrow_outer_end, right_eyebrow_inner_end, right_eyebrow_outer_end, nose_tip, mouth_left_corner, mouth_right_corner, mouth_center_top_lip, mouth_center_bottom_lip

Left and right here refers to the point of view of the subject.

In some examples, some of the target keypoint positions are misssing (encoded as missing entries in the csv, i.e., with nothing between two commas).

The input image is given in the last field of the data files, and consists of a list of pixels (ordered by row), as integers in (0,255). The images are 96x96 pixels.

Data link: https://www.kaggle.com/c/facial-keypoints-detection/data?select=test.zip

## Results/Discussion
- CNN, which is usually used for classification, can be used to predict the facial keypoints.
- Here CNN works as a regression model, hence in the last layer linear activation is used, and to predict cordinates as close as actual, we have used mean squared error loss function.
- Model can do even better if the missing values are lesser.
