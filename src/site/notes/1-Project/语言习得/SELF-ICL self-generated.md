---
{"dg-publish":true,"permalink":"/1-Project/语言习得/SELF-ICL self-generated/"}
---

[[5-Attachment/ZoteroNote/@SelfICLZeroShot_2023_Chen\|@SelfICLZeroShot_2023_Chen]]
# 1 理念
- Most techniques
	- Most techniques assume the access to large-scale external sources (e.g., training dataset or relevant text corpus) is available, 
	- from which demonstrations can be selected with methods such as nearest neighbor search or other pre-defined, sophisticated similarity metrics (Liu et al., 2022; Rubin et al., 2022; Wu et al., 2022).
- However, in most real-world scenario
	- users query LLMs (e.g., through APIs or web interface) without the access to existing corpus for their target tasks.
- Also
	- spending additional effort to handcraft demonstrations may negatively affect their workflows.
# 2 代码逻辑
- (1) Given a query and a corresponding task description, the LLM is prompted to generate k (e.g., k=3) pseudo-inputs.
- (2) Collect the pseudo-inputs and predict their pse udo-labels via zero-shot prompting.
- (3) Perform ICL with pseudo-demonstrations constructed from the generated pseudo-input-label pairs.
![Zero-shot Self-Generated Demo-20240216-1.png|400](/img/user/5-Attachment/Image/Zero-shot%20Self-Generated%20Demo-20240216-1.png)
![Zero-shot Self-Generated Demo-20240216.png|350](/img/user/5-Attachment/Image/Zero-shot%20Self-Generated%20Demo-20240216.png)
# 3 对比之前的ICL方法
![SELF-ICL self-generated-20240216.png|475](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240216.png)    
# 4 实验设置
## 4.1 语言模型
| 模型 | instruct |
| ---- | ---- |
| InstructGPT | text-davinci-003 (Ouyang et al., 2022) |
| PaLM-2 | text-bison-001 [PaLM 2 models  \|  Google AI for Developers](https://ai.google.dev/models/palm) |
| GPT-3.5 | gpt-3.5-turbo-instruct [OpenAI API](https://platform.openai.com/docs/models/overview) |
## 4.2 Prompt
### 4.2.1 Direct prompting
![SELF-ICL self-generated-20240216-4.png|325](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240216-4.png)
### 4.2.2 CoT prompting
"Let's think step by step"
![SELF-ICL self-generated-20240216-2.png|425](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240216-2.png)
## 4.3 Pseudo-Inputs Generation
理念：[[1-Project/语言习得/ICL 理解#2 Pseudo-inputs’ diversity\|ICL 理解#2 Pseudo-inputs’ diversity]]
### 4.3.1 Batch inference
the number of example instances in the prompt equals the number of given test input, i.e., the batch size. 
![SELF-ICL self-generated-20240217.png|350](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240217.png)
### 4.3.2 Prompting with diversity hints
the model is explicitly instructed to provide “new”, “diverse”, and “creative” pseudo-input instances.
![SELF-ICL self-generated-20240217-1.png|425](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240217-1.png)
### 4.3.3 Prompting without diversity hints
simply remove the key words “new”, “diverse”, and “creative” in the instruction, and keep all other settings unchanged.
## 4.4 Similarity gap between pseudo- and real-inputs
![SELF-ICL self-generated-20240217-5.png|350](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240217-5.png)
# 5 实验结果
## 5.1 ICL方法+Prompt策略
![SELF-ICL self-generated-20240216-6.png](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240216-6.png)
![SELF-ICL self-generated-20240216-5.png](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240216-5.png)
## 5.2 ICL方法+其他LM（模型泛化能力）
![SELF-ICL self-generated-20240216-3.png](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240216-3.png)
## 5.3 Pseudo-Inputs Generation
### 5.3.1 Similarity
![SELF-ICL self-generated-20240217-2.png|400](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240217-2.png)
### 5.3.2 Performance
可视化不好的地方：在文字中说No Diverse是 `simply remove the key words “new”, “diverse”, and “creative” in the instruction, and keep all other settings unchanged.` ，但在图中没有体现。
![SELF-ICL self-generated-20240217-3.png|425](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240217-3.png)
### 5.3.3 The similarity gap between pseudo- and real-inputs
indicating the pseudo-inputs are close to the real-inputs and are likely robust against the copying effect.
![SELF-ICL self-generated-20240217-4.png](/img/user/5-Attachment/Image/SELF-ICL%20self-generated-20240217-4.png)
# 6 Gap
## 6.1 对copying effect的理解
#gap 
Exploring the underlying relationship between the copying effect and Wei et al. (2023)’s findings are left as future works.
Wei et al. (2023): [[5-Attachment/ZoteroNote/@LargerLanguage_2023_Wei\|@LargerLanguage_2023_Wei]]
## 6.2 Better diversify approaches
- comprehensive prompt searching
- experiment with temperature adjustments