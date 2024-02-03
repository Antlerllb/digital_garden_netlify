---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/OUTFOX LLM-generated Essay Detection through In-context Learning with Adversarially Generated Examples/"}
---

# 1 OUTFOX: LLM-generated Essay Detection through In-context Learning with Adversarially Generated Examples
## 1.1 Metadata
* Authors: [[Ryuto Koike\|Ryuto Koike]], [[Masahiro Kaneko\|Masahiro Kaneko]], [[Naoaki Okazaki\|Naoaki Okazaki]]
* Date: 2023-09-04
* Citation: 3
- Tags: 
- Status: #Noted
* Attachments: [arXiv Fulltext PDF](zotero://open-pdf/library/items/GS5AM9CL)
## 1.2 Abstract
Large Language Models (LLMs) have achieved human-level fluency in text generation, making it difficult to distinguish between human-written and LLM-generated texts. This poses a growing risk of misuse of LLMs and demands the development of detectors to identify LLM-generated texts. However, existing detectors lack robustness against attacks: they degrade detection accuracy by simply paraphrasing LLM-generated texts. Furthermore, a malicious user might attempt to deliberately evade the detectors based on detection results, but this has not been assumed in previous studies. In this paper, we propose OUTFOX, a framework that improves the robustness of LLM-generated-text detectors by allowing both the detector and the attacker to consider each other's output. In this framework, the attacker uses the detector's prediction labels as examples for in-context learning and adversarially generates essays that are harder to detect, while the detector uses the adversarially generated essays as examples for in-context learning to learn to detect essays from a strong attacker. Experiments in the domain of student essays show that the proposed detector improves the detection performance on the attacker-generated texts by up to +41.3 points in F1-score. Furthermore, the proposed detector shows a state-of-the-art detection performance: up to 96.9 points in F1-score, beating existing detectors on non-attacked texts. Finally, the proposed attacker drastically degrades the performance of detectors by up to -57.0 points F1-score, massively outperforming the baseline paraphrasing method for evading detection.
# 2 数据集
## 2.1 原文
We instruct three LMs to generate essays: ChatGPT(`gpt-3.5-turbo-0613`), GPT-3.5(`text-davinci-003`), and `FLAN-T5-XXL`. We split the dataset into three parts: train/validation/test with 14400/500/500 examples, respectively.
Additionally, `(train\|valid\|test)_contexts.pkl` includes the prompts used to generate essays in each set. We use these to compute the likelihood in statistical outlier detectors.
We also provide the attacked essays by our OUTFOX attacker in `data/chatgpt/test/test_outfox_attacks.pkl` and the attacked essays by DIPPER in `data/dipper/(chatgpt|text_davinci_003|flan_t5_xxl)/test_attacks.pkl`.
![OUTFOX LLM-generated Essay Detection through In-context Learning with Adversarially Generated Examples-20240115.png](/img/user/5-Attachment/Image/OUTFOX%20LLM-generated%20Essay%20Detection%20through%20In-context%20Learning%20with%20Adversarially%20Generated%20Examples-20240115.png)
## 2.2 整理
