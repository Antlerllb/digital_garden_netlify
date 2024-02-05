---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Summary/"}
---

# 1 标题

# 2 摘要
Recently, Carlos Alcaraz secured a historic victory by defeating Novak Djokovic in the 2023 Wimbledon Gentlemen’s final. To gain a better understanding of the swings during the match, we will delve into a detailed modeling of the momentum.

For Task 1 and Task 2, we develop a **Multiagent Momentum Prediction Model**. Our model takes input features for each timestep and processes them sequentially through **an LSTM, a Sequence Encoder, a Sequence Prior, and a Sequence Decoder** to generate the Momentum Sequence. According to experimental results, **the average momentum value for all players** is **4.8**. **Carlos Alcaraz exhibited the highest momentum** throughout the entire match, with a value of **7.03**. Additionally, players with stronger momentum show the most significant gains in "ace" and "net points won".

For Task 3, we introduce the **Klaassen-Magnus ELO Ratings algorithm**. We input momentum and other action features, utilize **Multinomial Logit** to obtain the **joint probability of strategic choices**, and finally calculate the **ELO Rating to capture the swing** in the match. For example, in the match between Fokina and Rune, the sequence of ELO Swing Ratings changed as follows: **[0.425, 0.873, 0.517, 0.132]**. Taking into account the swing information, the Spanish tennis team **replaced Alejandro Davidovich Fokina with Carlos Alcaraz** in the second phase step, thereby improving the overall probability of winning.

For Task 4, we generalize the proposed method using the **Attacker-Defender Dribble Model**. We adapt the model to different ball shapes and playing fields by employing the **Three-Dimensional Kinematics of a Spherical Object**, and abstract the competing entities into **"Attacker" and "Defender."** For example, in the basketball game between the Phoenix Suns and the New York Knicks on January 3, 2023, the ELO Swing Rating sequence was **[0.356, 0.572, 0.871, 0.763, 0.446, 0.213]**. Considering the swing information, the Phoenix Suns **replaced Jordan Goodwin with Mitchell Robinson** in the third phase step.

Last but not least, we summarize the suggestions and write a memorandum to assist coaches to prepare players for events.

# 3 草稿
**不能只有对4个问题的回答**

近期，Carlos Alcaraz secured a historic victory by defeating Novak Djokovic In the 2023 Wimbledon Gentlemen’s final。为了更好理解比赛中的swing，我们将对Momentum进行深入建模。

对于Task 1和Task 2，我们构建了Multiagent Momentum Prediction Model。对于Momentum的Prediction，Our model将包含timesteps的输入特征依次传入LSTM, **Sequence Encoder**, **Sequence Prior**和**Sequence Decoder**以得到Momentum Sequence。根据实验结果，所有球员的平均momentum值为xxx，Carlos Alcaraz在整场赛事中的momemtum最高，值为xxx。当球员momentum较强时，ace and net_pt_won获得的增益最强，系数为3.2。当球员的momentum drop时，"Double Fault," and "Unforced Error"会显著增加。

对于Task3，我们introduce了Klaassen-Magnus ELO Ratings 算法。我们输入momentum和其他行为特征，利用Multinomial Logit获得策略选择的联合概率，最后计算ELO Rating来capture战况中的swing。例如，Fokina对决Rune的比赛中的ELO Swing Rating变化序列为[0.425, 0.873, 0.517, 0.132]。西班牙网球队考虑到了swing信息，在第2个phase step后将Alejandro Davidovich Fokina替换为Carlos Alcaraz，提高了总体胜利概率。

对于Task 4，我们利用Attacker-defender Dribble Model泛化我们提出的预测模型。我们利用Three Dimensional Kinematics of Spherical Object让模型始配不同的球形和球场，再abstract the competing entities into "Attacker" and "Defender."。例如，在2023年1月3日Phoenix Suns对决New York Knicks的篮球比赛中，ELO Swing Rating的变化序列为[0.356, 0.572, 0.871, 0.763, 0.446, 0.213]，Phoenix Suns考虑了swing信息并在第3个phase step将Jordan Goodwin替换为Mitchell Robinson。从综合角度看，模型对篮球、足球、乒乓球的胜利预测精度都高达90%，体现了极强的泛化能力。

Last but not least, we summarize the suggestions and write a memorandum to assist coaches to prepare players for events.

# 4 备用
## 4.1 task3
match间的swing表明：The strategic decision to replace  with proved successful for the Spanish tennis team. 为了帮助球员获得momentum增益，我们建议他们conduct a thorough analysis of their opponent's historical serving, hitting, and movement patterns.