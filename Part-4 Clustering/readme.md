Clustering

Clustering is basically a technique that groups similar data points such that the points in the same group are more similar to each other than the points in the other groups. The group of similar data points is called a Cluster.


K-Means Clustering

Kmeans algorithm is an iterative algorithm that tries to partition the dataset into Kpre-defined distinct non-overlapping subgroups (clusters) where each data point belongs to only one group. It tries to make the intra-cluster data points as similar as possible while also keeping the clusters as different (far) as possible. It assigns data points to a cluster such that the sum of the squared distance between the data points and the cluster’s centroid (arithmetic mean of all the data points that belong to that cluster) is at the minimum. The less variation we have within clusters, the more homogeneous (similar) the data points are within the same cluster.
Applications
kmeans algorithm is very popular and used in a variety of applications such as market segmentation, document clustering, image segmentation and image compression, etc. 

Hiericahial clustering

Hiericahial clustering is an algorithm that groups similar objects into groups called cluster. The endpoint is a set of cluster, where each cluster is distinct from each other, and the objects within each cluster are broadly similar to each other.
The basic algorithm:
    • Compute the proximity matrix
    • Let each data point be a cluster
    • Repeat: Merge the two closest clusters and update the proximity matrix
    • Until only a single cluster remains
      
A Dendrogram is a tree-like diagram that records the sequences of merges or splits.
      
