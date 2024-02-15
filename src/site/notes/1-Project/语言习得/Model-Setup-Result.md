---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Model-Setup-Result/"}
---

[[5-Attachment/ZoteroNote/@MindGap_2023_Stahl\|@MindGap_2023_Stahl]]

- Model
	- For classification, we fine-tune the language model DeBERTa (He et al., 2020) with 134M parameters, 12 layers, and a hidden size of 768 (microsoft/deberta-base) provided by Huggingface (Wolf et al., 2020). To quantify its learning success, we also report the results of a random classifier that makes random predictions and a majority classifier that always predicts the majority training class.
- Experimental Setup
	- We tune the training hyperparameters of DeBERTa in a grid-search manner using Raytune (Liaw et al., 2018). We explored numbers of epochs in {8, 16, 24} with learning rates in {10−6, 5 · 10−6, 10−5} and batch size 16. The best F1-score on the validation set was achieved by training for 24 epochs with a learning rate of 10−5.
- Results
	- Table 6 shows the classification results. The learning success of the DeBERTa model suggests the possibility of automating the task of enthymeme detection in learner arguments on our corpus. However, further improvements using more advanced approaches are expected and encouraged.

![Model-Setup-Result-20240209.png|450](/img/user/5-Attachment/Image/Model-Setup-Result-20240209.png)