---
{"dg-publish":true,"permalink":"/1-Project/语言习得/ICL 理解/"}
---

# 1 Construction of demonstrations
[[5-Attachment/ZoteroNote/@SelfICLZeroShot_2023_Chen\|@SelfICLZeroShot_2023_Chen]] Min et al. (2022b)
## 1.1 Four aspects
**Given** a set of k-shot demonstrations denoted as ${(x_1, y_1), …, (x_k, y_k)}$, where $x_i$ is the input text and $y_i$ is the label.
The ***input-label mapping***: whether xi is paired with a correct yi.
The ***input space***: the underlying distribution behind x1, …, xk.
The ***label space***: the possible label set inferred from y1, …, yk. (Input with instruction-like descriptions could also inform model of the label space.)
The ***pairing format***: the format representing the xi-yi pair.
## 1.2 Surprising finding
the ***input-label mapping*** is not a necessary criteria for successful ICL
# 2 Pseudo-inputs’ diversity
## 2.1 结论的setting
[[5-Attachment/ZoteroNote/@SelfICLZeroShot_2023_Chen\|@SelfICLZeroShot_2023_Chen]]
- Min et al. (2022b)
	- inputs are randomly sampled from the training set
- SELF-ICL (ours)
	- based on only one reference, i.e., the given test input
	- the generated pseudo-inputs are likely to be of great semantic similarity with that test input, and fail to capture the correct input space distribution
## 2.2 Copying effect -> hurt performance
- Min et al. (2022b)’s finding does not hold
- [[1-Project/语言习得/Copying effect\|Copying effect]]: models tend to copy the labels paired with inputs that are very similar to the test input
- With no guarantee for the correctness of SELF-ICL’s pseudo-labels, the copying effect would potentially hurt the ICL performance.
## 2.3 Increase the pseudo-inputs’ diversity
To mitigate the possible impact of copying effect, increasing the pseudo-inputs’ diversity is essential.
three different approaches for constructing pseudo-inputs:
(1) Batch inference, (2) Prompting with diversity hints, and (3) Prompt without diversity hints.