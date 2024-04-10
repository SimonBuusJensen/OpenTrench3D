# OpenTrench3D: A Photogrammetric 3D Point Cloud Dataset for Semantic Segmentation of Underground Utilities
[**[Paper]**]() [**[Download]**](#download) [**[Results]**](#results)

![Group 69](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/08534599-0b4a-4e17-88ee-7b9bacf99d6d)

The official repository of the OpenTrench3D dataset.
Identifying and classifying underground utilities is a task of growing importance for efficient and effective urban planning and infrastructure maintenance. 
We present OpenTrench3D, a novel and comprehensive 3D Semantic Segmentation point cloud dataset designed for advancing the research and development in the urban underground utilities domain. 

# Dataset:
We introduce **OpenTrench3D**, the first publicly available point cloud dataset of underground utilities from open trenches. 
It features 310 fully annotated point clouds consisting of a total of 528 million points categorised into 5 unique classes (see description [**Classes**](#classes)).
OpenTrench3D comprises photogrammetrically derived 3D point clouds capturing detailed scenes of open trenches, revealing underground utilities.

## Overview
The dataset consists of 310 point clouds collected across 7 distinct areas, which include 5 water project areas and 2 district heating project areas:
![dataset-overview](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/9bd90aa7-e170-4e96-a3c2-7d192d116acc)

## Classes:
OpenTrench3D features 5 classes: 
- **Main Utility** (id: 0): Newly installed utilities, which is the main utility of interest for surveying and mapping. In our dataset, this class is representing two distinct types of utilities: water and district heating.
- **Other Utility** (id: 1): Existing utilities uncovered during excavation belonging to other utility owners.
- **Trench** (id: 2): The surrounding open excavation pit where the utilities are laid.
- **Inactive Utility** (id: 3): Out-of-service utilities belonging to the utility owner.
- **Misc** (id: 4): Miscellaneous trench items such as pipe-like objects, work equipment and left-over cut pipe segments **(ignored in training/evaluation)**

![gew](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/b56bf874-0142-4a74-867c-886037431aec)

## Attributes:
The format of a points cloud is the following: [X, Y, Z, R, G, B, C]
- X: x-coordinates (meters)
- Y: y-coordinates (meters)
- Z: z-coordinates (meters)
- R: Red color channel (0-255)
- G: Green color channel (0-255)
- B: Blue color channel (0-255)
- C: Class id (0, 1, 2, 3 or 4) 

## Statistics
OpenTrench3D comprises ~498 million points. The below figure, displays the number of point clouds in each area and the number of points per class and in total (stated in thousands).

![image](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/7254c8a7-567c-4a72-95cf-faad7af4b446)


# Capturing Method:
TODO

# Download:
OpenTrench3D comprises 310 point clouds in .ply file format:

**OpenTrench3D on Kaggle**: [link](https://www.kaggle.com/datasets/hestogpony/opentrench3d/data?select=Examples)

**Direct Download link (~6GB compressed and ~22.5GB when uncompressed)**: [link](https://www.kaggle.com/datasets/hestogpony/opentrench3d/download?datasetVersionNumber=1)


# Results

# License:
OpenTrench3D is distributed under the [CC BY-NC 4.0 License](https://creativecommons.org/licenses/by-nc/4.0/)
