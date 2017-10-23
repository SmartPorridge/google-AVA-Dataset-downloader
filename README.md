**AVA Atomic Visual Action Dataset**

The AVA dataset densely annotates 80 atomic visual actions in 57.6k movie clips with actions localized in space and time, resulting in 210k action labels with multiple labels per human occurring frequently. The main differences with existing video datasets are: 

1. the definition of atomic visual actions, which avoids collecting data for each and every complex action; 
2. precise spatio-temporal annotations with possibly multiple annotations for each human; 
3. the use of diverse, realistic video material (movies). 

**More details about the dataset and initial experiments can be found in this** [arXiv paper](https://arxiv.org/abs/1705.08421 "悬停显示"). 
  
The AVA dataset contains 192 videos split into 154 training and 38 test videos. Each video has 15 minutes annotated in 3 second intervals, resulting in 300 annotated segments. These annotations are specified by two CSV files: [ava_train_v1.0.csv](https://research.google.com/ava/download/ava_train_v1.0.csv "悬停显示") and [ava_test_v1.0.csv](https://research.google.com/ava/download/ava_test_v1.0.csv "悬停显示"). 

Each row contains an annotation for one person performing an action in an interval, where that annotation is associated with the middle frame. Different persons and multiple action labels are described in separate rows. 

The Youtube video IDs (train split) is [ava_ytids_train_v1.0.txt](./ava_ytids_train_v1.0.txt)
The Youtube video IDs (test split) is [ava_ytids_test_v1.0.txt](./ava_ytids_test_v1.0.txt)

**The format of a row is the following: video_id, middle_frame_timestamp, person_box, action_id**
1. video_id: YouTube identifier
2. middle_frame_timestamp: in seconds from the start of the YouTube.
3. person_box: top-left (x1, y1) and bottom-right (x2,y2) normalized with respect to frame size, where (0.0, 0.0) corresponds to the top left, and (1.0, 1.0) corresponds to bottom right.
4. action_id: identifier of an action class, see [ava_action_list_v1.0.pbtxt](https://research.google.com/ava/download/ava_action_list_v1.0.pbtxt "悬停显示")

The dataset is made available by Google Inc. under a [Creative Commons Attribution 4.0 International (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/ "悬停显示").
