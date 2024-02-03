---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/SeqXGPT Sentence-Level AI-Generated Text Detection/"}
---

# 1 SeqXGPT: Sentence-Level AI-Generated Text Detection
## 1.1 Metadata
* Authors: [[Pengyu Wang\|Pengyu Wang]], [[Linyang Li\|Linyang Li]], [[Ke Ren\|Ke Ren]], [[Botian Jiang\|Botian Jiang]], [[Dong Zhang\|Dong Zhang]], [[Xipeng Qiu\|Xipeng Qiu]]
* Date: 2023-12-14
* Citation: arXiv:2310.08903 [cs]
- Tags: 
- Status: #Noted 
* Attachments: [Wang et al. - 2023 - SeqXGPT Sentence-Level AI-Generated Text Detectio.pdf](zotero://open-pdf/library/items/I64LQ335)
## 1.2 Abstract
Widely applied large language models (LLMs) can generate human-like content, raising concerns about the abuse of LLMs. Therefore, it is important to build strong AI-generated text (AIGT) detectors. Current works only consider document-level AIGT detection, therefore, in this paper, we first introduce a sentence-level detection challenge by synthesizing a dataset that contains documents that are polished with LLMs, that is, the documents contain sentences written by humans and sentences modified by LLMs. Then we propose \textbf{Seq}uence \textbf{X} (Check) \textbf{GPT}, a novel method that utilizes log probability lists from white-box LLMs as features for sentence-level AIGT detection. These features are composed like \textit{waves} in speech processing and cannot be studied by LLMs. Therefore, we build SeqXGPT based on convolution and self-attention networks. We test it in both sentence and document-level detection challenges. Experimental results show that previous methods struggle in solving sentence-level AIGT detection, while our method not only significantly surpasses baseline methods in both sentence and document-level detection challenges but also exhibits strong generalization capabilities.
# 2 Perplexity
We use four open-source (L)LMs to construct our SeqXGPT-Bench: GPT2-xl (1.5B), GPT-Neo (2.7B), GPT-J (6B) and LLaMA (7B). These models are also utilized to extract perplexity lists, which are used to construct the original features of our SeqXGPT and the contrastive features for Sniffer.
{ #743f33}
