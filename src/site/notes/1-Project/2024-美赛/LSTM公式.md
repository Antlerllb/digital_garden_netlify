---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/LSTM公式/"}
---

# 1 文本
**Long Short-Term Memory (LSTM)**[^1] is a type of recurrent neural network (RNN) designed to capture and retain information over sequential data. The key components are the input gate (itit​), forget gate (ftft​), and output gate (otot​). The LSTM equations are as follows:
ft​it​C~t​Ct​ot​ht​​=σ(Wf​⋅[ht−1​,xt​]+bf​)=σ(Wi​⋅[ht−1​,xt​]+bi​)=tanh(WC​⋅[ht−1​,xt​]+bC​)=ft​⋅Ct−1​+it​⋅C~t​=σ(Wo​⋅[ht−1​,xt​]+bo​)=ot​⋅tanh(Ct​)​
Here, xtxt​ represents the input at timestep tt, htht​ is the hidden state, CtCt​ is the cell state, and σσ is the sigmoid activation function.
# 2 图示
#公式 
![5-Attachment/Image/LSTM公式-20240203.png](/img/user/5-Attachment/Image/LSTM%E5%85%AC%E5%BC%8F-20240203.png)

[^1]: Hochreiter, S., & Schmidhuber, J. (1997). Long short-term memory. _Neural computation_, _9_(8), 1735-1780.