---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Model I/"}
---

# 1 框架
- 模型：拟合比赛流程（模型图）
	- 回答：球员的表现和程度
- 指标：隐马尔可夫+ELO指标（流程图与算法）
	- 回答：动量的存在
# 2 Model I: Multiagent Time-Series Prediction Model
## 2.1 Bi-LSTMs Sequence Model
Our model utilizes the concepts of timestep, agent trajectories, and masks to capture and analyze the temporal dynamics of a tennis match, considering historical movements and applying binary filters for effective time-series prediction.

Table: Multiagent Temporal Dynamics Notion

| Notion | Description |
| ---- | ---- |
| Timestep | A specific moment or interval in the sequence of events during a tennis match |
| Agent trajectories | Historical strategy of the agents in the tennis court up to the specified time in the time series data |
| Mask | Binary array that is applied to the data at each timestep |

Figure
[[1-Project/2024-美赛/Model I 概念解释图\|Model I 概念解释图]]