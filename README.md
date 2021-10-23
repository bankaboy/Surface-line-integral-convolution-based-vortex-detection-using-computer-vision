# Surface line integral convolution-based vortex detection using computer vision
**Version 1.0.0**

This is your README. READMEs are where you can communicate what your project is and how to use it.

We proposed a new approach using convolutional neural networks to detect flow structures directly from streamline plots, using the line integral convolution method. We show that our computer vision-based approach is able to reduce the number of false positives and negatives entirely.
Write your name on line 6, save it, and then head back to GitHub Desktop.

## Requirements
The Vortex Detection using Computer Vision based on YOLOv3 works only on Python 3.7 and superior. The following library are installed via pip in order to run the model:
*	Torchvision
*	PyTorch/1.6.0-
*	Albumentations
*	config
*	NumPy
*	Matplotlib
*	Tensorboard

## Tensorboard
Track training progress in:
1. Mean Average Precision (mAP value)
2. Loss Function
3. Class accuracy - Object accuracy - No Object accuracy

For mAP and Loss function:
`tensorboard --logdir=logs`

For correct_class, correct_obj, and correct_Noobj:
`tensorboard --logdir=runs`

## Download pretrained weights


## Training Datasets
We extract a total of 100 images from the symmetry plane of “Taylor Green Vortex problem flow is simulated using Large Eddy Simulation (LES) at Re=1600” in the x-direction and label vortices on these 100 images that we process with ParaView through python scripting to generate 100 images using line integral convolution-based streamline plots.

## Test Datasets
We select two additional images from the symmetry plane in the x-direction, which are not part of the training datasets, and use that for testing the accuracy of our vortex detection framework based on computer vision. The two images are shown in Figure below, where test image 1, on the left-hand side, contains 16 vortices and test image 2, on the right-hand side, contains 24 vortices. We observe that the test images contain mostly symmetrical vortex structures along the main axes.
<table align="center" style="border: 0"> 
  <tr>
		<td><img src="images/test_image1_before_detecting.png" height="250" width="250" style="border: 0">    
    </td>
    <td><img src="images/test_image2_before_detecting.png" height="250" width="250" style="border: 0">    
    </td>

 </tr>
	<tr align="center" >
	<td><center>(a) Test image 1 with 16 vortices.</center></td>
    <td><center>(b) Test image 2 with 24 vortices.</center></td>

  </tr>
  <tr align="center">
    <td colspan="2" >Fig.1 - Test images showing vortical structures obtained with the
	    <br> line integral convolution-based streamline algorithm.</td>
  </tr>	
 </table>


## Detecting vortices through computer vision

<table align="center" style="border: 0"> 
  <tr>
		<td><img src="images/testimage1.png" height="250" width="250" style="border: 0">    
    </td>
    <td><img src="images/testimage2.png" height="250" width="250" style="border: 0">    
    </td>

 </tr>
	<tr align="center" >
	<td><center>Test image1</center></td>
    <td><center>Test image2</center></td>

  </tr>
  <tr align="center">
    <td colspan="2" >Fig.2 - The output result of test images. The red box is the predicted bounding box</td>
  </tr>	
 </table>



<table align="center" style="border: 0"> 
  <tr>
		<td><img src="images/Loss_function.png" height="280" width="570" style="border: 0">    
   
 </tr>
	<tr align="center" >
	<td><center>Fig.3 - loss values curve in the time of training epochs.</center></td>
   
  </tr>
   </table>
   
   <table align="center" style="border: 0"> 
  <tr>
		<td><img src="images/mAp_values.png" style="border: 0">    
   
 </tr>
	<tr align="center" >
	<td><center>Fig.4 - Mean Average precision curve in the time of training epochs.</center></td>
   
  </tr>
   </table>



