# Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review [Journal Pre-print]
Welcome to the official repository of our journal paper: 

### Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review

Thang-Anh-Quan Nguyen*, Amine Bourki*, Màtyàs Macudzinski, Anthony Brunel, and [Mohammed Bennamoun](https://research-repository.uwa.edu.au/en/persons/mohammed-bennamoun)

(*: Denotes equal contribution).
  
![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/89ed66ae-7f9c-4bec-a388-ad7a5fd650c9)


  [[Paper]()]     [[arXiv](https://arxiv.org/pdf/2402.11141.pdf)$^1$]     [[Website](https://arxiv.org/pdf/2402.11141.pdf)]
  
$1$: Most up-to-date version with extended bibliography and additional contents.

## 1. Introduction
This repository presents a comprehensive review of recent works in the field of Neural Radiance Fields (NeRFs), with a specific focus on the integration of semantic information for enhanced visual scene understanding. Neural radiance fields have demonstrated the potential of coordinate-based neural representation, also known as neural fields or implicit neural representation. Our review aims to provide a detailed analysis of the advancements in this area, shedding light on the significance of semantically-aware NeRFs in various applications.

We invite you to explore the information and insights offered by this repository, which includes a curated list of papers, datasets, and comprehensive benchmark results related to semanticaly-aware NeRFs in the context of visual scene understanding.

### Contact
Please feel free to [contact me](mailto:amine.bourki@inception-lab.com), or open a [github issue](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/issues) if you have suggestions for improvements, insights, or if you'd like to contribute with new results or references!


## 2. Comparative Analysis of Previous NeRF Studies

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/84cec94a-6c82-4307-b8c7-20dc37d0ea16)

'Semantic Tasks' include: G: 3D Geometry Enhancement, S: Segmentation, E: Editable NeRFs,
O: Object Detection and 6D Pose, H: Holistic Decomposition, L: NeRFs and Language, .: denotes missing task. 
'Semantic Focus' refers to whether the primary focus of the study is on semantics. *: Interesting reference, but not a journal paper.

## 3. Taxonomy of our Study on Semantically-aware NeRFs (SRFs)

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/b321080b-3282-4f94-b528-9f8959057778)

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/9bf9ee8f-a8fb-4aff-bf51-05399a001e44)


![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/fff8b4a2-917f-4fde-9d53-04cc52f3eb34)


## 4. Datasets

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/71ae6de8-ad3e-4015-aebb-05d998879cfd)

### Overview of existing datasets for SRF-based multi-view scene understanding.
Legend: ‘Centricity’ refers to scene and/or object-centric datasets, respectively denoted with S and O above.



