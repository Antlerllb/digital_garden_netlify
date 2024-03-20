---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Related Work/"}
---

# 1 原论文的框架
LDA: language development assessment
- Linguistic-features-based Methods
- Neural-networks-based Methods
# 2 语言习得
## 2.1 撰写想法
- 合并2条路线的文章，对比师兄的写法和摘要，写出自己的句子。
- 再找几篇新的文献。
## 2.2 文献列表
### 2.2.1 Linguistic features
- Hancke and Meurers (2013)
	- tracked the development of writing complexity and accuracy in German students’ early academic language development, spanning first through eighth grade.
	- They strengthened the applicability and reliability of their models by incorporating a comprehensive set of complexity features across various writing subjects.
- Vajjala and Lõo (2014)
	- concentrated on approaches that automate the prediction of a learner’s language proficiency in Estonian.
	- The methods employed the extraction of morphological and POS tag information from the texts produced by the learners.
- Pilán and Volodina (2018)
	- conducted a comprehensive analysis of predictive features extracted from receptive and productive texts in the context of Swedish L2 acquisition.
- Miaschi et al. (2020)
	- employed linguistic features automatically extracted from students’ written essays to assess the development of written language abilities in L2 Spanish learners.
- Miaschi et al. (2021b)
	- proposed a style measure method to assess the development of written language competence in Italian L1 learners. The measure involved capturing various linguistic features related to text style.
- Bulté and Housen (2014)
	- conducted a investigation with the aim of determining the nature and extent of English L2 writing proficiency development among 45 adult ESL learners over the course of an intensive short-term academic English language program. The investigation utilized quantitative measures that specifically focused on various aspects of lexical and syntactic complexity observed in the learners’ writing performance.
	- aimed to compare the scores obtained from these measures with the subjective ratings given for the overall writing quality of the learners.
### 2.2.2 Neural networks
- Sagae (2021)
	- conducted a study to investigate whether a fully data-driven model of language development, incorporating a recurrent neural network to encode utterances, could effectively track the evolution in children’s language throughout their language development, comparable to expertly established language assessment metrics for language-specific information.
- HIAM (Wu et al., 2023)
	- The novel sequential information attention mechanism used in HIAM (Wu et al., 2023) captured the interaction between essay pairs.
	- This mechanism incorporates attention weights from the last-written essay into the pair representation by relying on the “[CLS]" token and employing average pooling.
- Barbini et al. (2023)
	- calculated the surprisal-based metrics by extracting token probabilities from pre-trained language-specific BERT models.
	- However, it is crucial to explore efficient methods of extracting language-independent text features and identify the differences and shared information between the first-written and second-written essays.
## 2.3 正文：Language Development Assessment
The trend in language development assessment is transitioning towards automation, shifting from linguistic-features-based methods to neural-networks-based methods.
Hancke and Meurers (2013) tracked the writing proficiency of German learners across different exam rating levels ranging from A1 to C1, integrating exhaustive syntactic and morphological features.
Vajjala and Lõo (2014) present methods for predicting language proficiency levels in Estonian learners according to the European CEFR scale, utilizing morphological and POS tag information extracted from written texts.
For the purpose of reducing linguistic complexity, Pilán and Volodina (2018) identified fourteen central linguistic features that not only contribute to simpler models but also improve language level classification performance.
To minimize manual intervention, Sagae (2021) investigated whether a recurrent neural network encoder, a fully data-driven model of language development, can accurately track changes in child language utterances over the course of language development.
Wu et al. (2023) introduced a novel sequential information attention mechanism, which automatically captures the interaction between essay pairs through attention weights integration and average pooling techniques.
[[5-Attachment/ZoteroNote/@ExploringCEFR_2013_Hancke\|@ExploringCEFR_2013_Hancke]]
[[5-Attachment/ZoteroNote/@AutomaticCEFR_2014_Vajjala\|@AutomaticCEFR_2014_Vajjala]]
[[5-Attachment/ZoteroNote/@InvestigatingImportance_2018_Pilan\|@InvestigatingImportance_2018_Pilan]]
[[5-Attachment/ZoteroNote/@TrackingChild_2021_Sagae\|@TrackingChild_2021_Sagae]]
[[5-Attachment/ZoteroNote/@BERT_4EVERLangLearn_2023_Wu\|@BERT_4EVERLangLearn_2023_Wu]]
# 3 LLM
关键词：Large Language Model
Pre-trained Language Model



As open-source large language models (LLMs) continue to ﬂourish and demonstrate remarkable competitiveness across various natural language generation (NLG) tasks, assessing the capabilities of LLMs has become an exceedingly challenging endeavor. To address this issue, Zheng et al. (2023) pioneered the creation of a chatbot arena, enabling users to provide pairwise evaluations of responses generated by two randomly...

Downstream transfer in language models Much previous work established a “pre-train and fine-tune” paradigm for enhancing LLM performance on downstream tasks (Radford et al., 2018; Dong et al., 2019; Vaswani et al., 2017; Devlin et al., 2018). However, fine-tuning is not always easily applicable (Hendrycks et al., 2020). More recent literature exhibits a paradigm shift towards “prompting” the model to predict the desired output (Liu et al., 2021; Raffel et al., 2020). Large LMs can exhibit strong performance in this setting (Brown et al., 2020). For smaller models to be able to perform similarly, additional engineering is usually required (Gao et al., 2021; Schick and Schütze, 2021b; Schick et al., 2020).
[[5-Attachment/ZoteroNote/@LargeLanguage_2023_Hoa\|@LargeLanguage_2023_Hoa]]

