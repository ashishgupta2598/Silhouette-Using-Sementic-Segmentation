# How I have calculated the Mean IOU
Mean IOU on Synthetic Data(ShapNet) comes out to be 0.897 and on Pascal Voc 2012 is
0.731 .
### Just Run it over a class.....and a for loop for Mean of batch of images and find it 
intersection = np.logical_and(target, prediction)<br>
union = np.logical_or(target, prediction)<br>
iou_score = np.sum(intersection) / np.sum(union)
