---
title: "Cluster Analysis"
output: html_notebook
editor_options: 
  chunk_output_type: inline
---


### Optimal Number of Clusters

According to the results of the three testing methods for optimal number of clusters - within sum of squares, average silhouette width and gap statistics - I choose to work with 9 clusters. 
According to within sum of squares method, 5 or 6 clusters seem fair for both periods. Meanwhile, the average silhouette width method gives us 2 clusters for the analysis. However, having 2 clusters would not account for enough variation within the Egyptian public opinion. The next nearest number of cluster that has similar average silhouette width is 6. Lastly, according to the gap statistics method, cluster 7 or 9 is the most optimal. I pick 9 clusters, which seem to work well according to all other methods.  

![](cluster.png)


### Prediction


![](t1.png)  

![](t2.png)


### PCA

Since PCA1 and PCA2 only explain 38% of the data, the vizualization would not be as useful.  


![](pca.png)  
