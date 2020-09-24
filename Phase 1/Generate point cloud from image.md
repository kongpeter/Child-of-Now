# Generate Point Cloud in Matlab

## Use Computer Vision Toolbox

The following codes show how to generate point cloud based on the given depth images. 

```matlab
[xyzPoints,flippedDepthImage] = depthToPointCloud(depthImage,depthDevice)
depthDevice = imaq.VideoDevice('kinect',2) % Connect with kinect
```

If you want to use `depthToPointCloud` function, you have to connect with a kinect device. because it assumes that the depth map came from the Kinect, and it uses Kinect's calibration parameters to get the 3D coordinates. However, due to COVID-19, we cannot go to campus, which means we don't have a kinect device. Thus, this function is useless for us.


## Stereo Camera Calibrator App

You can use the `Stereo Camera Calibrator` app to calibrate a stereo camera, which you can then use to recover depth from images. A stereo system consists of two cameras: camera 1 and camera 2. The app can either estimate or import the parameters of individual cameras. The app also calculates the position and orientation of camera 2, relative to camera 1.

The `Stereo Camera Calibrato`r app produces an object containing the stereo camera parameters. You can use this object to

- Rectify stereo images using the `rectifyStereoImages` function.
- Reconstruct the 3-D scene using the `reconstructScene` function.
- Compute 3-D locations corresponding to matching pairs of image points using the `triangulate` function.