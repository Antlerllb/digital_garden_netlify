---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/LLMDet A Third Party Large Language Models Generated Text Detection Tool/"}
---

# 1 LLMDet: A Third Party Large Language Models Generated Text Detection Tool
## 1.1 Metadata
* Authors: [[Kangxi Wu\|Kangxi Wu]], [[Liang Pang\|Liang Pang]], [[Huawei Shen\|Huawei Shen]], [[Xueqi Cheng\|Xueqi Cheng]], [[Tat-Seng Chua\|Tat-Seng Chua]]
* Date: 2023-11-03
* Citation: arXiv:2305.15004 [cs]
- Tags: 
- Status: #Noted
* Attachments: [Wu et al. - 2023 - LLMDet A Third Party Large Language Models Genera.pdf](zotero://open-pdf/library/items/WR3BB9RG)
## 1.2 Abstract
Generated texts from large language models (LLMs) are remarkably close to high-quality human-authored text, raising concerns about their potential misuse in spreading false information and academic misconduct. Consequently, there is an urgent need for a highly practical detection tool capable of accurately identifying the source of a given text. However, existing detection tools typically rely on access to LLMs and can only differentiate between machine-generated and human-authored text, failing to meet the requirements of fine-grained tracing, intermediary judgment, and rapid detection. Therefore, we propose LLMDet, a model-specific, secure, efficient, and extendable detection tool, that can source text from specific LLMs, such as GPT-2, OPT, LLaMA, and others. In LLMDet, we record the nexttoken probabilities of salient n-gram as features to calculate proxy perplexity for each LLM. By jointly analyzing the proxy perplexities of LLMs, we can determine the source of the generated text. Experimental results show that LLMDet yields impressive detection performance while ensuring speed and security, achieving 98.54% precision and about ×5.0 faster for recognizing human-authored text. Additionally, LLMDet can effortlessly extend its detection capabilities to a new open-source model. We will provide an open-source tool at https://github.com/TrustedLLM/LLMDet.
# 2 Perplexity
In LLMDet, we record the nexttoken probabilities of salient n-gram as features to calculate proxy perplexity for each LLM. 
![LLMDet A Third Party Large Language Models Generated Text Detection Tool-20240118.png|350](/img/user/5-Attachment/Image/LLMDet%20A%20Third%20Party%20Large%20Language%20Models%20Generated%20Text%20Detection%20Tool-20240118.png)
{ #8e5ef1}
