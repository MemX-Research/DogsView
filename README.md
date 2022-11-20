# DogsView

This repository contains the DogsView dataset described in the paper "Unveiling Causal Attention in Dogs’ Eyes with Smart Eyewear".

<!-- If you use this dataset in your work, please cite our paper:
```
citation goes here
``` -->

## Dataset
Data for the DogsView dataset was collected in a controlled experimental setting and in an open outdoor setting. All videos including eye videos and world videos were collected under 1920x1080 resolution, 30fps, infrared recording conditions and 1920x1088 resolution, 30fps recording conditions, respectively. Currently we have 57 pairs of videos and they are divided. We divide the video of the experimental environment into 4 cases according to the experimental content, and each case contains the data of 5 dogs; the open scene is divided into 3 fields, which are from the same dog. The detailed construction of the dataset is given in Chapter 4 of the paper.

The dataset can be downloaded [here](https://www.dropbox.com/sh/gbuqcbx4rfm9fhv/AAAked71G0hePdaXYq9YBLBka?dl=0).

## Data Format
All videos are divided into in-lab part and field study part.In-lab part videos are divided into 4 cases, each one is divided into 5 dogs, they have different numbers of folders.Field study videos come from the same dog and are divided into three cases: safeguarding, dog cognition and animal-computer interaction, each case has different numbers of folders.Every single folder contains three videos and two files.

**eye video.mp4**: This video contains eye images stored in MP4 format which is recorded under 1920*1080 resolution, 30fps, infrared recording conditions.

**world video.mp4**: This video contains world images seen from the dog's point of view, which is stored in MP4 format which is recorded under 1920*1088 resolution, 30fps recording conditions.

**gazed world video.mp4**: This video is a world video marked with gaze positions locations.

**gaze_positions.csv**:This CSV file contains the eye tracking result of corresponding eye video.

It contains the following attributes:

`world_index`: The frame number.

`norm_pos_x` and `norm_pos_y`: The gaze position in the space of the scene frame. The are floating point numbers and origin 0,0 at the bottom left and 1,1 at the top right.

**auto_annotation.csv**:This CSV file contains the annotation which is automatically annotated by our proposed model of every attentive session in a video 

`attentive session start frame`: The frame number of the start frame of an attentive session.

`attentive session end frame`: The frame number of the end frame of an attentive session.

`dog behavior`: The behavior finally made by the dog in this clip.

`human action`: The most important human action which causes the corresponding dog behavior.



