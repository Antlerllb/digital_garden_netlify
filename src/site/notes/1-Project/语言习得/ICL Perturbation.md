---
{"dg-publish":true,"permalink":"/1-Project/语言习得/ICL Perturbation/"}
---

[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
# 1 概念
- (Min et al., 2022c)
	- ICL models do not rely on input-label mapping as much as expected, casting doubts on the effectiveness of ICL
- (Wei et al., 2023)
	- Even with 100% wrong labels, little performance drop is observed with ICL models.
	- extremely large LMs can override semantic priors when these perturbations are applied
- Replicate a set of diagnostic experiments(Min et al., 2022c)
	- perturbing the in-context examples
	- (e.g., using fewer/more shots, replacing correct labels with random labels).
# 2 实验
| 实验设置 | 解释 |
| ---- | ---- |
| No Perturbation |  |
| No Input | remove the inputs but keep the labels |
| Random Label | randomly select one of the valid options as the output |
| Wrong Label | randomly select one of the wrong options |
| No Label | remove the labels but keep the inputs |
Note that all four perturbations can be applied to ICL models, but only (3)(4) can be applied to FT-based method.
# 3 对比的模型
examine both large-size (800M) and XL-size (3B) models, selecting the better model between T5-LM and T0 initialization.
# 4 结果
- 总体 Observation
	- All ICL methods are still rather insensitive to perturbations
	- FiDICL suffers from No Label perturbation more than the other two methods.
- T0-FT method
	- No Perturbation > Random Label > Wrong Label
- ICL: Concat, T5-LM-FiD, T0-Ensemble
	- No Label效果最差：may be capturing more information from the labels
	- struggle to learn from input-label mapping, despite their improved performance over Concat-ICL
	- Enabling ICL models to learn effectively and faithfully from examples remains a challenging problem. #gap
![ICL Perturbation-20240214.png|450](/img/user/5-Attachment/Image/ICL%20Perturbation-20240214.png)
