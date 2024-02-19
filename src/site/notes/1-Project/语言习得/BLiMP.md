---
{"dg-publish":true,"permalink":"/1-Project/语言习得/BLiMP/"}
---

# 1 理念
- Instead of
	- Instead of prompting for a acceptability judgments on individual sentences, as is most commonly done for human subjects
- they present #使用LM的原因
	- they present an LM with two sentences that only differ in one structural or lexical property. For a given minimal pair $m_i$ consisting of an acceptable sentence $s_{i,1}$ and an unacceptable sentence $s_{i,2}$,
	- **if an LM evaluates $P(s_{i,1}) > P(s_{i,2})$, then the model has succeeded on $m_i$.**
- 或许可以尝试 #gap
	- 把修改过的几次作业用相似度匹配，几次作业只有一点差异，弄成一个数据集？
# 2 语言现象
[[5-Attachment/ZoteroNote/@BLiMPBenchmark_2020_Warstadt\|@BLiMPBenchmark_2020_Warstadt]]
![BLiMP-20240218.png](/img/user/5-Attachment/Image/BLiMP-20240218.png)
# 3 实验结果
[[5-Attachment/ZoteroNote/@BLiMPBenchmark_2020_Warstadt\|@BLiMPBenchmark_2020_Warstadt]]
## 3.1 主实验
![BLiMP-20240218-1.png](/img/user/5-Attachment/Image/BLiMP-20240218-1.png)
## 3.2 控制变量
句子长度、PPL、接受对数概率、模型置信度、参数大小
![BLiMP-20240218-2.png|450](/img/user/5-Attachment/Image/BLiMP-20240218-2.png)
![BLiMP-20240218-4.png|450](/img/user/5-Attachment/Image/BLiMP-20240218-4.png)
![BLiMP-20240218-5.png|400](/img/user/5-Attachment/Image/BLiMP-20240218-5.png)
## 3.3 没看懂
![BLiMP-20240218-3.png](/img/user/5-Attachment/Image/BLiMP-20240218-3.png)