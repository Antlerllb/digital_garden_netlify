---
{"dg-publish":true,"permalink":"/1-Project/语言习得/使用LM的原因/"}
---

# 1 使用LM评估句对的原因
[[5-Attachment/ZoteroNote/@BLiMPBenchmark_2020_Warstadt\|@BLiMPBenchmark_2020_Warstadt]]
- however
	- the use of supervision prevents making strong conclusions about the sentence encoding component,
	- since it is not possible to distinguish what the encoder knows from what is learned through supervised training on acceptability data
- evaluate
	- whether the LM assigns a higher probability to the acceptable sentence in each minimal pair to determine which grammatical distinctions LMs are sensitive to.
- **model’s linguistic knowledge**
	- allows us to compare models in a fine-grained way
- LM probability
	- LM probability of a sentence can only serve as **a proxy for acceptability** if confounding factors impacting a sentence’s probability such as length and lexical content are controlled for.
	- [[1-Project/语言习得/BLiMP#1 理念\|BLiMP#1 理念]]
可能可以改成：模型的语言知识有利于对比人的语言知识
# 2 之前没人使用in-context
[[1-Project/语言习得/CoLA#1 介绍\|CoLA#1 介绍]]
将LM改为in-context
