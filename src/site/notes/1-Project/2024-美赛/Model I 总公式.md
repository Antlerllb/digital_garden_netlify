---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Model I 总公式/"}
---

# 1 文本
**Our Model**: The complete generative process of our model is as follows:
P(X,Y)=∏t=1nP(yt∣zt,ht)⋅P(zt∣zt−1,X)⋅P(ht∣xt,ht−1)P(X,Y)=t=1∏n​P(yt​∣zt​,ht​)⋅P(zt​∣zt−1​,X)⋅P(ht​∣xt​,ht−1​)
Here, YY represents the output sequence, and P(X,Y)P(X,Y) is the joint probability of input and output sequences.
# 2 图示
![5-Attachment/Image/Model I 总公式-20240203.png](/img/user/5-Attachment/Image/Model%20I%20%E6%80%BB%E5%85%AC%E5%BC%8F-20240203.png)