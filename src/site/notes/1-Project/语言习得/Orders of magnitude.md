---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Orders of magnitude/"}
---

[[5-Attachment/ZoteroNote/@EvaluatingNeural_2023_VazquezMartinez\|@EvaluatingNeural_2023_VazquezMartinez]]
#low-resource 
# 1 Training
- most models are trained on
	- orders of magnitude more input than humans
	- plain text form
	- BERT: 3.3B forms, Chinchilla: 1.4T
- humans receive
	- in spoken or signed form
	- English-learning child: 10M word per year
	- (Fenson et al., 1994; Bornstein et al., 2004).
# 2 Grammar learning
- not all aspects of linguistic knowledge are learned at the same time
- are acquired very early in all languages (e.g., Brown, 1973; Slobin, 2022)
	- inflectional morphology, case marking, word order, and major transformations
- are learned rather late in English (may emerge much earlier in other languages)
	- derivational morphology (Jarmulowicz, 2002)
	- passivization (Pinker et al., 1987)
	- control and cleft structures (Chomsky, 1969)
	- the dative constructions (Gropen et al., 1989)
# 3 Vocabulary learning vs grammar learning
#vocab-vs-gammar
## 3.1 Evidence
#longitudial 
- children
	- recorded at regular intervals from age 1 to 3 (Providence Corpus (Demuth et al., 2006))
- vocabulary size: less overlap (Hart and Risley, 1995; Bornstein et al., 2004)
	- On average, fewer than 20% of the first 100 words are shared between any two children.
	- The overlap merely rises to about 40% for the first 1,000, which is the upper limit of a three-year old’s vocabulary size. 
	- [[1-Project/语言习得/Word learning trajectories\|Word learning trajectories]]
- grammars: highly uniform even at this stage
	- Major syntactic categories, word order and argument structure, and the core morphological rules (Brown, 1973)
	- on the basis of at most around 10M words per year (Hart and Risley, 1995)
	- a vocabulary size of only a few hundred types (Fenson et al., 1994)
	- all children produce similar grammatical errors during this time
## 3.2 Claim
- vocabulary learning: a matter of rote learning (words)
	- include:
		- arbitrary pairing of sounds and meanings
		- morphological processes (e.g., irregularity)
		- syntactic structures (e.g., sub-categorization, collocations, etc.).
	- There is no escape from experience: more data results in better learning.
- grammar learning: structural learning (rules)
	- require from generalizations over the vocabularies.
- existing LM benchmarks #gap
	- a mixture of tests for both vocabulary learning and grammar learning
	- not well reflected: The distinction between rote learning and structural learning
- expected: carefully curated linguistic materials
	- structurally diverse
	- have minimized lexical and semantic confounds.
# 4 Exp
- successful learning in the limit (e.g., 100M word) is not sufficient
	- Example: "add -ed" rule (past tense)
	- a neural model of English past tense (Kirov and Cotterell, 2018): does so with over 3,000 verb lemmas.
	- children: before or around 3 (Kuczaj, 1977), their vocabulary only contains around 300 or so verbs (Marcus et al., 1992).
- #gap
	- compare the training trajectory of LMs
	- as a function of the training data volume
	- against the developmental benchmarks of specific linguistic phenomena