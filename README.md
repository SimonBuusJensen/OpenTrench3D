# OpenTrench3D: A Photogrammetric 3D Point Cloud Dataset for Semantic Segmentation of Underground Utilities
[**[Paper]**](https://arxiv.org/abs/2404.07711) [**[Download]**](#download) [**[Results]**](#results) [**[Quick Start]**](#quickstart)

![Group 69](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/08534599-0b4a-4e17-88ee-7b9bacf99d6d)

The official repository of the OpenTrench3D dataset.
Identifying and classifying underground utilities is a task of growing importance for efficient and effective urban planning and infrastructure maintenance. 
We present OpenTrench3D, a novel and comprehensive 3D Semantic Segmentation point cloud dataset designed for advancing research and development in the underground utility domain. 

# News
- 💥 Apr, 2024: OpenTrench3D accepted for CVPRW - [1st Workshop on Urban Scene Modeling](https://usm3d.github.io/)

# Dataset:
We introduce **OpenTrench3D**, the first publicly available point cloud dataset of underground utilities from open trenches. 
It features **310 fully annotated point clouds** consisting of a total of **528 million points** categorised into **5 unique classes** (see description [**Classes**](#classes)).
OpenTrench3D consists of photogrammetrically derived 3D point clouds capturing detailed scenes of open trenches, revealing underground utilities.

## Overview
The dataset consists of 310 point clouds with a total of ~528 million points collected across 7 distinct areas, which include 5 water project areas and 2 district heating project areas:
![dataset-overview](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/9bd90aa7-e170-4e96-a3c2-7d192d116acc)

## Classes:
OpenTrench3D features 5 classes following a utility owner-centric classification scheme: 
- **Main Utility** (id: 0): Newly installed utilities, which is the main utility of interest for surveying and mapping. In our dataset, this class is representing two distinct types of utilities: water and district heating.
- **Other Utility** (id: 1): Existing utilities uncovered during excavation belonging to other utility owners.
- **Trench** (id: 2): The surrounding open excavation pit where the utilities are laid.
- **Inactive Utility** (id: 3): Out-of-service utilities belonging to the utility owner.
- **Misc** (id: 4): Miscellaneous trench items such as pipe-like objects, work equipment and left-over cut pipe segments **(ignored in training/evaluation)**

![gew](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/b56bf874-0142-4a74-867c-886037431aec)

# Quick Start


# Results
## 5-fold cross-validation on the water areas
We conduct a 5-fold cross-validation on the water areas and in two rounds. Initially, we include the Inactive Utility class during training and evaluation and subsequently, we ignore it. The results are shown in below table:

![results-5-fold-cross-validation](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/667567d3-c7a0-474f-bafa-6ac137f5d375)

## Fine-tuning evaluation on heating areas
We conduct We conduct a fine-tuning evaluation on the heating areas in the following way: 
1. pre-train model weights on Water Area 1-4.
2. Fine-tune model weights on 1, 5, 10, 20 and all (29) samples from Heating Area 1.
3. Evaluate the fine-tuned models on Heating Area 2.
The results are shown in the below figure:

<img width="8873" alt="results-fine-tuning-evaluation" src="https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/07a3b7d6-d40a-4d72-9a44-29141b208fdf">

### Qualitative results
Here we compare the inference of a PointNeXt model trained on Water Area 1-4, a PointNeXt model trained on 1 and 10 samples from Heat Area 1 and a pre-trained and fine-tuned PointNeXt models fine-tuned on 1 and 10 samples:

![qualitative-results](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/022c34f1-7543-413e-837d-5253ef798b2d)

# Capturing Method:
The OpenTrench3D dataset is gathered using close-range photogrammetry captured using video recordings from everyday smartphones.
The procedure is divided into three straightforward steps:
1. Apply markings around the open trench, used as Ground Control Points (GCP), possibly using a spray marker.
2. Carefully video record the trench from various angles, ensuring the camera is aimed down towards the utilities visible in the trench.
3. Upload the captured video through the [SmartSurvey](https://it34.com/en/services/smartsurvey-app-en/) application. Subsequently, the video data is sent to a server for processing into a 3D point cloud.

# Download:
OpenTrench3D comprises 310 point clouds in .ply file format with the following attributes: [X, Y, Z, R, G, B, C]
- X, Y, Z: x-, y- and z-coordinates in meters
- R, G, B: Red, Green and Blue color channel (0-255)
- C: Class id (0, 1, 2, 3 or 4)

**OpenTrench3D on Kaggle**: [link](https://www.kaggle.com/datasets/hestogpony/opentrench3d/data?select=Examples)

**Direct Download link (~6GB compressed and ~22.5GB when uncompressed)**: [link](https://www.kaggle.com/datasets/hestogpony/opentrench3d/download?datasetVersionNumber=1)

#  Acknowledgement
We thank the students who assisted in data annotation, and to [IT34](https://it34.com/en/), [Ambolt AI](https://ambolt.io/en/), Innovation Fund Denmark, DigitalLead and [AI Denmark](https://aidenmark.dk/) for their support and funding. 
Special thanks to Kalundborg and Novafos Utility Company for granting data access.

# License:
OpenTrench3D is distributed under the [CC BY-NC 4.0 License](https://creativecommons.org/licenses/by-nc/4.0/)
