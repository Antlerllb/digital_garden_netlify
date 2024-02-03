---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/Token Prediction as Implicit Classification to Identify LLM-Generated Text/"}
---

# 1 Token Prediction as Implicit Classification to Identify LLM-Generated Text
## 1.1 Metadata
* Authors: [[Yutian Chen\|Yutian Chen]], [[Hao Kang\|Hao Kang]], [[Vivian Zhai\|Vivian Zhai]], [[Liangze Li\|Liangze Li]], [[Rita Singh\|Rita Singh]], [[Bhiksha Raj\|Bhiksha Raj]]
* Date: 2023-11-15
* Citation: 1
- Tags: #LLM
- Status: #Noted 
* Attachments: [arXiv Fulltext PDF](zotero://open-pdf/library/items/7RYF977A)
## 1.2 Abstract
This paper introduces a novel approach for identifying the possible large language models (LLMs) involved in text generation. Instead of adding an additional classification layer to a base LM, we reframe the classification task as a next-token prediction task and directly fine-tune the base LM to perform it. We utilize the Text-to-Text Transfer Transformer (T5) model as the backbone for our experiments. We compared our approach to the more direct approach of utilizing hidden states for classification. Evaluation shows the exceptional performance of our method in the text classification task, highlighting its simplicity and efficiency. Furthermore, interpretability studies on the features extracted by our model reveal its ability to differentiate distinctive writing styles among various LLMs even in the absence of an explicit classifier. We also collected a dataset named OpenLLMText, containing approximately 340k text samples from human and LLMs, including GPT3.5, PaLM, LLaMA, and GPT2.
# 2 子数据集
| 子数据集 | 来源 | 数量 |
| ---- | ---- | ---- |
| Human | OpenWebText，多主题的网页爬取数据， [[5-Attachment/Paper/The Pile An 800GB Dataset of Diverse Text for Language Modeling\|Pile]] 已涵盖涵盖 | 60k |
| GPT3.5 | 重述人类文本（OpenAI’s gpt-3.5-turbo API） | 60k |
| PaLM | 重述人类文本（text-bison-001 API） | 60k |
| LLaMA7B | 提供人类文本的前75 tokens，让模型补全 | 60k |
| GPT2-1B | [[5-Attachment/Paper/gpt-2-output-dataset\|gpt-2-output-dataset]] | 60k |
