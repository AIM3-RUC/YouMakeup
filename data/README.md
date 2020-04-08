We introduce the dataset for the **YouMakeupVQA challenge**


### Training and Validation set

#### Training Set
The training set of the two ordering tasks contains **1680 videos along with their annotations**. We provide two files for the video ids and annotations.

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
train/train_steps.json
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



#### Validation Set
To help the participants develop models, we also provide all videos and their captions in the validation set. The video id is in 
```
valid/valid_id
```
and the step captions are in
```
valid/valid_steps.json
```

### Task
#### Facial Image Ordering
The facial image ordering task is to sort a series of shuffled facial images into the right order according to the ordered step captions.
We provide the question file and image folder for this task. 

##### Validation Set
There are 1200 questions in the validation set generated from 280 videos. The questions are in 
```
task/image_ordering/valid/image_ordering_validation.json
```
with one question per line.
Attribute | Meaning
--- | ---
question_id | id of the question
step_caption  | a list of ordered step descriptions for the video
candidate_answer    | 4 candidate answers of the facial image order
groundtruth  | right order of the 5 facial images 

The images for questions can be download and placed in
```
task/image_ordering/valid/images/
```
Each folder is corresponding to a question named by the question id.

##### Test Set
There are 1500 questions generated from 420 videos in the test set. The test set share the same structure with validation set. The questions are in
```
task/image_ordering/test/image_ordering_test.json
```
and the images can be downloaded and placed in
```
task/image_ordering/test/images
```

The method to download images is in the last section.


#### Step Ordering
The step ordering task evaluates the capability of sorting a series of step captions into the right order according to the video. We provide two files for video ids and questions.

##### Validation Set
The validation set contains 1800 questions generated from 280 videos.
The video ids from the YouTube website are in
```
task/step_ordering/dev/valid_vid
```
with one video id per line.

The question file is 
```
task/step_ordering/valid/step_ordering_validation.json
```
 with one question per line.
 
Attribute | Meaning
--- | ---
video_id | id of video
step_caption | 5 step descriptions chosen randomly from the video
candidate_answer | 4 candidate answers of the step order
groundtruth | right order of the steps


##### Test Set
There are 3200 questions generated from 420 videos. The video id is in
```
task/step_ordering/test/validation_vid
```

The question file is 
```
task/step_ordering/test/step_ordering_test.json
```


### Data Download
The data license form should be signed before accessing the data. Please sign the form and send it to youmakeupvqa@163.com and we will provide the link for data download.
