# OpenTrench3D: A 3D Point Cloud Dataset of Open Trenches for Semantic Segmentation of Underground Utilities
[**[Paper]**]() [**[Download]**](#download) [**[Results]**](#results)

![Group 69](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/08534599-0b4a-4e17-88ee-7b9bacf99d6d)

The official repository of the OpenTrench3D dataset.
Identifying and classifying underground utilities is a task of growing importance for efficient and effective urban planning and infrastructure maintenance. 
We present OpenTrench3D, a novel and comprehensive 3D Semantic Segmentation point cloud dataset designed for advancing the research and development in the urban underground utilities domain. 

# Dataset:
OpenTrench3D comprises photogrammetrically derived 3D point clouds capturing detailed scenes of open trenches, revealing underground utilities.

## Overview:
The dataset consists of 310 point clouds collected across 7 distinct areas, which include 5 water utility areas collected in Copenhagen, Denmark and 2 district heating utility areas, collected in Kalundborg, Denmark.

![Group 68 (1)](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/8a90a225-10b5-469a-8fed-47a485d5173e)

## Classes:
OpenTrench3D features 4 classes: 
- Main Utility Pipe (id: 0)
- Other Utility Pipe (id: 1)
- Trench (id: 2)
- Ignored Objects (ignored in training/evaluation) (id: 3)

![Group 67](https://github.com/SimonBuusJensen/OpenTrench3D/assets/32246995/23732797-5cb0-4531-8fc3-0bacaaaef2e6)

## Attributes:
The format of a points cloud is the following: [X, Y, Z, R, G, B, C]
- X: x-coordinates (meters)
- Y: y-coordinates (meters)
- Z: z-coordinates (meters)
- R: Red color channel (0-255)
- G: Green color channel (0-255)
- B: Blue color channel (0-255)
- C: Class id (0, 1, 2 or 3)

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
