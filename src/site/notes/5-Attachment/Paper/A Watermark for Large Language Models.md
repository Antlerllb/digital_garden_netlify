---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/A Watermark for Large Language Models/"}
---

# 1 A Watermark for Large Language Models
## 1.1 Metadata
* Authors: [[John Kirchenbauer\|John Kirchenbauer]], [[Jonas Geiping\|Jonas Geiping]], [[Yuxin Wen\|Yuxin Wen]], [[Jonathan Katz\|Jonathan Katz]], [[Ian Miers\|Ian Miers]], [[Tom Goldstein\|Tom Goldstein]]
* Date: 2023-06-06
* Citation: OPT-2.7B
- Tags: 
- Status: #Todo
* Attachments: [Kirchenbauer et al. - 2023 - A Watermark for Large Language Models.pdf](zotero://open-pdf/library/items/NGQJET7D)
## 1.2 Abstract
Potential harms of large language models can be mitigated by watermarking model output, i.e., embedding signals into generated text that are invisible to humans but algorithmically detectable from a short span of tokens. We propose a watermarking framework for proprietary language models. The watermark can be embedded with negligible impact on text quality, and can be detected using an efficient opensource algorithm without access to the language model API or parameters. The watermark works by selecting a randomized set of “green” tokens before a word is generated, and then softly promoting use of green tokens during sampling. We propose a statistical test for detecting the watermark with interpretable p-values, and derive an informationtheoretic framework for analyzing the sensitivity of the watermark. We test the watermark using a multi-billion parameter model from the Open Pretrained Transformer (OPT) family, and discuss robustness and security.
# 2 Perplexity{ #ce4127}


To compute perplexity, the larger, Oracle Language Model is fed the original prompt as input, as described in the main body, and perplexity is computed via taking the exponential of the average token-wise loss according to the oracle’s next token distribution at every output index. Note that loss is computed for only the generated tokens produced by either a watermarked or non-watermarked model.
{ #9addc7}
