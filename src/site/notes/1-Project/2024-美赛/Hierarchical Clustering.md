---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Hierarchical Clustering/"}
---

Hierarchical clustering involves measuring the similarity (or dissimilarity) between pairs of rows and columns and forming a hierarchical tree-like structure, known as a dendrogram. The process starts by computing a correlation distance between each pair of rows and columns. These distances are then used to build a hierarchical tree, where similar rows or columns are joined together based on the average linkage.

Figure: Hierarchical Clustering For Match Status And Player Actions
[[1-Project/2024-美赛/变量聚类图\|变量聚类图]]

Considering the high correlation coefficient of 0.97 between the variables p1_points_won and p2_points_won, it is evident that these two features are likely to convey nearly identical information. By eliminating redundant features, the model can be streamlined, potentially improving its interpretability and generalization to new data.
The hierarchical clustering results reveal interesting patterns in the tennis match data. There is a strong correlation between player 1 approaching the net and winning the point. This suggests that net play is an effective strategy for player 1. There is a strong correlation between player 2 having a break point opportunity and missing it. This implies that missed break point opportunities are closely associated with player 2.
