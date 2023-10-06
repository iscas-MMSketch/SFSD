# SFSD dataset

This repository hosts the SFSD dataset. Please refer to our paper for more information: ["Stroke-based semantic segmentation for scene-level free-hand sketches"](https://link.springer.com/article/10.1007/s00371-022-02731-8). 

**Download**: [SFSD]()

## Overview

- Dataset Description
  - Dataset Summary
  - Dataset Construction Process
  - Dataset Sample
  - Dataset Structure
- Dataset Statistics and Analysis
- Citation

## Dataset Description

### Dataset Summary

Our **Scene-level Free-hand Sketch Dataset (SFSD)** has the characteristics of scene-level, completely free-hand, multi-modal, and vector storage data format. SFSD is composed of **12K** sketch-photo pairs over **40** object categories, where the sketches were completely hand-drawn and each contains 7 objects on average. In addition to the semantic segmentation addressed in this paper, SFSD can also support retrieval, generation, and other sketch-related tasks as well.

### Dataset Construction Process

The construction of SFSD involved the following three phases:

1. **Image Preparation**: The reference photos were selected from **MS COCO**. To filter the photos, we first excluded those with more than 10 objects. Then, we manually selected the photos by the following criteria: (1) The scenes are restricted to wildlife, outdoor sports, and out-of-town streets. (2) The photos have high integrity, moderate background complexity, and objects that are relatively easy to identify and draw.
2. **Sketch Collection**: We recruited 40 participants with different levels of painting skill. In order to standardize the process of drawing, we established an online sketching system to collect stroke sequences. We placed the reference image on the left side of the drawing board and asked participants to give full play to their drawing ability. 
3. **Sketch Annotation:** We deployed a sketch annotation system to annotate SFSD. Another group of participants were employed to finish the sketch annotation. Each stroke was assigned with certain background or foreground categories. Attributes like drawing completeness and similarity of all objects are also recorded for future work.

### Dataset Sample

Example sketch-photo pairs in SFSD. The sketch shown was annotated at the instance level. 

<img src="C:%5CUsers%5C123%5CDesktop%5CSnipaste_2023-09-28_15-47-44.png" alt="Snipaste_2023-09-28_15-47-44" style="zoom:60%;" />

Scene-level sketch segmentation aims to predict class label of **each stroke** in scene sketch, which outperforms object-level segmentation of a large margin in the aspect of semantic context.

<img src="C:%5CUsers%5C123%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5C1695886975350.png" alt="1695886975350" style="zoom:67%;" />

### Dataset Structure

```
SFSD
├── images
├── sketch		           (contains stroke information)
├── sketchImg
└── categories_info.json   (category details)
```

## Dataset Statistics and Analysis

The following table shows comparison of different sketch components with existing scene sketch datasets, ranging from strokes, objects to categories. Our dataset contains **40** categories, more than twice the number of categories in SketchyCOCO, which also referenced **real images**. In our dataset, sketches contain an average of **146 strokes**, which is much higher than previous single-object sketch dataset and can describe more details of the objects. Moreover, to the best of our knowledge, previous scene sketch datasets do not contain **stroke order information**.


## Citation

```
@article{zhang2022stroke,
  title={Stroke-based semantic segmentation for scene-level free-hand sketches},
  author={Zhang, Zhengming and Deng, Xiaoming and Li, Jinyao and Lai, Yukun and Ma, Cuixia and Liu, Yongjin and Wang, Hongan},
  journal={The Visual Computer},
  pages={1--13},
  year={2022},
  publisher={Springer}
}
```
