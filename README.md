# Structure from Motion (SfM)

This project is an implementation of SfM: to reconstruct a 3D scene and simultaneously obtain the camera poses of a monocular camera w.r.t. the given scene. The ain is to create entire rigid structure from a set of images with different view points (or equivalently a camera in motion).

### Approach 

The steps followed for creating the SfM algorithm are:
* Feature Matching and Outlier rejection using RANSAC
* Estimating Fundamental Matrix
* Estimating Essential Matrix from Fundamental Matrix
* Estimate Camera Pose from Essential Matrix
* Check for Cheirality Condition using Triangulation
* Perspective-n-Point
* Bundle Adjustment

The implementation is included in Code and the detailed explaination for each step is explained in the report attached.

### Results
Given  a set of 5 images of Unity Hall at WPI:
<p align="center">
  <img src="InputData\1.png" alt="input" width="100"/>
  <img src="InputData\2.png" alt="input" width="100"/>
  <img src="InputData\3.png" alt="input" width="100"/>
  <img src="InputData\4.png" alt="input" width="100"/>
  <img src="InputData\5.png" alt="input" width="100"/>
</p>

The end result we obtained was:
<p align="center">
  <img src="IntermediateOutputImages\All.png" alt="output" width="500"/>
</p>

Where we can see the 5 estimated camera poses and the 2D point cloud of the building from a top view. 
The results for each steps are included in the IntermediateOutputImages and the report.

### References
1. https://rbe549.github.io/spring2023/proj/p2/
