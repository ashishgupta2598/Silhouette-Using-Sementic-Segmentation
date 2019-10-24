# How I have calculated the Mean IOU
# Just Run it over a class.....and find it 
intersection = np.logical_and(target, prediction)<br>
union = np.logical_or(target, prediction)<br>
iou_score = np.sum(intersection) / np.sum(union)
