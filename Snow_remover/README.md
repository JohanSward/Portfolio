## The snow remover algorithm
Me and my friend were driving home a cold and snowy December evening after working on a computer vision project in Helsingborg in Sweden. We were brainstorming ideas how to use a very interesting result we hade seen in a recently published paper. As the snowing intensified, we started to talk about if it is possible to remove the effect of snow in a video, e.g., if you have surveillence camera overlooking a parking lot is it possible to filter out the snowing so that the footage looks like it is without any snowing at all? When I got home I asked my friend to record his back yard when it was snowing using his go-pro. Here is a sample of the images that was recorded. 

[Image]

The most straight forward way to solve this problem would be to have an already clean image to use as the ground truth. In this way it would be rather easy to use as input the images with snowing and train the network to remove the snow by comparing it to the clean image. However, if this is going to work in the parking lot example, we will not have a clean image, and even if we had it would not be correct if any of the cars in the parking lot would drive off or arrive. 

To address this problem, I took inspiration from [this paper](https://arxiv.org/pdf/1803.04189.pdf) and in my case means that I can train the network using only images where there is snowing. So if I have 10 images, each containging snowing, I may train the network by letting each of the 10 images be the ground truth an let the other nine images constitute the training set, which means that the 10 images will produce 90 input-output pairs. This works since each images will not (at least with very small probability) have the snow corrupting the same part of the image. Also, this means that one can train the network with only a few images, which in turn means that one can update the network as soon as the background image is changing, e.g., when a new car arrives at the parking lot. 

These are the results from the network:

[image]

This is the network I used:

[image]

An easier solution to the problem is to use a median filter in the temporal direction. If we stack the images from the video, we may use look at each pixel and take the median over M images seperated by $\delta t$ miliseconds. These are the results

[image]
