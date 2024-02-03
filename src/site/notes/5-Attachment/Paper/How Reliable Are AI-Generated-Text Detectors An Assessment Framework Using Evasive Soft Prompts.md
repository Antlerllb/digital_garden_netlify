---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/How Reliable Are AI-Generated-Text Detectors An Assessment Framework Using Evasive Soft Prompts/"}
---

# 1 How Reliable Are AI-Generated-Text Detectors? An Assessment Framework Using Evasive Soft Prompts
## 1.1 Metadata
* Authors: [[Tharindu Kumarage\|Tharindu Kumarage]], [[Paras Sheth\|Paras Sheth]], [[Raha Moraffah\|Raha Moraffah]], [[Joshua Garland\|Joshua Garland]], [[Huan Liu\|Huan Liu]]
* Date: 2023-10-08
* Citation: arXiv:2310.05095 [cs]
- Tags: 
- Status: #Todo
* Attachments: [Kumarage et al. - 2023 - How Reliable Are AI-Generated-Text Detectors An A.pdf](zotero://open-pdf/library/items/83DH3NFD)
## 1.2 Abstract
In recent years, there has been a rapid proliferation of AI-generated text, primarily driven by the release of powerful pre-trained language models (PLMs). To address the issue of misuse associated with AI-generated text, various highperforming detectors have been developed, including the OpenAI detector and the Stanford DetectGPT. In our study, we ask how reliable these detectors are. We answer the question by designing a novel approach that can prompt any PLM to generate text that evades these highperforming detectors. The proposed approach suggests a universal evasive prompt, a novel type of soft prompt, which guides PLMs in producing "human-like" text that can mislead the detectors. The novel universal evasive prompt is achieved in two steps: First, we create an evasive soft prompt tailored to a specific PLM through prompt tuning; and then, we leverage the transferability of soft prompts to transfer the learned evasive soft prompt from one PLM to another. Employing multiple PLMs in various writing tasks, we conduct extensive experiments to evaluate the efficacy of the evasive soft prompts in their evasion of state-of-the-art detectors.
# 2 Perplexity
Table 3 presents the perplexity change values for each evasion technique in LLaMA generations. The perplexity is computed using an independent PLM, GPT2-XL (Radford et al., 2019). 
“GPT2-XL”后边的论文是Language models are unsupervised multitask learners。
{ #bca956}
