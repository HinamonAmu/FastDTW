# FastDTW
FastDTW algorithm
（1）Use the abstraction of the original data to complete the coarse-grained,
     where the coarse-grained data points are the mean values of the corresponding multiple points,and then iterate for many times:
     1/1->1/2->1/4->1/8...
（2）DTW algorithm is applied on the coarser granularity.
（3）The path obtained by (2) is further fine-grained,and on the basis of fine-grained,it expands the space by 1 or 2 granularity
     in all directions.
     the specific execution flow diagram of FastDTW is shown in figure 1:
     ...
     Fig.1  The four different resolutions evaluated during a complete run of the FastDTW algorithm.
     It is easy to see that the time complexity of FastDTW is O(N(8r+4)),which is close to O(N) when the granularity is small enough.
