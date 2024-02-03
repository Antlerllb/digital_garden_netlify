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
**Sequence Encoder (Bi-LSTM)**: The sequence encoder processes input sequences and captures their contextual information using a Bidirectional Long Short-Term Memory (Bi-LSTM) network. For a given sequence of inputs X=(x1,x2,…,xn)X=(x1​,x2​,…,xn​), the forward and backward hidden states ht→ht​​ and ht←ht​​ at each timestep tt are computed as follows:

> [!NOTE] 公式排版
> 文本
> **Sequence Encoder (Bi-LSTM)**: The sequence encoder processes input sequences and captures their contextual information using a Bidirectional Long Short-Term Memory (Bi-LSTM) network. For a given sequence of inputs X=(x1,x2,…,xn)X=(x1​,x2​,…,xn​), the forward and backward hidden states ht→ht​​ and ht←ht​​ at each timestep tt are computed as follows:
> The final hidden state is obtained by concatenating both directions: ht=[ht→;ht←]ht​=[ht​​;ht​​].
> 
> 正文
> ![5-Attachment/Image/Model I-20240203.png](/img/user/5-Attachment/Image/Model%20I-20240203.png)

Figure: Bi-LSTMs Sequence Model For Tennis Prediction
[[1-Project/2024-美赛/Model I 模型图\|Model I 模型图]]


## 2.2 