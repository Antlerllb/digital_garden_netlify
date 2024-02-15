---
{"dg-publish":true,"permalink":"/5-Attachment/ZoteroNote/@ZICLZeroShot_2023_Lyu/","title":"Z-ICL: Zero-Shot In-Context Learning with Pseudo-Demonstrations"}
---

# 1 Z-ICL: Zero-Shot In-Context Learning with Pseudo-Demonstrations
## 1.1 Link
- Url: https://aclanthology.org/2023.acl-long.129
- Item: [item](zotero://select/library/items/QBAU4IHL)
- File: [ZICLZeroShot_2023_Lyu.pdf](zotero://open-pdf/library/items/E57MXPK4)
## 1.2 Abstract
Although large language models can be prompted for both zero- and few-shot learning, performance drops significantly when no demonstrations are available. In this paper, we introduce Z-ICL, a new zero-shot method that closes the gap by constructing pseudo-demonstrations for a given test input using a raw text corpus. Concretely, pseudo-demonstrations are constructed by (1) finding the nearest neighbors to the test input from the corpus and pairing them with random task labels, and (2) applying a set of techniques to reduce the amount of direct copying the model does from the resulting demonstrations. Evaluation on nine classification datasets shows that Z-ICL outperforms previous zero-shot methods by a significant margin, and is on par with in-context learning with labeled training data in the few-shot setting. Overall, Z-ICL provides a significantly higher estimate of the zero-shot performance levels of a model, and supports future efforts to develop better pseudo-demonstrations that further improve zero-shot results.