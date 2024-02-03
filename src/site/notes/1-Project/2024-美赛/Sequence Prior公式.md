---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Sequence Prior公式/","tags":["公式"]}
---

# 1 文本
**Sequence Prior**: The sequence prior models the temporal dependencies and encodes the prior information about the sequence. It can be represented as a probability distribution over the latent space. Let ztzt​ be the latent variable at timestep tt, then the sequence prior is defined as:
P(zt∣zt−1,X)=PriorModel(zt−1,ht)P(zt​∣zt−1​,X)=PriorModel(zt−1​,ht​)
# 2 图示
![5-Attachment/Image/Sequence Prior公式-20240203.png](/img/user/5-Attachment/Image/Sequence%20Prior%E5%85%AC%E5%BC%8F-20240203.png)