### Training set
The training set contains **1680 videos along with their annotations**. We provide two files for the video ids and annotations.

The video ids from the YouTube website are in
```
train/train_id
```
with one video id per line. Videos can be accessed by
```
https://www.youtube.com/watch?v=${video_id}
```
For example, you can access the video 'z4eIfjpRPVo' by
```
https://www.youtube.com/watch?v=z4eIfjpRPVo
```

The annotations of steps are in
```
train/steps.json
```
with annotations of one video per line. The annotation record for each video contains

Attribute | Meaning
---|---
video_id | YouTube video id
title     | video title
step     | step annotation

For each step, we provide annotations for temporal boundaries, facial areas and natural language descriptions.

Attribute | Meaning
--- | ---
key | step index
startime | step start time
endtime  | step end time
area     | a list of related facial areas
caption  | natural language descriptions of the step

### Task
#### Facial Image Ordering
The facial image ordering task is to sort a series of shuffled facial images into the right order according to the ordered step captions.
We provide the question file and image folder for this task. 


There are 1200 questions in the question file
```
task/image_ordering/image_ordering_validation.json
```
with one question per line.
Attribute | Meaning
--- | ---
question_id | id of the question
step_caption  | a list of ordered step descriptions for the video
candidate_answer    | 4 candidate answers of the facial image order
groundtruth  | right order of the 5 facial images 

You can download the validation set for image ordering task from
[Google Drive](https://drive.google.com/open?id=1-Wb5gbIIV6H75Pk1NjYdKATYZ1uitI99) and save it in
```
task/image_ordering/
```
Each folder is corresponding to a question named by the question id.


#### Step Ordering
The step ordering task evaluates the capability of sorting a series of step captions into the right order according to the video. We provide two files for video ids and questions.

The video ids from the YouTube website are in
```
train/train_id
```
with one video id per line.

The question file is 
```
task/step_ordering/step_ordering_validation.json
```
It contains 1800 questions with one question per line.

Attribute | Meaning
--- | ---
video_id | id of video
step_caption | 5 step descriptions chosen randomly from the video
candidate_answer | 4 candidate answers of the step order
groundtruth | right order of the steps
