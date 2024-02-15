---
{"dg-publish":true,"permalink":"/5-Attachment/ZoteroNote/@GPTREIncontext_2023_Wan/","title":"GPT-RE: In-context Learning for Relation Extraction using Large Language Models"}
---

# 1 GPT-RE: In-context Learning for Relation Extraction using Large Language Models
## 1.1 Link
- Url: https://aclanthology.org/2023.emnlp-main.214
- Item: [item](zotero://select/library/items/EUN263Q9)
- File: [GPTREIncontext_2023_Wan.pdf](zotero://open-pdf/library/items/D5L27VBD)
## 1.2 Abstract
In spite of the potential for ground-breaking achievements offered by large language models (LLMs) (e.g., GPT-3) via in-context learning (ICL), they still lag significantly behind fully-supervised baselines (e.g., fine-tuned BERT) in relation extraction (RE). This is due to the two major shortcomings of ICL for RE: (1) low relevance regarding entity and relation in existing sentence-level demonstration retrieval approaches for ICL; and (2) the lack of explaining input-label mappings of demonstrations leading to poor ICL effectiveness. In this paper, we propose GPT-RE to successfully address the aforementioned issues by (1) incorporating task-aware representations in demonstration retrieval; and (2) enriching the demonstrations with gold label-induced reasoning logic. We evaluate GPT-RE on four widely-used RE datasets, and observe that GPT-RE achieves improvements over not only existing GPT-3 baselines, but also fully-supervised baselines as in Figure 1. Specifically, GPT-RE achieves SOTA performances on the Semeval and SciERC datasets, and competitive performances on the TACRED and ACE05 datasets. Additionally, a critical issue of LLMs revealed by previous work, the strong inclination to wrongly classify NULL examples into other pre-defined labels, is substantially alleviated by our method. We show an empirical analysis.