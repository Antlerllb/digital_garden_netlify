---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Minimal (or none) textual context/"}
---

[[5-Attachment/ZoteroNote/@NoClues_2023_Pitarch\|@NoClues_2023_Pitarch]] #code 
# 1 文字介绍
- the impact of long/short prompting for LRC #gap 
- hypothesis
	- commonly used PTLMs already encode enough linguistic knowledge
		- allow the use of minimal (or none) textual context for some linguistically motivated tasks
		- In such cases, very simple prompts work almost as well or even better than hand-crafted, more complex verbalizations
- Reducing the need of complex prompting
	- notably reduces the need of human effort and the need for data pre-processing, and favors techniques that are language neutral
	- since they do not rely on syntactic structures
- #contribution
	- We show empirically that SoTA results for LRC can be reached by providing very simple verbalizations of the data or even no verbalization at all (null prompting) when fine-tuning and testing a PTLM.
# 2 不同Minimal程度的Prompt模板
![In-context learning-20240215.png|400](/img/user/5-Attachment/Image/In-context%20learning-20240215.png)
# 3 实验结果
## 3.1 根据模型分类讨论
![In-context learning-20240215-1.png|400](/img/user/5-Attachment/Image/In-context%20learning-20240215-1.png)
## 3.2 根据词性分类讨论
![Minimal (or none) textual context-20240215.png|400](/img/user/5-Attachment/Image/Minimal%20(or%20none)%20textual%20context-20240215.png)