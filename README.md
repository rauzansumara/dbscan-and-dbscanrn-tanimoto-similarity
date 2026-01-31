## DBSCAN and DBSCANRN Tanimoto Similarity

### DAMI project
Task:
1. Implementation of DBSCAN-Tanimoto Similarity
2. Implementation of DBSCANRN-Tanimoto Similarity (Naive & Opt)
3. Clustering quality measures: Purity, Rand, Davies−Bouldin and Silhouette Coefficient 

Clustering is one of the most important tasks of both artificial intelligence and data mining. That is a way to group a set of data points in a way that similar data points are grouped together. There are different approaches and algorithms to perform clustering tasks which is of them is algorithms based on density clustering. Based on discussed in the lecture, we will implement algorithms of Density-Based Spatial Clustering of Applications with Noise (DBSCAN) and Density-based spatial clustering using reverse nearest neighbors (DBSCRN). 

However, noted during project consultations, there are some inconsistencies in the paper presenting the pseudo-code of the DBSCRN algorithm [1](https://arxiv.org/abs/1811.07615). For this reason, we will implement some modification of DBSCRN (which will be called DBSCANRN) instead of DBSCRN. In DBSCANRN, we will keep core point and non-core points definitions as given in the pseudo-code of DBSCRN. Namely, a point is considered as a DBSCRN (and by this DBSCANRN) non-core point if the number of their reverse k-nearest neighbors is less than k (lines 2-3 in the DBSCRN pseudo-code). Otherwise, it is considered as a core point (line 5 in the DBSCRN pseudo-code). We implement DBSCANRN in a way similar to NBC, except that instead of adding k+-nearest neighbors of a core point to a cluster, its reverse k-nearest neighbors will be added to the cluster.