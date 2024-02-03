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
| Timesteps | A specific moment or interval in the sequence of events during a tennis match |
| Agent trajectories | Historical strategy of the agents in the tennis court up to the specified time in the time series data |
| Mask | Binary array that is applied to the data at each timestep |

As the match progresses, Timesteps capture specific moments, indicating discrete points in time where the model observes and records the historical strategies or movements of the agents, such as tennis players. The dynamic nature of Timesteps allows the model to adapt to the changing dynamics of the game, considering the sequential nature of events.  The use of masks allows the model to selectively attend to actions that are relevant for the prediction task while maintaining privacy or preventing the opposing agent from observing certain strategic moves. Masked actions provide a mechanism for agents to execute strategies that are concealed from their opponents, adding an element of strategic complexity to the prediction model.

Figure: Multiagent Timesteps Input
[[1-Project/2024-美赛/Model I 概念解释图\|Model I 概念解释图]]

By employing masks to filter out unobservable actions, the model can focus on the subset of actions that contribute to the observable dynamics of the game. This can enhance the accuracy of predictions by considering only the relevant and visible aspects of agent behavior.
[[1-Project/2024-美赛/LSTM公式\|LSTM公式]]
[[1-Project/2024-美赛/Sequence Encoder公式\|Sequence Encoder公式]]
[[1-Project/2024-美赛/Sequence Prior公式\|Sequence Prior公式]]
[[1-Project/2024-美赛/Sequence Decoder公式\|Sequence Decoder公式]]
[[1-Project/2024-美赛/Model I 总公式\|Model I 总公式]]
This model leverages the tennis match information captured by the Bi-LSTM encoder, incorporates latent variables through the sequence prior, and generates output sequences using the sequence decoder. The training involves maximizing the log-likelihood of the observed data.

Figure: Bi-LSTMs Sequence Model For Tennis Prediction
[[1-Project/2024-美赛/Model I 模型图\|Model I 模型图]]

## 2.2 Todo