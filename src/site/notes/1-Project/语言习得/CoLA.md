---
{"dg-publish":true,"permalink":"/1-Project/语言习得/CoLA/"}
---

# 1 介绍
[[5-Attachment/ZoteroNote/@BLiMPBenchmark_2020_Warstadt\|@BLiMPBenchmark_2020_Warstadt]]
- CoLA (Warstadt et al., 2019b)
- 内容
	- The most recent and comprehensive corpus
	- containing 10k sentences covering a wide variety of linguistic phenomena provided as examples in linguistics papers and books
- 设计初衷 #gap 
	- Although CoLA can provide evidence about phenomenon-specific knowledge of models, this method is limited by the need to train a **supervised classifier** on CoLA data prior to evaluation.
	- This is because CoLA is designed for binary acceptability classification, and there is no generally accepted method for obtaining binary acceptability predictions **from unsupervised models like LMs.**
# 2 和其他Benchmark的关系
[[5-Attachment/ZoteroNote/@BLiMPBenchmark_2020_Warstadt\|@BLiMPBenchmark_2020_Warstadt]]
体现该数据集的重要性
- GLUE (Wang et al., 2018)
	- CoLA, which is included in the GLUE benchmark
	- has been used to track advances in the sensitivity of reusable sentence encoding models to acceptability