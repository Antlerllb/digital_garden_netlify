---
{"dg-publish":true,"permalink":"/5-Attachment/ZoteroNote/@SelfICLZeroShot_2023_Chen/","title":"Self-ICL: Zero-Shot In-Context Learning with Self-Generated Demonstrations"}
---

# 1 Self-ICL: Zero-Shot In-Context Learning with Self-Generated Demonstrations
## 1.1 Link
- File: [SelfICLZeroShot_2023_Chen.pdf](zotero://open-pdf/library/items/RV6Y9LFZ)
- Url: https://aclanthology.org/2023.emnlp-main.968
- Item: [item](zotero://select/library/items/JA5WB8KT)
## 1.2 Abstract
Large language models (LLMs) have exhibited striking in-context learning (ICL) ability to adapt to target tasks with a few input-output demonstrations. For better ICL, different methods are proposed to select representative demonstrations from existing training corpora. However, such settings are not aligned with real-world practices, as end-users usually query LMs without access to demonstration pools. In this work, we introduce Self-ICL—a simple framework which bootstraps LMs' intrinsic capabilities to perform zero-shot ICL. Given a test input, Self-ICL first prompts the model to generate pseudo-inputs. Next, the model predicts pseudo-labels for the pseudo-inputs via zero-shot prompting. Finally, we perform ICL for the test input with the pseudo-input-label pairs as demonstrations. Evaluation on 23 BIG-Bench Hard tasks shows Self-ICL outperforms zero-shot baselines on both average accuracy and head-to-head comparison. Moreover, with zero-shot chain-of-thought, Self-ICL achieves results comparable to using real demonstrations. Additionally, we conduct a range of analyses to validate Self-ICL's effectiveness and provide insights for its behaviors under different settings.