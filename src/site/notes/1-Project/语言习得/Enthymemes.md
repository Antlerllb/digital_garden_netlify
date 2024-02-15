---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Enthymemes/"}
---

[[5-Attachment/ZoteroNote/@MindGap_2023_Stahl\|@MindGap_2023_Stahl]]
# 1 Enthymemes
- Argumentative writing
	- To write a logically strong or cogent argument
	- present sufficient evidence (premises)
	- justifies the argument’s claim (conclusion)
- ADUs
	- argumentative discourse units
- enthymemes
	- arguments draw on premises that are left implicit (Feng and Hirst, 2011)
	- which may be key to match the expectations of the audience (Habernal et al., 2018)
- However
	- may be insufficient to accept its conclusion (Johnson and Blair, 2006)
	- the quality of an argument will also often be limited (Alshomary et al., 2020b)
- Goal/Task
	- assess whether there is a possibly problematic enthymematic gap (pointing to locations of enthymemes)
	- generate a new ADU that fills the gap (making suggestions on how to reconstruct the enthymemes if desired)
- We create enthymemes only that cannot be detected by a BERT model.
# 2 Contribution
- An **automated** approach for **creating** corpora of enthymematic arguments in learner essays
- A **corpus** for studying two new NLP tasks on learner arguments: enthymeme detection and enthymeme reconstruction
- **Baseline approaches to detecting and reconstructing** enthymemes computationally
# 3 Corpus
- effectiveness of our automatic approach
	- inadequate enthymemes that are harmful to the quality of arguments
	- while not making their texts seem unnatural
- manually assess
	- the induced reduction in logical argument quality in terms of sufficiency
	- the naturalness of the enthymematic arguments in comparison to the original arguments written by learners
# 4 Detection
- Treat enthymeme detection as a binary classification task
- Given a learner argument and a position within the argument, predict whether there is an inadequate enthymeme (say, a logical gap) at the given position
# 5 Reconstruction
- Treat enthymeme reconstruction as a maskinfilling task
- Given a learner argument and a known enthymeme position within the argument, generate the enthymeme
