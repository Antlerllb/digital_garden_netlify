---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Logit公式/"}
---

# 1 文本
The probability that a tennis player exhibits a particular momentum outcome (e.g., gaining or losing momentum) is modeled as follows:
P(Player experiences momentum outcome i)=eβ⋅X∑j=12eβ⋅XP(Player experiences momentum outcome i)=∑j=12​eβ⋅Xeβ⋅X​
In this expression, ββ represents a vector containing the model parameters, and XX encompasses the input features associated with momentum, such as timesteps, won sets, won games, won points, serve width, serve depth, double faults, and unforced errors:
β=[β0,β1,…,β9]β=[β0​,β1​,…,β9​]
X=[timesteps,won_sets,won_games,won_points,serve_width,serve_depth,double_err,unf_err]X=[timesteps,won_sets,won_games,won_points,serve_width,serve_depth,double_err,unf_err]
# 2 图示
#公式 
把Momentum加进去
![5-Attachment/Image/Logit公式-20240204.png|475](/img/user/5-Attachment/Image/Logit%E5%85%AC%E5%BC%8F-20240204.png)