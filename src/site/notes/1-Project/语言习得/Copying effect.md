---
{"dg-publish":true,"permalink":"/1-Project/语言习得/Copying effect/"}
---

[[5-Attachment/ZoteroNote/@ZICLZeroShot_2023_Lyu\|@ZICLZeroShot_2023_Lyu]]
# 1 对比 Typical ICL
the demonstrations are sampled uniformly at random from the true distribution
e.g., the training data in case of existing NLP datasets
# 2 Copying Effect
Copying in ICL: how seen token patterns affect the ICL’s prediction?
Copying Effect需要被reduce
- Olsson et al. (2022)
	- identifies specific attention heads that, when predicting the next token, look for the previous similar tokens of the current last token in the demonstrations, and copy the tokens following those similar tokens.
- Our work similarly finds
	- ICL is prone to copy previously seen text from the demonstrations, but specifically with the particular input-label format in the demonstrations
- ***Copying Effect***
	- when demonstrations contain input text that is very similar to the test input, the model exhibits a behavior
# 3 图示
The model tends to copy the label from the demonstration input that is close to the test input.
![Copying-20240215.png](/img/user/5-Attachment/Image/Copying-20240215.png)
# 4 结果
The gap between gold and random labels is more significant with nearest ICL than with ICL.
**The correctness of labels matters more** when the demonstrations are closer to the test input.
下文的Nearest代表：Copying effect
![Copying effect-20240215.png|425](/img/user/5-Attachment/Image/Copying%20effect-20240215.png)