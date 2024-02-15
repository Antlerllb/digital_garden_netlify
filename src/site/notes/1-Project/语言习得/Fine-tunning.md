---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Fine-tunning/"}
---

# 1 Fine-tunning
[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
- (Zhang et al., 2021)
	- initializing a model with pre-trained weights and optimizing it based on a few examples
	- yields strong performance on a wide range of NLP tasks
- (Schick and Schütze, 2021; Gao et al., 2021)
	- be further improved by incorporating prompts and demonstrations in the input
- (Liu et al., 2022)
	- parameter-efﬁcient ﬁne-tuning methods can be applied to improve memory and storage costs
# 2 Reformulate into different NLP tasks
[[5-Attachment/ZoteroNote/@ReformulatingNLP_2023_Gkoumas\|@ReformulatingNLP_2023_Gkoumas]]
During fine-tuning emphasis is placed on strategies for reformulating the classification task into different NLP tasks.
- Standard Fine-tuning
- Multitask Fine-tuning with MLM
	- L multitask−MLM−separately
	- L multitask−MLM−joint
- Entailment-based Fine-tuning
- Prompt-based Learning
	- Standard Prompt-based
	- Prompt-based with Demonstration Examples
	- Prompt-based with Inverse Learning Objective
- Random Rate