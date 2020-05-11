# cvdl
3D pose estimation and object instance recognition

The project is created in the context of TUM course [Tracking and Detection for Computer Vision](http://campar.in.tum.de/Chair/TeachingWs19TDCV).

The idea is to use triplets (anchor, puller and pusher objects) to estimate 3D pose and recognize the object instance at the same time. 
The triplet loss in combination with the pairwise loss are used. Please refer to [P. Wohlhart and V. Lepetit. Learning descriptors for object recognition and 3d pose estimation](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Wohlhart_Learning_Descriptors_for_2015_CVPR_paper.pdf).
for more details.

The overall pipeline is the following:
![alt text](https://github.com/DianaDI/cvdl/blob/master/src/img/Architecture.JPG)

The network output is a 16-dim descriptor vector. After perfroming t-SNE on them for test test, 
we could see the following visualisation in 3D for 5 object classes:

![alt text](https://github.com/DianaDI/cvdl/blob/master/src/tsne.png)

The accuracy of object instance recognition is 91% for current implementation.

Pose estimation accuracy can be seen on the histogram (with horisontal axis defining angles' degrees): 

![alt text](https://github.com/DianaDI/cvdl/blob/master/src/hist.png)
