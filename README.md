# Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review [Journal Pre-print]
Welcome to the official repository of **Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review** (Journal Pre-print).

### Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review

Thang-Anh-Quan Nguyen*, Amine Bourki*, Matyas Macudzinski, Anthony Brunel, and [Mohammed Bennamoun](https://research-repository.uwa.edu.au/en/persons/mohammed-bennamoun)

(*: Denotes equal contribution).
  
![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/89ed66ae-7f9c-4bec-a388-ad7a5fd650c9)


  [[Paper]()]     [[arXiv](https://arxiv.org/)]     [[Website](https://arxiv.org/)]


## 1. Introduction
This repository presents a comprehensive review of recent works in the field of Neural Radiance Fields (NeRFs), with a specific focus on the integration of semantic information for enhanced visual scene understanding. Neural radiance fields have demonstrated the potential of coordinate-based neural representation, also known as neural fields or implicit neural representation. Our review aims to provide a detailed analysis of the advancements in this area, shedding light on the significance of semantically-aware NeRFs in various applications.

We invite you to explore the wealth of information and insights offered by this repository, which includes a curated list of papers, datasets, and comprehensive benchmark results related to semanticaly-aware NeRFs in the context of visual scene understanding.

### Contact
Please feel free to [contact me](mailto:amine.bourki@inception-lab.com), or open a [github issue](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/issues) if you have suggestions for improvements, insights, or if you'd like to contribute with new results or references!


## 2. Comparative Overview of Previous NeRF Studies

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/84cec94a-6c82-4307-b8c7-20dc37d0ea16)

#### Comparative overview of previously existing NeRF surveys w.r.t semantic considerations. 
'Semantic Tasks' include: G: 3D Geometry Enhancement, S: Segmentation, E: Editable NeRFs,
O: Object Detection and 6D Pose, H: Holistic Decomposition, L: NeRFs and Language, .: denotes missing task. 
'Semantic Focus' refers to whether the primary focus of the study is on semantics. *: Interesting reference, but not a journal paper.

## 3. Taxonomy of our Study on Semantically-aware NeRFs

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/b321080b-3282-4f94-b528-9f8959057778)

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/9bf9ee8f-a8fb-4aff-bf51-05399a001e44)


![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/fff8b4a2-917f-4fde-9d53-04cc52f3eb34)


## 4. Datasets and Evaluation

### Overview of existing datasets for SRF-based multi-view scene understanding.
Legend: ‘Centricity’ refers to scene and/or object-centric datasets, respectively denoted with S and O above.

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/71ae6de8-ad3e-4015-aebb-05d998879cfd)





