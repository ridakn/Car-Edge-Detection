# Car-Edge-Detection

<p align = "justify">
A computer vision project to use edge detection to detect the edges in car images in order to remove the background and just get the car. </p>

## Introduction

<p align = "justify">
Since the car images used for training can have many unwanted attributes in the images like reflections on the car of light or other objects, this can reduce accuracy as these can be also considered as damage by the network. One technique we tried to solve this issue was to use edge detection for the images. Edge detection is a multistage algorithm which scans the images and outputs the edges based on some input values we give which are thresholds used in the algorithm. </p>

In this example, the minimum and maximum values are 255 for both.

<img width="973" alt="Screen Shot 2021-07-04 at 12 43 15 AM" src="https://user-images.githubusercontent.com/32781544/124366494-28a85600-dc05-11eb-8af9-eb0d88a8b0dd.png">

## Blurring

<p align = "justify">
As can be seen in the above example, the edge detection algorithm might be able to remove the unwanted reflection, however, it is also removing the edges of the damage which isn't what we want. Therefore, we try blurring techniques before running edge detection on the images. Image blurring is an image processing technique that performs a convolution operation between the given image and a low-pass filter kernel. It reduces the edge content and makes the transition from one colour to another smoother; therefore, it's useful for reducing noise in images. </p>

An example of Gaussian Blurring and edge detection.

<img width="971" alt="Screen Shot 2021-07-04 at 12 44 08 AM" src="https://user-images.githubusercontent.com/32781544/124366502-3067fa80-dc05-11eb-8f7d-b87e135d00b1.png">

<p align = "justify">
The following examples showcase that our technique of first blurring the original image then using edge detection works since it removes noise while keeping intact the edges of the damage which is our main concern. </p>

<img width="680" alt="Screen Shot 2021-07-04 at 12 44 46 AM" src="https://user-images.githubusercontent.com/32781544/124366512-3958cc00-dc05-11eb-80a2-36efb61f894f.png">

<p align = "justify">
This technique worked on most of the images in our training set; however, for a few images it removed the damaged area as well. The below examples showcase such images and it can be seen it is when the damage is a similar colour to the car and hence not as starkly different; therefore, the damage is also removed and considered an edge. </p>

<img width="713" alt="Screen Shot 2021-07-04 at 12 45 26 AM" src="https://user-images.githubusercontent.com/32781544/124366515-41187080-dc05-11eb-9c34-70c81df1816a.png">

## References

1.	https://www.analyticsvidhya.com/blog/2018/07/building-mask-r-cnn-model-detecting-damage-cars-python/
2.	https://www.robots.ox.ac.uk/~vgg/software/via/via-1.0.6.html
3.	https://docs.opencv.org/trunk/da/d22/tutorial_py_canny.html
4.	https://www.analyticsvidhya.com/blog/2018/07/building-mask-r-cnn-model-detecting-damage-cars-python/








