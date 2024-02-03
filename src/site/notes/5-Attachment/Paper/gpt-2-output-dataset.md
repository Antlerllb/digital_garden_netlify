---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/gpt-2-output-dataset/"}
---

- 链接
	- [openai/gpt-2-output-dataset: Dataset of GPT-2 outputs for research in detection, biases, and more](https://github.com/openai/gpt-2-output-dataset)
- 生成方式
	- 用在WebText上训练的GPT-2模型生成数据
- 数据集组成
	- 250K documents from the WebText test set
	- 250K random samples (temperature 1, no truncation)
	- 250K samples generated with Top-K 40 truncation