| **\textbf{Datasets}**                           | **\textbf{Venue}** | **\textbf{\#Scenes}** | **\textbf{\#Imgs}** | **\textbf{Centricity}** | **\textbf{Type}** | **\textbf{Data Modalities}** | **\textbf{Annotations}**                  | **\textbf{URL}**                                                                        |
|-------------------------------------------------|--------------------|-----------------------|---------------------|-------------------------|-------------------|------------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------|
| **3DMV-VQA~\cite{hong20233d}**                  | CVPR 2023          | 5000                  | 600K                | S+O                     | Indoor            | RGB                          | Visual question \                         | [URL](https://vis-www.cs.umass.edu/3d-clr/}{\faLink})          |
| **NeRDS 360~\cite{irshad2023neo}**              | ICCV 2023          | 75                    | 15k                 | S+O                     | Urban             | Synthetic                    | \makecell[l]{3D object boxes              |
| **ScanNet++~\cite{yeshwanth2023scannet}**       | ICCV 2023          | 460                   | 3.7M                | S                       | Indoor            | RGB-D                        | \makecell[l]{2D/3D panoptic segmentation} | \Dhref{https://cy94.github.io/scannetpp/}{\faLink}                                      |
| **KITTI-360~\cite{liao2022kitti}**              | PAMI 2022          | 10                    | 150K                | S+O                     | Urban             | RGB                          | LiDAR                                     | \makecell[l]{2D/3D object boxes                                                         |
| **SHIFT~\cite{sun2022shift}**                   | CVPR 2022          | 4850                  | 2.5M                | S+O                     | Urban             | Synthetic                    | \makecell[l]{2D/3D object boxes           |
| **HM3D Sem~\cite{yadav2023habitat}**            | arXiv 2022         | 216                   | -                   | S                       | Indoor            | Mesh                         | 3D semantic segmentation                  | \Dhref{https://aihabitat.org/datasets/hm3d-semantics/}{\faLink}                         |
| **3D-FRONT~\cite{fu20213d}**                    | ICCV 2021          | 18968                 | -                   | S+O                     | Indoor            | Synthetic                    | 3D semantic segmentation                  | \Dhref{https://tianchi.aliyun.com/specials/promotion/alibaba-3d-scene-dataset}{\faLink} |
| **HyperSim~\cite{roberts2021hypersim}**         | ICCV 2021          | 461                   | 77.4K               | S+O                     | Indoor            | Synthetic                    | \makecell[l]{2D/3D object boxes           |
| **Waymo~\cite{sun2020scalability}**             | CVPR 2020          | 1150                  | 1M                  | S+O                     | Urban             | RGB                          | LiDAR                                     | \makecell[l]{2D/3D object boxes                                                         |
| **nuScenes~\cite{caesar2020nuscenes}**          | CVPR 2020          | 1000                  | 1.4M                | S+O                     | Urban             | RGB                          | LiDAR                                     | \makecell[l]{3D object boxes                                                            |
| **Replica~\cite{straub2019replica}**            | arXiv 2019         | 18                    | -                   | S                       | Indoor            | Mesh                         | 2D/3D panoptic segmentation               | \Dhref{https://github.com/facebookresearch/Replica-Dataset}{\faLink}                    |
| **Matterport 3D~\cite{chang2017matterport3d}**  | 3DV 2017           | 90                    | 194.4K              | S                       | Indoor            | RGB-D                        | 2D/3D panoptic segmentation               | \Dhref{https://niessner.github.io/Matterport//}{\faLink}                                |
| **CLEVR~\cite{johnson2017clevr}**               | CVPR 2017          | -                     | 100K                | O                       | Indoor            | Synthetic                    | Visual question \                         | answer                                                                                  | \Dhref{https://cs.stanford.edu/people/jcjohns/clevr/}{\faLink} |
| **ScanNet~\cite{dai2017scannet}**               | CVPR 2017          | 1513                  | 2.5M                | S+O                     | Indoor            | RGB-D                        | \makecell[l]{3D object boxes              |
| **Virtual KITTI~\cite{gaidon2016virtual}**      | CVPR 2016          | 5                     | 17K                 | S+O                     | Urban             | Synthetic                    | \makecell[l]{2D/3D object boxes           |
| **SUN RGB-D~\cite{song2015sun}**                | CVPR 2015          | 47                    | 10.3K               | S+O                     | Indoor            | RGB-D                        | \makecell[l]{2D/3D object boxes           |
| **Shapenet~\cite{chang2015shapenet}**           | arXiv 2015         | -                     | -                   | O                       | Objects           | CAD model                    | 3D part segmentation                      | \Dhref{https://shapenet.org/}{\faLink}                                                  |
| **KITTI~\cite{geiger2012we, geiger2013vision}** | CVPR 2012          | 22                    | 15K                 | S+O                     | Urban             | RGB                          | LiDAR                                     | \makecell[l]{2D/3D object boxes                                                         |

## Citation
If you find this work useful, please consider citing it as follows:

```
@inproceedings{SRFs2024,
  title={Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review},
  author={Nguyen, Thang-Anh-Quan Nguyen and Bourki, Amine and Macudzinski, Matyas and Brunel, Anthony and Bennamoun, Mohammed},
  journal={arXiv preprint arXiv:2xxxx},
  year={2024}
}
```

