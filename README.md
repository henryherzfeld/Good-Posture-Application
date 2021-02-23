
# Good Posture Application


#### An application designed to track posture from a camera in real time and provide feedback on a user's posture.

Developed at the [Machine Perception and Cognitive Robotics LAB (MPCR)](https://mpcrlab.com/) at FAU, a team of students ([Paul Morris](https://github.com/pmorris2012), [Henry Herzfeld](https://github.com/henryherzfeld), [Michael Keller](https://github.com/michaelkeller21)) lead efforts to develop an application to track posture in real-time. The first implementation made use of the [Microsoft Kinect SDK](https://developer.microsoft.com/en-us/windows/kinect/), providing a scoring for a particular user's posture. 

<p align="center">
<img width="400" alt="kinect" src="https://michaelkeller21.github.io/images/kinect%20demo.jpg">
</p>


However support for Kinect 2.0 SDK is diminishing, and the score provided to the user wasn't granular enough. To improve on this model [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose), an ML system from CMU to produce keypoint estimation of human pose on images was selected, such that its output from single frames could be fed into a neural network to perform classification on posture.



<p align="center">
<img width="150" alt="kinect" src="https://michaelkeller21.github.io/images/openpose.png">
<br>An example of a skeleton with just 24 keypoints
</p>

<br>
<p align="center">
<img width="400" alt="alt" src="https://michaelkeller21.github.io/images/Classifier%20sample.jpg">
<br>POC Dataset
</p>
<br>
After producing a proof-of-concept and hand-labeling thousands of frames, our fully-connected neural network classifier was able to produce satisfactory accuracy for our small dataset:
<br>                                                                                                          
<p align="center">
<img width="400" alt="alt" src="https://michaelkeller21.github.io/images/Classifier%20Composition.jpg">
<img width="400" alt="alt" src="https://michaelkeller21.github.io/images/Classifier%20results.jpg">
</p>

 Future work includes using a stereoscopic camera to augment our dataset and replacing the fully-connected classifier.
