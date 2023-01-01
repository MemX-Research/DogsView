# DogsView

This repository contains the DogsView dataset described in the paper "Unveiling Causal Attention in Dogs’ Eyes with Smart Eyewear".

<!-- If you use this dataset in your work, please cite our paper:
```
citation goes here; add memx

``` -->

## Dataset
The DogsView dataset was collected in various open-world scenarios from five dog subjects. All videos, including eye/scene videos, have a spatial resolution of 1920x1080 and a sampling rate of 30fps. Currently, we have 63 pairs of eye/scene video clips. A detailed description of the DogsVies dataset is given in Section 4 of the paper.

The dataset can be downloaded [here](https://www.dropbox.com/sh/gbuqcbx4rfm9fhv/AAAked71G0hePdaXYq9YBLBka?dl=0).

## Data Format
The DogsView dataset has 63 folders. Each folder is named "scenario_x_dog_y_z", where x is the number of open-world scenarios, y is the number of dog subjects, and z is the repeated times for dog y in scenario x. Each folder contains three videos and two CSV files described as follows:

**eye video.mp4**: This video contains eye videos recorded under infrared recording conditions.

**world video.mp4**: This video contains scene videos from dog subjects' filed-of-view.

**gazed world video.mp4**: This video is the scene video marked with a dog subject's gaze point positions.

**gaze_positions.csv**: This CSV file contains the eye-tracking results.

It contains the following attributes:

`world_index`: The frame number of the scene video.

`norm_pos_x` and `norm_pos_y`: The gaze position in the space of the scene frame. They are floating point numbers with origin point (0,0) at the bottom left and ending point (1,1) at the top right.

**auto_annotation.csv**: This CSV file contains the annotations, which the CANINE model automatically obtains for each attentive session in a scene video. 

`attentive session start frame`: The starting frame number in an attention session.

`attentive session end frame`: The ending frame number in an attention session.

`dog behavior`: The dog subject's behavior in an attention session.

`human action`: The human subject's action (or called communicative cues) that causes the dog's responsive behaviors.



