---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Summary/"}
---

# 1 标题

# 2 摘要
Recently, Carlos Alcaraz secured a historic victory by defeating Novak Djokovic in the 2023 Wimbledon Gentlemen’s final. In order to gain a better understanding of the swings during the match, we will delve into a detailed modeling of the momentum.
For Task 1 and Task 2, we build a Multiagent Momentum Prediction Model. Our model takes input features for each timestep and sequentially passes them through an LSTM, a Sequence Encoder, a Sequence Prior, and a Sequence Decoder to obtain the Momentum Sequence. According to experimental results, the average momentum value for all players is 4.8. Carlos Alcaraz exhibited the highest momentum throughout the entire match, with a value of 7.03. Additionally, our findings reveal that when players have stronger momentum, the gains in "ace" and "net points won" are most significant, with a coefficient of 3.2. Conversely, when a player's momentum drops, the occurrences of "Double Fault" and "Unforced Error" significantly increase.
#Todo 
For Task 3, we introduce the Klaassen-Magnus ELO Ratings algorithm. We input momentum and other action features, utilize Multinomial Logit to obtain the joint probability of strategic choices, and finally calculate the ELO Rating to capture the dynamics of the match. We modeled player exchanges within the Spanish tennis team, and the swing observed between matches indicates that the strategic decision to replace Alejandro Davidovich Fokina with Carlos Alcaraz was successful.
To assist players in gaining momentum advantages, we recommend conducting a thorough analysis of their opponent's historical serving, hitting, and movement patterns.
# 3 草稿
**不能只有对4个问题的回答**

近期，Carlos Alcaraz secured a historic victory by defeating Novak Djokovic In the 2023 Wimbledon Gentlemen’s final。为了更好理解比赛中的swing，我们将对Momentum进行深入建模。

对于Task 1和Task 2，我们构建了Multiagent Momentum Prediction Model。对于Momentum的Prediction，Our model将包含timesteps的输入特征依次传入LSTM, **Sequence Encoder**, **Sequence Prior**和**Sequence Decoder**以得到Momentum Sequence。根据实验结果，所有球员的平均momentum值为xxx，Carlos Alcaraz在整场赛事中的momemtum最高，值为xxx。当球员momentum较强时，ace and net_pt_won获得的增益最强，系数为3.2。当球员的momentum drop时，"Double Fault," and "Unforced Error"会显著增加。

对于Task3，我们introduce了Klaassen-Magnus ELO Ratings 算法。我们输入momentum和其他行为特征，利用Multinomial Logit获得策略选择的联合概率，最后计算ELO Rating来capture战况中的swing。我们对西班牙网球队中的player exchange进行了建模，match间的swing表明：The strategic decision to replace Alejandro Davidovich Fokina with Carlos Alcaraz proved successful for the Spanish tennis team. 为了帮助球员获得momentum增益，我们建议他们conduct a thorough analysis of their opponent's historical serving, hitting, and movement patterns.

对于Task 4，我们利用Attacker-defender Dribble Model泛化我们提出的预测模型。我们利用Three Dimensional Kinematics of Spherical Object让模型始配不同的球形和球场，再abstract the competing entities into "Attacker" and "Defender." ，最后从力学角度解构momentum。我们对篮球队伍Phoenix Suns中的2023年1月3日比赛的player exchange进行了建模，match间的swing表明：根据momentum将Jordan Goodwin替换为Mitchell Robinson顺应了swing的趋势，还提高了Phoenix Suns方作为Attacker时的momentum。最后从综合角度来看，The win predictions for various player categories across different sports are consistently accurate, with most categories achieving accuracy levels close to or exceeding 90%.

Last but not least, we summarize the suggestions and write a memorandum to assist coaches to prepare players for events.

