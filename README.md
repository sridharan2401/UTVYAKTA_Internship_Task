# Image Registration Using OpenCV
## Objective:
1.	From the sample/test images provided, you have to identify the features and align the images according to the original.
2.	The test images may be scaled, offset or rotated or a combination of these.
3.	Ideally, the test image should be aligned to the original image in the same orientation and scale.
4.	You may use any language of your preference to accomplish this task.	

## Approach – Image Registration using OpenCV | Python
	This task is accomplished by using Image Registration and Homography using OpenCV.
	The language which is used for the completion of task is Python 3.0. 
  
## Image Registration: 
	Image registration is a digital image processing technique which helps in align different images of the same scene. 
	For instance, sample/test images which is rotated or scaled or offset or combination of all these can align according
	to the original image.
  
## Image Registration Process:
1.	Converted both test image and original image to grayscale.
2.	ORB (Oriented FAST and Rotated BRIEF) is used to detect and compute keypoints and its associated descriptors of test image and original image.
3.	Match features from the image to be aligned i.e. test image, to the original or reference image and store the coordinates of the corresponding keypoints. Keypoints are simply the selected few points which are used to compute the transform, and descriptors are histograms of the image gradients to characterize the appearance of a keypoint.
4.	Brute Force Matcher with Hamming distance as a measure mode is used for matching keypoints of both test image and reference image.	
5.	Sorted the matches to pick the top matches and remove the noisy matches. Top 85% matches are selected.
6.	Homography is obtained for the keypoints of both images. RANSAC	(Random sample Consensus) algorithm is used to avoid outliers.
7.	Apply homography transform the test image according to the original image.
