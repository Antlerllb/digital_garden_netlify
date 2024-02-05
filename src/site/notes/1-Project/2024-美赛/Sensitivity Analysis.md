---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Sensitivity Analysis/"}
---

[[1-Project/2024-美赛/敏感性分析图\|敏感性分析图]]

# 1 其他文本
[[5-Attachment/ZoteroNote/@HierarchicalApproach_2024_dePaulaOliveira\|@HierarchicalApproach_2024_dePaulaOliveira]]
transparent approach. When updating weights at the end of a season, it is crucial to document the changes 
and consider their impact on score comparability. Practitioners could maintain a version history of weights used 
each season, allowing for historical ON score re-calibrations when necessary. Furthermore, it may be beneficial 
to perform sensitivity analyses to understand the extent of changes due to weight updates. This practice can 
provide insights into whether re-calibrations significantly alter the interpretation of an athlete’s performance 
across seasons. These steps will ensure that practitioners are equipped to handle the potential challenges of weight 
updating in longitudinal analyses.

[[5-Attachment/ZoteroNote/@LinkingRotation_2017_Damme\|@LinkingRotation_2017_Damme]]
Parameter sensitivity
We need to consider only dribbles where the quality of the model fit is directly impacted by the value of the 
parameters. In other words, for each parameter under consideration we filter out dribbles where significant variations on the value of that parameter did not translate into significant variations in the model error.
Sensitivity study is performed by perturbing one of the parameters (say βa ) by a given percent value ±ρ while 
leaving the others fixed, then simulating the new attacker and defender trajectory using these new set of parameters with our model, and evaluating the new error. We then deem this dribble to be sensitive with respect to βa 
if the relative change in error is at least |ρ| . The results derived in “Analysis of parameter distributions” section are 
evaluated with ρ =±25% , for a grand total of (293, 274, 535, 522) dribbles for (βa, βd, αa/τa, αd/τd) (since for 
each parameter analysis we only use dribbles that are sensitive to that parameter). Similarly, the results in Section 
“Quantifying the Impact of Parameter Variations on Dribble Quality” are evaluated with dribbles that are sensitive 
to at least one of the ρ =±10%, ±25%, ±50% , leaving us with (377, 359, 541, 531) dribbles for (βa, βd, αa, αd).

