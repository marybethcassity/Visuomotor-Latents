# BAMS
## get_bams_embeddings
This notebook takes a trained BAMS (https://multiscale-behavior.github.io/) model and pose data (DeepLabCut '.csvs') and returns features for behavorial classification/ studies of dynamic movement. 
The embeddings are shape (n samples, n frames per sample, n bams features) where samples = DLC '.csvs'. Frame level embeddings, where each frame from the pose 
csvs is its own datapoint, are shape (n samples * n frames per sample, n bams features). These frame level data points are embedded into a 3D space using UMAP and clustered in the UMAP 
space using DBSCAN. Sequence level embeddings can also be computed by averaging each feature over the frames of the sample and are shape (n samples, n bams features).

Created by:

Mary Beth Cassity @ mary.beth.cassity@cornell.edu

Sarvestani Lab, Cornell University

Code last updated: 

9/13/2024

![Visuomotor-Latents](https://github.com/user-attachments/assets/d74607bf-f8ba-425c-aa96-7d582f836345)
