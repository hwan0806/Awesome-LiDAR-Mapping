# Awesome-LiDAR-Mapping [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)



This repository is a collection of paper with open-sourced codes for LiDAR-based mapping methods. It includes LiDAR-based odometry, dynamic object removal, and multiple map merging frameworks, which is essential for long-term robotic autonomy. </br>
Thanks to the authors of the [LiDAR Odometry Survey](https://arxiv.org/abs/2312.17487) and [Awesome LiDAR Place Recognition](https://github.com/hogyun2/awesome-lidar-place-recognition) for inspiring this work.



## [Table of Contents](#table-of-contents)
- [LiDAR Mapping](#lidar-mapping)
  - [LiDAR Only](#lidar-only)
  - [LiDAR-Inertial](#lidar-inertial)
  - [Multiple LiDARs](#multiple-lidars)
  - [Learning-based Mapping](#learning-based-mapping)
- [Static Mapping](#static-mapping)
  - [Algorithm-based](#algorithm-based)
  - [Learning-based](#learning-based)
- [Multiple Map Merging](#multiple-map-merging)
- [Useful repository](#useful-repository)
  - [LiDAR Odometry](#lidar-odometry)
  - [SLAM Framework (Odometry+PGO)](#slam-framework-odometrypgo)
  - [Evaluation](#evaluation)
- [Acknowledgement](#acknowledgement)
- [Contact](#contact)



**Venue Acronyms**
- `ICRA`
- `IROS`
- `RSS`
- `RAL`
- `CVPR`
- `ICCV`
- `AAAI`
- `TIV`
- `TPAMI`
- `TRO`
- `NATCOM`
- `ISPRS`
- `SJ`



## LiDAR Mapping

### LiDAR Only

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|14|`RSS`|[LOAM: Lidar odometry and mapping in real-time](https://www.ri.cmu.edu/pub_files/2014/7/Ji_LidarMapping_RSS2014_v8.pdf)|[![Github stars](https://img.shields.io/github/stars/laboshinl/loam_velodyne.svg)](https://github.com/laboshinl/loam_velodyne)<br>[![Github stars](https://img.shields.io/github/stars/HKUST-Aerial-Robotics/A-LOAM.svg)](https://github.com/HKUST-Aerial-Robotics/A-LOAM)|
|18|`RSS`|[Efficient Surfel-Based SLAM using 3D Laser Range Data in Urban Environments](https://roboticsproceedings.org/rss14/p16.pdf)|[![Github stars](https://img.shields.io/github/stars/jbehley/SuMa.svg)](https://github.com/jbehley/SuMa)|
|18|`IROS`|[LeGO-LOAM: Lightweight and Ground-Optimized Lidar Odometry and Mapping on Variable Terrain](https://ieeexplore.ieee.org/abstract/document/8594299)|[![Github stars](https://img.shields.io/github/stars/RobustFieldAutonomyLab/LeGO-LOAM.svg)](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM)|
|19|`RSS`|[A Modular Optimization Framework for Localization and Mapping](https://www.roboticsproceedings.org/rss15/p43.pdf)|[![Github stars](https://img.shields.io/github/stars/MOLAorg/mola.svg)](https://github.com/MOLAorg/mola)|
|20|`ICRA`|[Loam livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV](https://ieeexplore.ieee.org/document/9197440)|[![Github stars](https://img.shields.io/github/stars/hku-mars/loam_livox.svg)](https://github.com/hku-mars/loam_livox)|
|20|`ICRA`|[LOL: Lidar-only Odometry and Localization in 3D point cloud maps](https://ieeexplore.ieee.org/abstract/document/9197450)|[![Github stars](https://img.shields.io/github/stars/RozDavid/LOL.svg)](https://github.com/RozDavid/LOL)|
|21|`ICRA`|[MULLS: Versatile LiDAR SLAM via Multi-metric Linear Least Square](https://ieeexplore.ieee.org/abstract/document/9561364)|[![Github stars](https://img.shields.io/github/stars/YuePanEdward/MULLS.svg)](https://github.com/YuePanEdward/MULLS)|
|21|`IROS`|[F-LOAM : Fast LiDAR Odometry and Mapping](https://arxiv.org/pdf/2107.00822)|[![Github stars](https://img.shields.io/github/stars/wh200720041/floam.svg)](https://github.com/wh200720041/floam)|
|21|`TGMS`|[T-LOAM: Truncated Least Squares Lidar-only Odometry and Mapping in Real-Time](https://ieeexplore.ieee.org/document/9446309)|[![Github stars](https://img.shields.io/github/stars/zhoupengwei/tloam.svg)](https://github.com/zhoupengwei/tloam)|
|21|`RAL`|[Interactive 3D Graph SLAM for Map Correction](https://ieeexplore.ieee.org/document/9212613)|[![Github stars](https://img.shields.io/github/stars/SMRT-AIST/interactive_slam.svg)](https://github.com/SMRT-AIST/interactive_slam)|
|22|`ICRA`|[CT-ICP: Real-time Elastic LiDAR Odometry with Loop Closure](https://arxiv.org/abs/2109.12979)|[![Github stars](https://img.shields.io/github/stars/jedeschaud/ct_icp.svg)](https://github.com/jedeschaud/ct_icp)|
|22|`RAL`|[Direct LiDAR Odometry: Fast Localization with Dense Point Clouds](https://arxiv.org/pdf/2110.00605)|[![Github stars](https://img.shields.io/github/stars/vectr-ucla/direct_lidar_odometry.svg)](https://github.com/vectr-ucla/direct_lidar_odometry)|
|22|`RAL`|[LOCUS 2.0: Robust and Computationally Efficient Lidar Odometry for Real-Time 3D Mapping](https://arxiv.org/pdf/2205.11784)|[![Github stars](https://img.shields.io/github/stars/NeBula-Autonomy/LOCUS.svg)](https://github.com/NeBula-Autonomy/LOCUS)|
|22|`RAL`|[Efficient and Probabilistic Adaptive Voxel Mapping for Accurate Online LiDAR Odometry](https://arxiv.org/abs/2109.07082)|[![Github stars](https://img.shields.io/github/stars/hku-mars/VoxelMap.svg)](https://github.com/hku-mars/VoxelMap)|
|23|`ICRA`|[Real-Time Simultaneous Localization and Mapping with LiDAR intensity](https://arxiv.org/abs/2301.09257)|[![Github stars](https://img.shields.io/github/stars/MISTLab/Intensity_based_LiDAR_SLAM.svg)](https://github.com/MISTLab/Intensity_based_LiDAR_SLAM)|
|23|`IROS`|[ECTLO: Effective Continuous-Time Odometry Using Range Image for LiDAR with Small FoV](https://ieeexplore.ieee.org/abstract/document/10341592)|[![Github stars](https://img.shields.io/github/stars/kevin2431/ECTLO.svg)](https://github.com/kevin2431/ECTLO)|
|23|`RAL`|[KISS-ICP: In Defense of Point-to-Point ICP – Simple, Accurate, and Robust Registration If Done the Right Way](?)|[![Github stars](https://img.shields.io/github/stars/PRBonn/kiss-icp.svg)](https://github.com/PRBonn/kiss-icp)|
|23|`ICRA`|[SLAMesh: Real-time LiDAR Simultaneous Localization and Meshing](https://arxiv.org/pdf/2303.05252)|[![Github stars](https://img.shields.io/github/stars/lab-sun/SLAMesh.svg)](https://github.com/lab-sun/SLAMesh)|
|23|`RAL`|[HBA: A Globally Consistent and Efficient Large-Scale LiDAR Mapping Module](https://ieeexplore.ieee.org/abstract/document/10024300)|[![Github stars](https://img.shields.io/github/stars/hku-mars/HBA.svg)](https://github.com/hku-mars/HBA)|
|21,</br>23|`RAL`,</br>`TRO`|[BALM: Bundle Adjustment for Lidar Mapping](https://ieeexplore.ieee.org/abstract/document/9366383),</br>[Efficient and Consistent Bundle Adjustment on Lidar Point Clouds](https://ieeexplore.ieee.org/abstract/document/10263983)|[![Github stars](https://img.shields.io/github/stars/hku-mars/BALM.svg)](https://github.com/hku-mars/BALM)|
|24|`RAL`|[Light-LOAM: A Lightweight LiDAR Odometry and Mapping based on Graph-Matching](https://arxiv.org/pdf/2310.04162)|[![Github stars](https://img.shields.io/github/stars/BrenYi/Light-LOAM.svg)](https://github.com/BrenYi/Light-LOAM)|
|24|`RAL`|[Traj-LO: In Defense of LiDAR-Only Odometry Using an Effective Continuous-Time Trajectory](https://ieeexplore.ieee.org/document/10387726)|[![Github stars](https://img.shields.io/github/stars/kevin2431/Traj-LO.svg)](https://github.com/kevin2431/Traj-LO)|
|24|`arXiv`|[MAD-ICP: It Is All About Matching Data – Robust and Informed LiDAR Odometry](https://arxiv.org/abs/2405.05828)|[![Github stars](https://img.shields.io/github/stars/rvp-group/mad-icp.svg)](https://github.com/rvp-group/mad-icp)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>


### LiDAR-Inertial

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|19|`ICRA`|[A Tightly Coupled 3D Lidar and Inertial Odometry and Mapping Approach](https://arxiv.org/abs/1904.06993)|[![Github stars](https://img.shields.io/github/stars/hyye/lio-mapping.svg)](https://github.com/hyye/lio-mapping)|
|20|`ICRA`|[LINS: A Lidar-Inertial State Estimator for Robust and Efficient Navigation](https://ieeexplore.ieee.org/abstract/document/9197567)|[![Github stars](https://img.shields.io/github/stars/ChaoqinRobotics/LINS---LiDAR-inertial-SLAM.svg)](https://github.com/ChaoqinRobotics/LINS---LiDAR-inertial-SLAM)|
|20|`IROS`|[LIO-SAM: Tightly-coupled Lidar Inertial Odometry via Smoothing and Mapping](https://ieeexplore.ieee.org/abstract/document/9341176)|[![Github stars](https://img.shields.io/github/stars/TixiaoShan/LIO-SAM.svg)](https://github.com/TixiaoShan/LIO-SAM)|
|21|`ICRA`|[Poisson Surface Reconstruction for LiDAR Odometry and Mapping](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/vizzo2021icra.pdf)|[![Github stars](https://img.shields.io/github/stars/PRBonn/puma.svg)](https://github.com/PRBonn/puma)|
|21|`IROS`|[CLINS : Continuous-Time Trajectory Estimation for LiDAR-Inertial System](https://arxiv.org/pdf/2109.04687.pdf)|[![Github stars](https://img.shields.io/github/stars/APRIL-ZJU/clins.svg)](https://github.com/APRIL-ZJU/clins)|
|21|`RAL`|[Towards High-Performance Solid-State-LiDAR-Inertial Odometry and Mapping](https://ieeexplore.ieee.org/document/9392274)|[![Github stars](https://img.shields.io/github/stars/KIT-ISAS/lili-om.svg)](https://github.com/KIT-ISAS/lili-om)|
|21,</br>22|`RAL`,</br>`TRO`|[FAST-LIO: A Fast, Robust LiDAR-inertial Odometry Package by Tightly-Coupled Iterated Kalman Filter](https://ieeexplore.ieee.org/abstract/document/9372856), </br> [FAST-LIO2: Fast Direct LiDAR-Inertial Odometry](https://ieeexplore.ieee.org/abstract/document/9697912)|[![Github stars](https://img.shields.io/github/stars/hku-mars/FAST_LIO.svg)](https://github.com/hku-mars/FAST_LIO)|
|22|`RAL`|[Faster-LIO: Lightweight Tightly Coupled Lidar-Inertial Odometry Using Parallel Sparse Incremental Voxels](https://ieeexplore.ieee.org/abstract/document/9718203)|[![Github stars](https://img.shields.io/github/stars/gaoxiang12/faster-lio.svg)](https://github.com/gaoxiang12/faster-lio)|
|22|`arXiv`|[SR-LIO: LiDAR-Inertial Odometry with Sweep Reconstruction](https://arxiv.org/abs/2210.10424)|[![Github stars](https://img.shields.io/github/stars/ZikangYuan/sr_lio.svg)](https://github.com/ZikangYuan/sr_lio)|
|23|`ICRA`|[Direct LiDAR-Inertial Odometry: Lightweight LIO with Continuous-Time Motion Correction](https://ieeexplore.ieee.org/document/10160508)|[![Github stars](https://img.shields.io/github/stars/vectr-ucla/direct_lidar_inertial_odometry.svg)](https://github.com/vectr-ucla/direct_lidar_inertial_odometry)|
|23|`ICRA`|[Asynchronous State Estimation of Simultaneous Ego-motion Estimation and Multiple Object Tracking for LiDAR-Inertial Odometry](https://ieeexplore.ieee.org/document/10161269)|[![Github stars](https://img.shields.io/github/stars/StephLin/LIO-SEGMOT.svg)](https://github.com/StephLin/LIO-SEGMOT)|
|23|`IROS`|[LIO-PPF: Fast LiDAR-Inertial Odometry via Incremental Plane Pre-Fitting and Skeleton Tracking](https://ieeexplore.ieee.org/abstract/document/10341524)|[![Github stars](https://img.shields.io/github/stars/xingyuuchen/LIO-PPF.svg)](https://github.com/xingyuuchen/LIO-PPF)|
|23|`RAL`|[FF-LINS: A Consistent Frame-to-Frame Solid-State-LiDAR-Inertial State Estimator](https://ieeexplore.ieee.org/abstract/document/10305296)|[![Github stars](https://img.shields.io/github/stars/i2Nav-WHU/FF-LINS.svg)](https://github.com/i2Nav-WHU/FF-LINS)|
|23|`RAL`|[LOG-LIO: A LiDAR-Inertial Odometry with Efficient Local Geometric Information Estimation](https://ieeexplore.ieee.org/abstract/document/10314726)|[![Github stars](https://img.shields.io/github/stars/tiev-tongji/LOG-LIO.svg)](https://github.com/tiev-tongji/LOG-LIO)|
|23|`RAL`|[RI-LIO: Reflectivity Image Assisted Tightly-Coupled LiDAR-Inertial Odometry](https://ieeexplore.ieee.org/document/10041769)|[![Github stars](https://img.shields.io/github/stars/RoboFeng/RI-LIO.svg)](https://github.com/RoboFeng/RI-LIO)|
|23|`RAL`|[Voxelmap++: Mergeable Voxel Mapping Method for Online LiDAR(-inertial) Odometry](https://ieeexplore.ieee.org/abstract/document/10321658)|[![Github stars](https://img.shields.io/github/stars/uestc-icsp/VoxelMapPlus_Public.svg)](https://github.com/uestc-icsp/VoxelMapPlus_Public)|
|23|`RAL`|[S-Graphs+: Real-time Localization and Mapping leveraging Hierarchical Representations](https://arxiv.org/abs/2212.11770)|[![Github stars](https://img.shields.io/github/stars/snt-arg/lidar_s_graphs.svg)](https://github.com/snt-arg/lidar_s_graphs)|
|23|`AIS`|[Point‐LIO: Robust High‐Bandwidth Light Detection and Ranging Inertial Odometry](https://onlinelibrary.wiley.com/doi/full/10.1002/aisy.202200459)|[![Github stars](https://img.shields.io/github/stars/hku-mars/Point-LIO.svg)](https://github.com/hku-mars/Point-LIO)|
|24|`ICRA`|[COIN-LIO: Complementary Intensity-Augmented LiDAR Inertial Odometry](https://arxiv.org/abs/2310.01235)|[![Github stars](https://img.shields.io/github/stars/ethz-asl/COIN-LIO.svg)](https://github.com/ethz-asl/COIN-LIO)|
|24|`ICRA`|[LIO-EKF: High Frequency LiDAR-Inertial Odometry using Extended Kalman Filters](https://arxiv.org/pdf/2311.09887)|[![Github stars](https://img.shields.io/github/stars/YibinWu/LIO-EKF.svg)](https://github.com/YibinWu/LIO-EKF)|
|24|`ICRA`|[DMSA - Dense Multi Scan Adjustment for LiDAR Inertial Odometry and Global Optimization](https://arxiv.org/abs/2402.19044)|[![Github stars](https://img.shields.io/github/stars/davidskdds/DMSA_LiDAR_SLAM.svg)](https://github.com/davidskdds/DMSA_LiDAR_SLAM)|
|24|`RAL`|[iG-LIO: An Incremental GICP-based Tightly-coupled LiDAR-inertial Odometry](https://ieeexplore.ieee.org/abstract/document/10380742)|[![Github stars](https://img.shields.io/github/stars/zijiechenrobotics/ig_lio.svg)](https://github.com/zijiechenrobotics/ig_lio)|
|24|`RAL`|[LIO-GVM: an Accurate, Tightly-Coupled Lidar-Inertial Odometry with Gaussian Voxel Map](https://arxiv.org/pdf/2306.17436)|[![Github stars](https://img.shields.io/github/stars/Ji1Xingyu/lio_gvm.svg)](https://github.com/Ji1Xingyu/lio_gvm)|
|24|`RAL`|[LIMOT: A Tightly-Coupled System for LiDAR-Inertial Odometry and Multi-Object Tracking](https://ieeexplore.ieee.org/abstract/document/10538416)|[![Github stars](https://img.shields.io/github/stars/tiev-tongji/LIMOT.svg)](https://github.com/tiev-tongji/LIMOT)|
|24|`arXiv`|[NV-LIO: LiDAR-Inertial Odometry using Normal Vectors Towards Robust SLAM in Multifloor Environments](https://arxiv.org/abs/2405.12563)|[![Github stars](https://img.shields.io/github/stars/dhchung/nv_lio.svg)](https://github.com/dhchung/nv_lio)|
|24|`arXiv`|[LOG-LIO2: A LiDAR-Inertial Odometry with Efficient Uncertainty Analysis](https://arxiv.org/abs/2405.01316)|[![Github stars](https://img.shields.io/github/stars/tiev-tongji/LOG-LIO2.svg)](https://github.com/tiev-tongji/LOG-LIO2)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>


### Multiple LiDARs

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|20|`IROS`|[A decentralized framework for simultaneous calibration, localization and mapping with multiple LiDARs](https://arxiv.org/abs/2007.01483)|[![Github stars](https://img.shields.io/github/stars/hku-mars/decentralized_loam.svg)](https://github.com/hku-mars/decentralized_loam)|
|21|`TRO`|[Robust Odometry and Mapping for Multi-LiDAR Systems with Online Extrinsic Calibration](https://arxiv.org/pdf/2010.14294)|[![Github stars](https://img.shields.io/github/stars/gogojjh/M-LOAM.svg)](https://github.com/gogojjh/M-LOAM)|
|23|`RAL`|[Asynchronous Multiple LiDAR-Inertial Odometry using Point-wise Inter-LiDAR Uncertainty Propagation](https://minwoo0611.github.io/publications/ral2023_mwjung.pdf)|[![Github stars](https://img.shields.io/github/stars/minwoo0611/MA-LIO.svg)](https://github.com/minwoo0611/MA-LIO)|
|23|`RAL`|[SLICT: Multi-Input Multi-Scale Surfel-Based Lidar-Inertial Continuous-Time Odometry and Mapping](https://ieeexplore.ieee.org/abstract/document/10048526)|[![Github stars](https://img.shields.io/github/stars/brytsknguyen/slict.svg)](https://github.com/brytsknguyen/slict)|
|23|`arXiv`|[Robust Multi-Modal Multi-LiDAR-Inertial Odometry and Mapping for Indoor Environments](https://arxiv.org/abs/2303.02684)|[![Github stars](https://img.shields.io/github/stars/TIERS/multi-modal-loam.svg)](https://github.com/TIERS/multi-modal-loam)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>


### Learning-based Mapping

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|21|`CVPR`|[PWCLO-Net: Deep LiDAR Odometry in 3D Point Clouds Using Hierarchical Embedding Mask Optimization](https://openaccess.thecvf.com/content/CVPR2021/html/Wang_PWCLO-Net_Deep_LiDAR_Odometry_in_3D_Point_Clouds_Using_Hierarchical_CVPR_2021_paper.html)|[![Github stars](https://img.shields.io/github/stars/IRMVLab/PWCLONet.svg)](https://github.com/IRMVLab/PWCLONet)|
|21|`ISPRS`|[DEEPLIO: DEEP LIDAR INERTIAL SENSOR FUSION FOR ODOMETRY ESTIMATION](https://isprs-annals.copernicus.org/articles/V-1-2021/47/2021/isprs-annals-V-1-2021-47-2021.pdf)|[![Github stars](https://img.shields.io/github/stars/ArashJavan/DeepLIO.svg)](https://github.com/ArashJavan/DeepLIO)|
|22|`TPAMI`|[Efficient 3D Deep LiDAR Odometry](https://arxiv.org/abs/2111.02135)|[![Github stars](https://img.shields.io/github/stars/IRMVLab/EfficientLO-Net.svg)](https://github.com/IRMVLab/EfficientLO-Net)|
|23|`ICRA`|[SHINE-Mapping: Large-Scale 3D Mapping Using Sparse Hierarchical Implicit NEural Representations](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/zhong2023icra.pdf)|[![Github stars](https://img.shields.io/github/stars/PRBonn/SHINE_mapping.svg)](https://github.com/PRBonn/SHINE_mapping)|
|23|`RAL`|[LONER: LiDAR Only Neural Representations for Real-Time SLAM](https://arxiv.org/abs/2309.04937)|[![Github stars](https://img.shields.io/github/stars/umautobots/LONER.svg)](https://github.com/umautobots/LONER)|
|23|`ICCV`|[NeRF-LOAM: Neural Implicit Representation for Large-Scale Incremental LiDAR Odometry and Mapping](https://arxiv.org/pdf/2303.10709)|[![Github stars](https://img.shields.io/github/stars/JunyuanDeng/NeRF-LOAM.svg)](https://github.com/JunyuanDeng/NeRF-LOAM)|
|23|`TIV`|[HPPLO-Net: Unsupervised LiDAR Odometry Using a Hierarchical Point-to-Plane Solver](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10160144&tag=1)|[![Github stars](https://img.shields.io/github/stars/IMRL/HPPLO-Net.svg)](https://github.com/IMRL/HPPLO-Net)|
|24|`CVPR`|[3D LiDAR Mapping in Dynamic Environments using a 4D Implicit Neural Representation](https://www.ipb.uni-bonn.de/pdfs/zhong2024cvpr.pdf)|[![Github stars](https://img.shields.io/github/stars/PRBonn/4dNDF.svg)](https://github.com/PRBonn/4dNDF)|
|24|`AAAI`|[DeepPointMap: Advancing LiDAR SLAM with Unified Neural Descriptors](https://arxiv.org/abs/2312.02684)|[![Github stars](https://img.shields.io/github/stars/ZhangXiaze/DeepPointMap.svg)](https://github.com/ZhangXiaze/DeepPointMap)|
|24|`arXiv`|[N3-Mapping: Normal Guided Neural Non-Projective Signed Distance Fields for Large-scale 3D Mapping](https://arxiv.org/abs/2401.03412)|[![Github stars](https://img.shields.io/github/stars/tiev-tongji/N3-Mapping.svg)](https://github.com/tiev-tongji/N3-Mapping)|
|24|`arXiv`|[PIN-SLAM: LiDAR SLAM Using a Point-Based Implicit Neural Representation for Achieving Global Map Consistency](https://arxiv.org/pdf/2401.09101v1)|[![Github stars](https://img.shields.io/github/stars/PRBonn/PIN_SLAM.svg)](https://github.com/PRBonn/PIN_SLAM)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>
</br>



## Static Mapping

### Algorithm-based

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|20|`IROS`|[Remove, then Revert: Static Point cloud Map Construction using Multiresolution Range Images](https://ieeexplore.ieee.org/abstract/document/9340856)|[![Github stars](https://img.shields.io/github/stars/gisbi-kim/removert.svg)](https://github.com/gisbi-kim/removert)|
|21|`RAL`|[ERASOR: Egocentric Ratio of Pseudo Occupancy-Based Dynamic Object Removal for Static 3D Point Cloud Map Building](https://arxiv.org/abs/2103.04316)|[![Github stars](https://img.shields.io/github/stars/LimHyungTae/ERASOR.svg)](https://github.com/LimHyungTae/ERASOR)|
|23|`RAL`|[Dynablox: Real-time Detection of Diverse Dynamic Objects in Complex Environments](https://ieeexplore.ieee.org/document/10218983)|[![Github stars](https://img.shields.io/github/stars/ethz-asl/dynablox.svg)](https://github.com/ethz-asl/dynablox)|
|23|`RSS`|[ERASOR2: Instance-Aware Robust 3D Mappingof the Static World in Dynamic Scenes](https://arxiv.org/abs/2103.04316)|[![Github stars](https://img.shields.io/github/stars/url-kaist/ERASOR2.svg)](https://github.com/url-kaist/ERASOR2)|
|24|`RAL`|[RH-Map: Online Map Construction Framework of Dynamic Objects Removal Based on Region-wise Hash Map Structure](https://ieeexplore.ieee.org/document/10356720)|[![Github stars](https://img.shields.io/github/stars/YZH-bot/RH-Map.svg)](https://github.com/YZH-bot/RH-Map)|
|24|`Nature`</br>`Com`|[Moving event detection from LiDAR point streams](https://www.nature.com/articles/s41467-023-44554-8)|[![Github stars](https://img.shields.io/github/stars/hku-mars/M-detector.svg)](https://github.com/hku-mars/M-detector)|
|24|`RAL`|[DUFOMap: Efficient Dynamic Awareness Mapping](https://arxiv.org/abs/2403.01449)|[![Github stars](https://img.shields.io/github/stars/KTH-RPL/dufomap.svg)](https://github.com/KTH-RPL/dufomap)|
|24|`RAL`|[BeautyMap: Binary-Encoded Adaptable Ground Matrix for Dynamic Points Removal in Global Maps](https://arxiv.org/abs/2405.07283)|[![Github stars](https://img.shields.io/github/stars/MKJia/BeautyMap.svg)](https://github.com/MKJia/BeautyMap)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>


### Learning-based

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|21|`RAL`|[Moving Object Segmentation in 3D LiDAR Data: A Learning-based Approach Exploiting Sequential Data](https://www.ipb.uni-bonn.de/pdfs/chen2021ral-iros.pdf)|[![Github stars](https://img.shields.io/github/stars/PRBonn/LiDAR-MOS.svg)](https://github.com/PRBonn/LiDAR-MOS)|
|22|`RAL`|[Receding Moving Object Segmentation in 3D LiDAR Data Using Sparse 4D Convolutions](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/mersch2022ral.pdf)|[![Github stars](https://img.shields.io/github/stars/PRBonn/4DMOS.svg)](https://github.com/PRBonn/4DMOS)|
|22|`IROS`|[Efficient Spatial-Temporal Information Fusion for LiDAR-Based 3D Moving Object Segmentation](https://arxiv.org/abs/2207.02201)|[![Github stars](https://img.shields.io/github/stars/haomo-ai/MotionSeg3D.svg)](https://github.com/haomo-ai/MotionSeg3D)|
|23|`IROS`|[InsMOS: Instance-Aware Moving Object Segmentation in LiDAR Data](https://ieeexplore.ieee.org/document/10342277)|[![Github stars](https://img.shields.io/github/stars/nubot-nudt/InsMOS.svg)](https://github.com/nubot-nudt/InsMOS)|
|23|`RAL`|[MotionBEV: Online LiDAR Moving Object segmentation with Bird's eye view based Appearance and Motion Features](https://ieeexplore.ieee.org/document/10287575)|[![Github stars](https://img.shields.io/github/stars/xieKKKi/MotionBEV.svg)](https://github.com/xieKKKi/MotionBEV)|
|23|`RAL`|[Building Volumetric Beliefs for Dynamic Environments Exploiting Map-Based Moving Object Segmentation](https://www.ipb.uni-bonn.de/pdfs/mersch2023ral.pdf)|[![Github stars](https://img.shields.io/github/stars/PRBonn/MapMOS.svg)](https://github.com/PRBonn/MapMOS)|
|24|`ICRA`|[MF-MOS: A Motion-Focused Model for Moving Object Segmentation](https://arxiv.org/abs/2401.17023)|[![Github stars](https://img.shields.io/github/stars/SCNU-RISLAB/MF-MOS.svg)](https://github.com/SCNU-RISLAB/MF-MOS)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>
</br>



## Multiple Map Merging

<!-- ### Algorithm-based -->

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|20,</br>22|`ICRA`|[LAMP: Large-scale autonomous mapping and positioning for exploration of perceptually-degraded subterranean environments](https://ieeexplore.ieee.org/abstract/document/9197082)</br>[LAMP 2.0: A robust multi-robot SLAM system for operation in challenging large-scale underground environments](https://ieeexplore.ieee.org/abstract/document/9830862)|[![Github stars](https://img.shields.io/github/stars/NeBula-Autonomy/LAMP.svg)](https://github.com/NeBula-Autonomy/LAMP)|
|21|`RAL`|[Ground and Aerial Collaborative Mapping in Urban Environments](https://ieeexplore.ieee.org/document/9234707)|[![Github stars](https://img.shields.io/github/stars/SYSU-RoboticsLab/GAC-Mapping.svg)](https://github.com/SYSU-RoboticsLab/GAC-Mapping)|
|22|`ICRA`|[LT-mapper: A Modular Framework for LiDAR-based Lifelong Mapping](https://ieeexplore.ieee.org/abstract/document/9811916)|[![Github stars](https://img.shields.io/github/stars/gisbi-kim/lt-mapper.svg)](https://github.com/gisbi-kim/lt-mapper)|
|22|`RAL`|[DiSCo-SLAM: Distributed Scan Context-Enabled Multi-Robot LiDAR SLAM With Two-Stage Global-Local Graph Optimization](https://ieeexplore.ieee.org/abstract/document/9662965)|[![Github stars](https://img.shields.io/github/stars/RobustFieldAutonomyLab/DiSCo-SLAM.svg)](https://github.com/RobustFieldAutonomyLab/DiSCo-SLAM)|
|23|`ICRA`|[Swarm-lio: Decentralized swarm lidar-inertial odometry](https://ieeexplore.ieee.org/document/10161355)|[![Github stars](https://img.shields.io/github/stars/hku-mars/Swarm-LIO2.svg)](https://github.com/hku-mars/Swarm-LIO2)|
|23|`Sensors`|[DCL-SLAM: A Distributed Collaborative LiDAR SLAM Framework for a Robotic Swarm](https://ieeexplore.ieee.org/abstract/document/10375928)|[![Github stars](https://img.shields.io/github/stars/PengYu-Team/DCL-SLAM.svg)](https://github.com/PengYu-Team/DCL-SLAM)|
|24|`ICRA`|[CoLRIO: LiDAR-Ranging-Inertial Centralized State Estimation for Robotic Swarms](https://arxiv.org/abs/2402.11790)|[![Github stars](https://img.shields.io/github/stars/PengYu-Team/Co-LRIO.svg)](https://github.com/PengYu-Team/Co-LRIO)|
|24|`RAL`|[Swarm-SLAM: Sparse Decentralized Collaborative Simultaneous Localization and Mapping Framework for Multi-Robot Systems](https://ieeexplore.ieee.org/document/10321649)|[![Github stars](https://img.shields.io/github/stars/MISTLab/Swarm-SLAM.svg)](https://github.com/MISTLab/Swarm-SLAM)|
|24|`JFR`|[LTA-OM: Long-Term Association LiDAR-Inertial Odometry and Mapping](https://onlinelibrary.wiley.com/doi/full/10.1002/rob.22337)|[![Github stars](https://img.shields.io/github/stars/hku-mars/LTAOM.svg)](https://github.com/hku-mars/LTAOM)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>
</br>



|?|`?`|[?](?)|[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

|?|`?`|[?](?)|[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

|?|`?`|[?](?)|[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|



## Useful repository

### LiDAR Odometry

|Summary|Repository|
|-|-|
|LIO_SAM_6axis: Support 6-axis IMU and low-cost GNSS|[![Github stars](https://img.shields.io/github/stars/JokerJohn/LIO_SAM_6AXIS.svg)](https://github.com/JokerJohn/LIO_SAM_6AXIS)|
|LIORF: Remove feature extraction module of LIO-SAM|[![Github stars](https://img.shields.io/github/stars/YJZLuckyBoy/liorf.svg)](https://github.com/YJZLuckyBoy/liorf)|
|LIO-SAM-MID360: Support MID360 LiDAR|[![Github stars](https://img.shields.io/github/stars/nkymzsy/LIO-SAM-MID360.svg)](https://github.com/nkymzsy/LIO-SAM-MID360)|
|S_FAST_LIO: Simplified Implementation of FAST_LIO2|[![Github stars](https://img.shields.io/github/stars/zlwang7/S-FAST_LIO.svg)](https://github.com/zlwang7/S-FAST_LIO)|
|FAST_LIO_ROS2: ROS2 version of Fast-LIO2|[![Github stars](https://img.shields.io/github/stars/Ericsii/FAST_LIO_ROS2.svg)](https://github.com/Ericsii/FAST_LIO_ROS2)</br>[![Github stars](https://img.shields.io/github/stars/Taeyoung96/FAST_LIO_ROS2.svg)](https://github.com/Taeyoung96/FAST_LIO_ROS2)|
|Multi_FastLio: Multiple LiDAR version of Fast-LIO2 with PTP Time Sync|[![Github stars](https://img.shields.io/github/stars/SeoDU/multi_fastlio.svg)](https://github.com/SeoDU/multi_fastlio)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>


### SLAM Framework (Odometry+PGO)

|Summary|Repository|
|-|-|
|Odometry(A-LOAM, LIO-SAM, Fast-LIO) + PGO module(Scan Context)|[![Github stars](https://img.shields.io/github/stars/gisbi-kim/SC-A-LOAM.svg)](https://github.com/gisbi-kim/SC-A-LOAM)</br>[![Github stars](https://img.shields.io/github/stars/gisbi-kim/SC-LIO-SAM.svg)](https://github.com/gisbi-kim/SC-LIO-SAM)</br>[![Github stars](https://img.shields.io/github/stars/gisbi-kim/FAST_LIO_SLAM.svg)](https://github.com/gisbi-kim/FAST_LIO_SLAM)|
|FAST-LIO-SAM:Fast-LIO2 + LIO-SAM|[![Github stars](https://img.shields.io/github/stars/yanliang-wang/FAST_LIO_LC.svg)](https://github.com/yanliang-wang/FAST_LIO_LC)</br>[![Github stars](https://img.shields.io/github/stars/kahowang/FAST_LIO_SAM.svg)](https://github.com/kahowang/FAST_LIO_SAM)</br>[![Github stars](https://img.shields.io/github/stars/engcang/FAST-LIO-SAM.svg)](https://github.com/engcang/FAST-LIO-SAM)|
|FAST-LIO-SAM-QN: FAST-LIO-SAM + Quatro + Nano-GICP|[![Github stars](https://img.shields.io/github/stars/engcang/FAST-LIO-SAM-QN.svg)](https://github.com/engcang/FAST-LIO-SAM-QN)|
|FAST-LIO-SAM-SC-QN: FAST-LIO-SAM-QN + Scan Context|[![Github stars](https://img.shields.io/github/stars/engcang/FAST-LIO-SAM-SC-QN.svg)](https://github.com/engcang/FAST-LIO-SAM-SC-QN)|
|Faster_LIO_SAM: Faster-Lio + Lio-SAM|[![Github stars](https://img.shields.io/github/stars/GDUT-Kyle/faster_lio_sam.svg)](https://github.com/GDUT-Kyle/faster_lio_sam)|
|IG-LIO + LIO-SAM|[![Github stars](https://img.shields.io/github/stars/liangheming/iG-LIO_SAM_LC.svg)](https://github.com/liangheming/iG-LIO_SAM_LC)</br>[![Github stars](https://img.shields.io/github/stars/INIF-FISH/IG_LIO_SLAM.svg)](https://github.com/INIF-FISH/IG_LIO_SLAM)|
|LeGO-LOAM + BoW3D|[![Github stars](https://img.shields.io/github/stars/chengwei0427/BoW3D-LeGO-LOAM.svg)](https://github.com/chengwei0427/BoW3D-LeGO-LOAM)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>



### Evaluation
|Summary|Repository|
|-|-|
|evo: Python package for the evaluation of odometry and SLAM|[![Github stars](https://img.shields.io/github/stars/MichaelGrupp/evo.svg)](https://github.com/MichaelGrupp/evo)|
|DynamicMap_Benchmark|[![Github stars](https://img.shields.io/github/stars/KTH-RPL/DynamicMap_Benchmark.svg)](https://github.com/KTH-RPL/DynamicMap_Benchmark)|
|Cloud Map Evaluation|[![Github stars](https://img.shields.io/github/stars/JokerJohn/Cloud_Map_Evaluation.svg)](https://github.com/JokerJohn/Cloud_Map_Evaluation)|
<p align="right">[<a href="#table-of-contents">back to table</a>]</p>
</br>

|Year|Venue|Paper Title|Repository|
|:-:|:-:|-|-|
|23|`ITSC`|[A Dynamic Points Removal Benchmark in Point Cloud Maps](https://arxiv.org/abs/2307.07260)|[![Github stars](https://img.shields.io/github/stars/KTH-RPL/DynamicMap_Benchmark.svg)](https://github.com/KTH-RPL/DynamicMap_Benchmark)|

|?|`?`|[?](?)|[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

|?|`?`|[?](?)|[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|




||[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

||[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

||[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

||[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|

||[![Github stars](https://img.shields.io/github/stars/link.svg)](https://github.com/link)|






<!-- 
<style>
  details {
    font-size: 1.5em;
  }
  summary {
    cursor: pointer;
    font-weight: bold;
  }
</style>

<details>
<summary>클릭하여 펼치기</summary>
</details> -->