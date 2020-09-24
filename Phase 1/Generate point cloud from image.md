# Generate Point Cloud in Matlab

## Use Computer Vision Toolbox

The following codes show how to generate point cloud based on the given depth images. 

```matlab
[xyzPoints,flippedDepthImage] = depthToPointCloud(depthImage,depthDevice)
depthDevice = imaq.VideoDevice('kinect',2) % Connect with kinect
```

If you want to use `depthToPointCloud` function, you have to connect with a kinect device. because it assumes that the depth map came from the Kinect, and it uses Kinect's calibration parameters to get the 3D coordinates. However, due to COVID-19, we cannot go to campus, which means we don't have a kinect device. Thus, this function is useless for us.