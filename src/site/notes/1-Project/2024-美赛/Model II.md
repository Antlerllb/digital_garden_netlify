---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Model II/"}
---

[[1-Project/2024-美赛/C题-网球动量\|C题-网球动量]]
# 1 框架
- 模型：隐马尔可夫+Klaassen-Magnus elo rating指标
	- Multinomial Logit
	- Klaassen-Magnus elo ratings
	- Win Pro
- 回答：使用至少一场比赛提供的数据
- prompt：我正在建模网球比赛的Klaassen-Magnus elo rating，输入数据包含2个玩家的timesteps, momentum, won_sets, won_games, won_points, serve_width, serve_depth, double_err, unf_err等。我希望这个模型中包含Barnett-Clarke 公式、Efron-Morris 估计量、Klaassen-Magnus elo 评分。请给我具体算法和建模流程。
# 2 Model II: Klaassen-Magnus ELO Ratings For Swing Capture
## 2.1 ELO Rating Algorithm
**The Multinomial Logit** is employed with the objective of capturing the dynamics of a tennis player's momentum. As a modeler, the focus is on constructing a predictive framework that describes the likelihood of different outcomes related to a player's momentum. This modeling perspective involves incorporating various input features to estimate the probabilities associated with distinct momentum-related scenarios.
The probability that a tennis player exhibits a particular momentum outcome (e.g., gaining or losing momentum) is modeled as follows:
[[1-Project/2024-美赛/Logit公式\|Logit公式]]
[[1-Project/2024-美赛/ELO算法描述\|ELO算法描述]]
[[1-Project/2024-美赛/Klaassen-Magnus ELO Ratings算法 v2\|Klaassen-Magnus ELO Ratings算法 v2]]
## 2.2 Result of Task 3: Swings of ELO Rating in Matches and Advices For a Player
This section aims to unravel swings of ELO ratings, revealing the strategic maneuvers and pivotal moments that shape the narrative of Wimbledon 2023. The visualizations below provide a comprehensive view of the swings between players, shedding light on the intense and evolving nature of these tennis encounters.

Figure: Swing between Players in Wimbledon 2023 Matches
[[1-Project/2024-美赛/比赛过程可视化-密度图\|比赛过程可视化-密度图]] + [[1-Project/2024-美赛/球员雷达图\|球员雷达图]]

In the initial phase of the first match, Alejandro Davidovich Fokina exhibited a robust performance, emphasizing powerful serves and successful break points. His radar chart showcased high values in "Ace," "Break Point Won," and "Net Point Won," indicating a strong focus on these aspects. As the match progressed to the end phase, Fokina faced challenges related to momentum, leading to an increase in errors such as double faults and missed break points as the match reached its conclusion.
With the introduction of Carlos Alcaraz, a notable shift occurred. In the beginning phase of the match against Holger Rune, Alcaraz displayed powerful and consistent performance across all radar chart parameters, indicating a strong momentum. The court momentum visualization supported this by illustrating Alcaraz's dynamic play on the court.
The strategic decision to replace Alejandro Davidovich Fokina with Carlos Alcaraz proved successful for the Spanish tennis team. Alcaraz's growing momentum, showcased in both radar charts and court momentum visualizations, played a crucial role in securing victory over Holger Rune as the matches unfolded.

 #Todo 建议
 In this study, we propose that players conduct a thorough analysis of their opponent's historical serving, hitting, and movement patterns. For instance, scrutinizing an opponent's serving tendencies could involve studying their preferred serve types, placement, and success rates in different situations. Examining hitting patterns may include understanding their shot preferences, strengths, and weaknesses in various playing conditions. Additionally, analyzing movement habits entails observing their court coverage, preferred positioning, and footwork tendencies during different points in a match. By delving into these specifics, players can strategically formulate pre-match preparations tailored to their opponent's individual style of play.