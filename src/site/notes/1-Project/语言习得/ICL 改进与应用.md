---
{"dg-publish":true,"permalink":"/1-Project/语言习得/ICL 改进与应用/"}
---

# 1 未分类的
[[5-Attachment/ZoteroNote/@FiDICLFusioninDecoder_2023_Ye\|@FiDICLFusioninDecoder_2023_Ye]]
- off the shelf (i.e., without any gradient update)
	- achieve competitive performance.
	- GPT-3 (Brown et al., 2020)
	- PaLM (Chowdhery et al., 2022)
- Smaller models
	- can be metatrained to obtain this capability (Chen et al., 2022; Min et al., 2022b)

[[5-Attachment/ZoteroNote/@FewshotIncontext_2023_Li\|@FewshotIncontext_2023_Li]]
- Empirically
	- Min et al. (2022)
		- the effectiveness of constructing prompts using an input-label pairing format
	- Liu et al. (2021)
		- experiment with the number of examples provided, as well the idea of retrieving relevant examples to a test input to construct the prompt with
	- Lampinen et al. (2022)
		- suggests that incorporating explanatory task instructions in context can improve performance

[[5-Attachment/ZoteroNote/@GPTREIncontext_2023_Wan\|@GPTREIncontext_2023_Wan]]
- 相关应用
	- solving math problems, commonsense reasoning, text classification, fact retrieval, natural language inference, and semantic parsing (Brown et al., 2020; Min et al., 2022b; Zhao et al., 2021; Liu et al., 2022b; Shin et al., 2021)
- Related work
	- various aspects to effectively utilize the advantages of GPT-3
		- prompt design (Perez et al., 2021) for proper input
		- coherence calibration (Malkin et al., 2022) for tackling the diverse generated output
	- locates in the demonstration part
		- ordered prompts (Lu et al., 2022)
		- retrieval-based demonstrations (Rubin et al., 2022; Liu et al., 2022b; Shin et al., 2021)

[[5-Attachment/ZoteroNote/@LearningIncontext_2023_Chen\|@LearningIncontext_2023_Chen]]
- Related work
	- enhance in-context learning by selecting valuable demonstrations (Liu et al., 2021; Rubin et al., 2022),
	- optimizing the order of demonstrations (Lu et al., 2022a)
	- calibrating output distributions (Zhao et al., 2021)
	- replicate in-context learning in smaller models (Min et al., 2022a; Chen et al., 2022b).
	- attempt to replicate incontext learning using smaller models (Min et al., 2022b; Chan et al., 2022)
	- there are efforts to understand the underlying mechanisms (Akyürek et al., 2022) of in-context learning which suggest that it can be compared to a metafunction and facilitate implicit fine-tuning (Dai et al., 2022; von Oswald et al., 2022)
# 2 Zero-shot
[[5-Attachment/ZoteroNote/@ZICLZeroShot_2023_Lyu\|@ZICLZeroShot_2023_Lyu]] #zero-shot
- Reynolds and McDonell (2021)
	- ICL mainly functions by activating the LM’s ability obtained during pretraining, and that the LM can achieve significantly better **zero-shot** performance by using a better **template**.




