# How I have calculated the Mean IOU
intersection = np.logical_and(target, prediction)<br>
union = np.logical_or(target, prediction)<br>
iou_score = np.sum(intersection) / np.sum(union)
