---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Memo-Descriptions/"}
---

# 1 How to captures the flow of play?
- Part 1
	- **Capture Timestep Actions**: Analyze the player's movements, shot selections, and decision-making during each point. (e.g., serve, forehand/backhand strokes, volleys)
	- **Capture Strategy Trajectories**: Understand how players adjust their tactics and game plans throughout the match. (e.g., approaching the net, playing defensively from the baseline)
	- [[1-Project/2024-美赛/Model I 概念解释图\|Model I 概念解释图]]
- Part 2
	- [[1-Project/2024-美赛/比赛过程可视化-折线图\|比赛过程可视化-折线图]]
# 2 How significant is momentum to performance?
- Part 1
	- [[1-Project/2024-美赛/平均得分热图\|平均得分热图]] 第1个Figure的第1排 + 第2个Figure的第1排
	- **Positive Correlations**: Momentum <-> Ace and Net_pt_won
	- **Negative Correlations**: Momentum <-> Double faults and Unforced Error
- Part 2
	- [[1-Project/2024-美赛/球员表现图表并排\|球员表现图表并排]] 只要图
	- 找个地方标注一下：Superstar players的球员的Momentum最高
# 3 How to predict the swing in a match?
- By calculating The Multinomial Logit and Klaassen-Magnus ELO Ratings, we can derive t**he swing patterns in different areas of the court at various phases** in a game.
- Swing in Tennis Matches
	- [[1-Project/2024-美赛/比赛过程可视化-密度图\|比赛过程可视化-密度图]] + [[1-Project/2024-美赛/球员雷达图\|球员雷达图]]
# 4 How can we generalize the model to other sports?
- Part 1
	- We are currently developing a generalized model applicable to basketball, soccer, tennis, and table tennis. We **abstract the competing entities** into two primary roles: "**Attacker**" and "**Defender**."
	- [[1-Project/2024-美赛/泛化模型解释图\|泛化模型解释图]]
- Part 2
	- Swing in Basketball Matches
		- [[1-Project/2024-美赛/篮球战局图\|篮球战局图]]
