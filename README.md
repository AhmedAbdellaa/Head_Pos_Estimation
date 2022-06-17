# Head Pose Estimation
![](https://github.com/AhmedAbdellaa/Head_Pos_Estimation/blob/master/result/2177168298_1.jpg?raw=true)
## Overview
Create a head pose estimator that can tell where the head is facing in degrees using Python and OpenCV 

## Technologies
Python,mediapipe,dlib , matplot, pandas, Numpy
Sklearn, open-cv



#### collect data
dlib : each image had mat file containing the location of the face point and pos label (pitch, yaw,roll)
so I collect points data, labels, and image names and store them in CSV file
mediapipe : instead of getting points from mat file I loop throw each image with only one face in it and could be recognized by mediapipe
#### preprosessing
-there is some image with label very odd from other images(outlier) dropped it 
-recenter and rescale 468 points
#### models
best model of (SVR,random-forest,xgboost,voting): is SVR with total r2score for three labels  = 82%

#### Notes
with dlib: model achieve very good accuracy at pos estimation put it was bad at locating face in several pos
with mediapipe : model achieve not bad accuracy at pos estimation put it was very good at locating face in image
