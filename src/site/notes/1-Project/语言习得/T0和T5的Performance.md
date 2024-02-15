---
{"dg-publish":true,"permalink":"/1-Project/语言习得/T0和T5的Performance/"}
---

[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
# 1 模型
| Model | 来源 |
| ---- | ---- |
| T5-LM-Adapt models | https://huggingface.co/google/t5-xl-lm-adapt |
| T0 models | (Sanh et al., 2022) |
- Difference between T0 and T5
	- The two model groups have the same model architecture but different weights
	- T0 is trained to multi-task on the P3 meta-train set using T5-LM-Adapt as initialization.
# 2 报告结果
⋆ marks the best ICL method in each size group
▲ marks the best ﬁne-tuning method in each size group.
![FT vs ICL-20240214.png](/img/user/5-Attachment/Image/FT%20vs%20ICL-20240214.png)
结果好：FiD-ICL **outperforms** Concat-ICL and Ensemble-ICL in all three size groups.
结果没那么好：FiD-ICL (T5-LM XL) **narrows the performance gap** between ICL and T-Few to be 3%.

