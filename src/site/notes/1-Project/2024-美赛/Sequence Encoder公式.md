---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Sequence Encoder公式/"}
---

# 1 文本
**Sequence Encoder**: The sequence encoder processes input sequences and captures their contextual information using a Bidirectional Long Short-Term Memory (Bi-LSTM) network. For a given sequence of inputs X=(x1,x2,…,xn)X=(x1​,x2​,…,xn​), the forward and backward hidden states ht→ht​​ and ht←ht​​ at each timestep tt are computed as follows:  
The final hidden state is obtained by concatenating both directions: ht=[ht→;ht←]ht​=[ht​​;ht​​].
# 2 图示
![5-Attachment/Image/Sequence Encoder公式-20240203.png](/img/user/5-Attachment/Image/Sequence%20Encoder%E5%85%AC%E5%BC%8F-20240203.png)