---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Retrieval-based Demonstrations/"}
---

# 1 介绍
[[5-Attachment/ZoteroNote/@GPTREIncontext_2023_Wan\|@GPTREIncontext_2023_Wan]]
- dynamically selecting few-shot demonstrations for each test example, instead of utilizing a fixed set, leads to significant improvement in GPT-3 ICL (Liu et al., 2022b; Shin et al., 2021; Rubin et al., 2022)
[[5-Attachment/ZoteroNote/@UnifiedDemonstration_2023_Li\|@UnifiedDemonstration_2023_Li]]
- ICL has been shown highly dependent on the provided demonstrations and thus promotes the research of demonstration retrieval: given a test input, relevant examples are retrieved from the training set to serve as informative demonstrations for in-context learning.
[[5-Attachment/ZoteroNote/@ZICLZeroShot_2023_Lyu\|@ZICLZeroShot_2023_Lyu]]
- in the setting where large training data is available, choosing demonstration examples that are close to the test input significantly helps ICL
# 2 Related work
[[5-Attachment/ZoteroNote/@ZICLZeroShot_2023_Lyu\|@ZICLZeroShot_2023_Lyu]]
- Liu et al. (2021)
	- retrieves the nearest training examples to the test input using a sentence encoder, either unsupervised or supervised.
- Rubin et al. (2021)
	- trains a retrieval system to choose examples that improve ICL.
- Liu et al. (2022)
	- retrieves the nearest neighbors from unlabeled training data, assigns estimated labels, and uses them for ICL.