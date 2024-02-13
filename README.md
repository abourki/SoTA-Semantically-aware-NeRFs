# SoTA-Semantically-aware-NeRFs
[Journal Pre-print] Semantically-aware Neural Radiance Fields for Visual Scene Understanding: A Comprehensive Review

Thang-Anh-Quan Nguyen*, Amine Bourki*, Matyas Macudzinski, Anthony Brunel, Mohammed Bennamoun

*: equal coontribution.

<p align="center">
  <a href="http://flybo.org/"><img width= 650 src="![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/e5f83286-2b00-49ef-95d7-eb987c99624f)"></a>
</p>



# 1. Comparative Overview of Previous NeRF Studies

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/b49c5b27-8ba3-4f89-b2da-045ae4e7b4ad)

# 2. Taxonomy of our Study on Semantically-aware NeRFs

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/1f4d4f96-f5b9-404d-96e7-2a9dafbfc1f8)

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/c6418018-5304-45d3-8f0e-e02983ec7174)



# 3. Datasets and Evaluation

## Overview of existing datasets for SRF-based multi-view scene understanding.
Legend: ‘Centricity’ refers to scene and/or object-centric datasets, respectively denoted with S and O above.

![image](https://github.com/abourki/SoTA-Semantically-aware-NeRFs/assets/12202074/f6b35395-9187-43cc-ad7d-d263fc1a60df)




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

# Permalink to the Most Up-to-date Version of our Paper

[arXiv link](https:google.com)