| **Datasets with URL**                                                                                      | **Venue**          | **#Scenes**           | **#Imgs**           | **Centricity**          | **Type**          | **Data Modalities**          | **Annotations**                           |
|------------------------------------------------------------------------------------------------------------|--------------------|-----------------------|---------------------|-------------------------|-------------------|------------------------------|-------------------------------------------|
| **[3DMV-VQA](https://vis-www.cs.umass.edu/3d-clr/)**                                                       | CVPR 2023          | 5000                  | 600K                | S+O                     | Indoor            | RGB                          | Visual question & answer                  | 
| **[NeRDS 360](https://zubair-irshad.github.io/projects/neo360.html)**                                      | ICCV 2023          | 75                    | 15k                 | S+O                     | Urban             | Synthetic                    | 3D object boxes; 2D panoptic segmentation |
| **[ScanNet++](https://cy94.github.io/scannetpp/)**                                                         | ICCV 2023          | 460                   | 3.7M                | S                       | Indoor            | RGB-D                        | 2D/3D panoptic segmentation               |
| **[KITTI-360](https://www.cvlibs.net/datasets/kitti-360/)**                                                | PAMI 2022          | 10                    | 150K                | S+O                     | Urban             | RGB & LiDAR                  | 2D/3D object boxes; 2D panoptic segmentation|
| **[SHIFT](https://www.vis.xyz/shift/)**                                                                    | CVPR 2022          | 4850                  | 2.5M                | S+O                     | Urban             | Synthetic                    | 2D/3D object boxes; 2D panoptic segmentation|
| **[HM3D Sem](https://aihabitat.org/datasets/hm3d-semantics/)**                                             | arXiv 2022         | 216                   | -                   | S                       | Indoor            | Mesh                         | 3D semantic segmentation                  |
| **[3D-FRONT](https://tianchi.aliyun.com/specials/promotion/alibaba-3d-scene-dataset)**                     | ICCV 2021          | 18968                 | -                   | S+O                     | Indoor            | Synthetic                    | 3D semantic segmentation                  | 
| **[HyperSim](https://github.com/apple/ml-hypersim)**                                                       | ICCV 2021          | 461                   | 77.4K               | S+O                     | Indoor            | Synthetic                    | 2D/3D object boxes; 2D/3D panoptic segmentation|
| **[Waymo](https://waymo.com/open/)**                                                                       | CVPR 2020          | 1150                  | 1M                  | S+O                     | Urban             | RGB & LiDAR                  | 2D/3D object boxes; 2D panoptic segmentation|
| **[nuScenes](https://www.nuscenes.org/)**                                                                  | CVPR 2020          | 1000                  | 1.4M                | S+O                     | Urban             | RGB & LiDAR                  | 3D object boxes; 2D panoptic segmentation |
| **[Replica](https://github.com/facebookresearch/Replica-Dataset)**                                         | arXiv 2019         | 18                    | -                   | S                       | Indoor            | Mesh                         | 2D/3D panoptic segmentation               |
| **[Matterport 3D](https://niessner.github.io/Matterport//)**                                               | 3DV 2017           | 90                    | 194.4K              | S                       | Indoor            | RGB-D                        | 2D/3D panoptic segmentation               |
| **[CLEVR](https://cs.stanford.edu/people/jcjohns/clevr/)**                                                 | CVPR 2017          | -                     | 100K                | O                       | Indoor            | Synthetic                    | Visual question & answer                  |
| **[ScanNet](http://www.scan-net.org/)**                                                                    | CVPR 2017          | 1513                  | 2.5M                | S+O                     | Indoor            | RGB-D                        | 3D object boxes; 2D/3D panoptic segmentation|
| **[Virtual KITTI](https://europe.naverlabs.com/research/computer-vision/proxy-virtual-worlds-vkitti-2/)**  | CVPR 2016          | 5                     | 17K                 | S+O                     | Urban             | Synthetic                    | 2D/3D object boxes; 2D panoptic segmentation|
| **[SUN RGB-D](https://rgbd.cs.princeton.edu/)**                                                            | CVPR 2015          | 47                    | 10.3K               | S+O                     | Indoor            | RGB-D                        | 2D/3D object boxes; 2D panoptic segmentation|
| **[Shapenet](https://shapenet.org/)**                                                                      | arXiv 2015         | -                     | -                   | O                       | Objects           | CAD model                    | 3D part segmentation                      |
| **[KITTI](https://www.cvlibs.net/datasets/kitti/)**                                                        | CVPR 2012          | 22                    | 15K                 | S+O                     | Urban             | RGB & LiDAR                  | 2D/3D object boxes; 2D panoptic segmentation|


## Citation
If you find this work useful, please consider citing it in your research as follows:

```
@article{SRFsota2024,
    title          = {Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review},
    author         = {Thang-Anh-Quan Nguyen and Amine Bourki and M\'aty\'as Macudzinski and Anthony Brunel and Mohammed Bennamoun},
    year           = {2024},
    eprint         = {2402.11141},
    archivePrefix  = {arXiv},
    primaryClass   = {cs.CV}
}
```


## Last Updates
- **02/17/2024:** Initial release :rocket:.
