---
{"dg-publish":true,"permalink":"/5-Attachment/ZoteroNote/@WinoDictProbing_2023_Eisenschlos/","title":"WinoDict: Probing language models for in-context word acquisition"}
---

# 1 WinoDict: Probing language models for in-context word acquisition
## 1.1 Link
- Url: https://aclanthology.org/2023.eacl-main.7
- Item: [item](zotero://select/library/items/L97ZL5HB)
- File: [WinoDictProbing_2023_Eisenschlos.pdf](zotero://open-pdf/library/items/WF8LWE5X)
## 1.2 Abstract
We introduce a new in-context learning paradigm to measure Large Language Models' (LLMs) ability to learn novel words during inference. In particular, we rewrite Winograd-style co-reference resolution problems by replacing the key concept word with a synthetic but plausible word that the model must understand to complete the task. Solving this task requires the model to make use of the dictionary definition of the new word given in the prompt. This benchmark addresses word acquisition, one important aspect of the diachronic degradation known to afflict LLMs. As LLMs are frozen in time at the moment they are trained, they are normally unable to reflect the way language changes over time. We show that the accuracy of LLMs compared to the original Winograd tasks decreases radically in our benchmark, thus identifying a limitation of current models and providing a benchmark to measure future improvements in LLMs ability to do in-context learning.
# 2 Exp
![@WinoDictProbing_2023_Eisenschlos-20240212.png](/img/user/5-Attachment/Image/@WinoDictProbing_2023_Eisenschlos-20240212.png)
![@WinoDictProbing_2023_Eisenschlos-20240212-1.png|325](/img/user/5-Attachment/Image/@WinoDictProbing_2023_Eisenschlos-20240212-1.png)
![@WinoDictProbing_2023_Eisenschlos-20240212-2.png|350](/img/user/5-Attachment/Image/@WinoDictProbing_2023_Eisenschlos-20240212-2.png)
# 3 Model and Prompt
![@WinoDictProbing_2023_Eisenschlos-20240213.png|350](/img/user/5-Attachment/Image/@WinoDictProbing_2023_Eisenschlos-20240213.png)![@WinoDictProbing_2023_Eisenschlos-20240213-1.png|350](/img/user/5-Attachment/Image/@WinoDictProbing_2023_Eisenschlos-20240213-1.png)