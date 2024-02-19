---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Z-ICL Pseudo/"}
---

[[5-Attachment/ZoteroNote/@ZICLZeroShot_2023_Lyu\|@ZICLZeroShot_2023_Lyu]] #code
# 1 理念
- Min et al. (2022)
	- ICL benefits mainly from the correct distribution of the inputs and the labels rather than the input-label correspondence.
- introduces a better zero-shot method
	- forming pseudo-demonstrations that are proxies of the input distribution and the label space
- We similarly use nearest neighbor search to retrieve sentences close to the test input, but are the first to
	- 这句话前文的related work见[[1-Project/语言习得/Retrieval-based Demonstrations\|Retrieval-based Demonstrations]]
	- (1) retrieve from a raw text corpus, in contrast to prior work that uses labeled or unlabeled training data collected for the task
	- (2) more closely study the connection between nearest neighbor inputs and random labels, through our copying effect hypothesis.
# 2 假设：Copying Effect
[[1-Project/语言习得/Copying effect\|Copying effect]]
Copying Effect需要被reduce
# 3 二分类例子
目标：making a prediction between great and terrible
参数：近邻 k = 3
![Zero-shot Pseudo-Demonstrations-20240215.png|450](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215.png)  
# 4 代码总逻辑
(1) finding the nearest neighbors to the test input from the corpus and pairing them with random task labels
(2) applying a set of techniques to reduce the amount of direct copying the model does from the resulting demonstrations.
![Zero-shot Pseudo-Demonstrations-20240215-1.png](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215-1.png)
# 5 对比其他工作
![Zero-shot Pseudo-Demonstrations-20240215-2.png|475](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215-2.png)
# 6 实验设置
## 6.1 模型
| Model | Params | Refer |
| ---- | ---- | ---- |
| GPT-J | 6B | (Wang and Komatsuzaki, 2021) |
| GPT-NeoX | 20B | (Black et al., 2022) |
| GPT-3 | 175B | (Brown et al., 2020) |
## 6.2 推断
two inference methods: 
- direct (a regular inference used in Brown et al. (2020))
- channel (Min et al., 2021)
# 7 实验结果
## 7.1 主实验
**Covered/not covered** by C indicates whether or not the domain of the dataset is covered by our text corpus.
Z-ICL is **significantly better than** previous zero-shot (No-demos) on all datasets, and is on par with ICL-gold on datasets covered by C.
![Zero-shot Pseudo-Demonstrations-20240215-3.png](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215-3.png)
## 7.2 Effect of the retrieval method
![Zero-shot Pseudo-Demonstrations-20240215-4.png|425](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215-4.png)
## 7.3 Effect of synonyms labeling
![Zero-shot Pseudo-Demonstrations-20240215-5.png|425](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215-5.png)
## 7.4 Effect of the size of the corpus
Because there are less sentences that are sufficiently close to the test input when the corpus is smaller, thus the ***relevance*** of the nearest neighbors and the test input drops.
This trend is clearer on the datasets covered by C than on the datasets not covered by C.
![Zero-shot Pseudo-Demonstrations-20240215-6.png](/img/user/5-Attachment/Image/Zero-shot%20Pseudo-Demonstrations-20240215-6.png)

