# Silhouette-Using-Sementic-Segmentation
Please visit PDF For better understading
##Architecture
![Screenshot_20190313-002300-4](https://user-images.githubusercontent.com/40520042/64706513-34c2a100-d4cf-11e9-9482-e1f968ba9acc.jpg)
![oie_ZWVBh1hmQ4wM](https://user-images.githubusercontent.com/40520042/64707427-9afbf380-d4d0-11e9-8434-a0f3604d2a25.jpg)

# INTRODUCTION
Image segmentation is a computer vision task in which we label specific regions of an image according to what's being shown. <br/>
"What's in this image, and where in the image is it located?"<br/>
More specifically, the goal of semantic image segmentation is to label each pixel of an image with a corresponding class of what is being represented. Because we're predicting for every pixel in the image, this task is commonly referred to as dense prediction.
<br/><br/>
One important thing to note is that we're not separating instances of the same class; we only care about the category of each pixel. In other words, if you have two objects of the same category in your input image, the segmentation map does not inherently distinguish these as separate objects. There exists a different class of models, known as instance segmentation models, which do distinguish between separate objects of the same class.

# OBJECTIVES
### Representing the task
Simply, our goal is to take either a RGB color image (height×width×3height×width×3) or a grayscale image (height×width×1height×width×1) and output a segmentation map where each pixel contains a class label represented as an integer (height×width×1height×width×1).
<br/><br/>
<i>Note</i>: For visual clarity, I've labeled a low-resolution prediction map. In reality, the segmentation label resolution should match the original input's resolution.
Similar to how we treat standard categorical values, we'll create our target by one-hot encoding the class labels - essentially creating an output channel for each of the possible classes.
<br><br>
A prediction can be collapsed into a segmentation map by taking the argmax of each depth-wise pixel vector.
We can easily inspect a target by overlaying it onto the observation.
<b> When we overlay a single channel of our target (or prediction), we refer to this as a mask which illuminates the regions of an image where a specific class is present.</b>











