---
{"dg-publish":true,"permalink":"/1-Project/语言习得/FT vs ICL/"}
---

# 1 Performance
[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
- ICL performance typically falls short of FT-based methods (Liu et al., 2022)
- FT
	- FT-based approaches currently achieve state-of-the-art performance (Liu et al., 2022)
- 实例对比实验
	- [[1-Project/语言习得/T0和T5的Performance\|T0和T5的Performance]]
# 2 Efficiency
[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
- FT
	- require backpropagating and computing gradients over the full models, which can be prohibitive under memory and resource constraints.
- ICL
	- more efﬁcient at its “learning” stage: it only uses one forwardpass and does not require gradients at all.
	- less efﬁcient at inference stage: the concatenated examples can become overly long and induce excessive computational costs.
# 3 Perturbation
[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
- FT
	- the performance of ﬁne-tuning would be drastically worse when labels are incorrect
- ICL
	- Even with 100% wrong labels, little performance drop is observed with ICL models.
# 4 Paradigm shift
[[5-Attachment/ZoteroNote/@NoClues_2023_Pitarch\|@NoClues_2023_Pitarch]]
More recently, the “pre-train, fine-tune” procedure is shifting in NLP tasks towards the “pre-train, prompt, and predict” paradigm (Liu et al., 2023)