---
{"dg-publish":true,"permalink":"/5-Attachment/ZoteroNote/@LearningIncontext_2023_Chen/","title":"Learning In-context Learning for Named Entity Recognition"}
---

# Learning In-context Learning for Named Entity Recognition
## Link
- Url: https://aclanthology.org/2023.acl-long.764
- Item: [item](zotero://select/library/items/3YAU5PDP)
- File: [LearningIncontext_2023_Chen.pdf](zotero://open-pdf/library/items/XW2PZ4FI)
## Abstract
Named entity recognition in real-world applications suffers from the diversity of entity types, the emergence of new entity types, and the lack of high-quality annotations. To address the above problems, this paper proposes an in-context learning-based NER approach, which can effectively inject in-context NER ability into PLMs and recognize entities of novel types on-the-fly using only a few demonstrative instances. Specifically, we model PLMs as a meta-function Lambda_instruction, demonstrations, text.M, and a new entity extractor can be implicitly constructed by applying new instruction and demonstrations to PLMs, i.e., (Lambda . M) (instruction, demonstrations) -\textgreaterF where F will be a new entity extractor F: text -\textgreater entities. To inject the above in-context NER ability into PLMs, we propose a meta-function pre-training algorithm, which pre-trains PLMs by comparing the (instruction, demonstration)-initialized extractor with a surrogate golden extractor. Experimental results on 4 few-shot NER datasets show that our method can effectively inject in-context NER ability into PLMs and significantly outperforms the PLMs+fine-tuning counterparts.