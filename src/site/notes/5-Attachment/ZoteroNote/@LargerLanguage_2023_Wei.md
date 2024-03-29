---
{"dg-publish":true,"permalink":"/5-Attachment/ZoteroNote/@LargerLanguage_2023_Wei/","title":"Larger language models do in-context learning differently"}
---

# Larger language models do in-context learning differently
## Link
- File: [arXiv.org Snapshot](zotero://open-pdf/library/items/K4DPVY7B); [LargerLanguage_2023_Wei.pdf](zotero://open-pdf/library/items/TM5LC5LB)
- Url: http://arxiv.org/abs/2303.03846
- Item: [item](zotero://select/library/items/CJUWZLGY)
## Abstract
We study how in-context learning (ICL) in language models is affected by semantic priors versus input-label mappings. We investigate two setups-ICL with flipped labels and ICL with semantically-unrelated labels-across various model families (GPT-3, InstructGPT, Codex, PaLM, and Flan-PaLM). First, experiments on ICL with flipped labels show that overriding semantic priors is an emergent ability of model scale. While small language models ignore flipped labels presented in-context and thus rely primarily on semantic priors from pretraining, large models can override semantic priors when presented with in-context exemplars that contradict priors, despite the stronger semantic priors that larger models may hold. We next study semantically-unrelated label ICL (SUL-ICL), in which labels are semantically unrelated to their inputs (e.g., foo/bar instead of negative/positive), thereby forcing language models to learn the input-label mappings shown in in-context exemplars in order to perform the task. The ability to do SUL-ICL also emerges primarily with scale, and large-enough language models can even perform linear classification in a SUL-ICL setting. Finally, we evaluate instruction-tuned models and find that instruction tuning strengthens both the use of semantic priors and the capacity to learn input-label mappings, but more of the former.