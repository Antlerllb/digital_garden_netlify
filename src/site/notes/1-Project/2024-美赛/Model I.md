---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Model I/"}
---

# 1 框架
- 模型：拟合比赛流程（模型图）
- 回答：球员的表现和程度
- 回答：动量的存在
# 2 Model I: Multiagent Time-Series Prediction Model
## 2.1 Bi-LSTMs Sequence Model
Our model utilizes the concepts of timestep, agent trajectories[^1], and masks to capture and analyze the temporal dynamics of a tennis match, considering historical movements and applying binary filters for effective time-series prediction.

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

## 2.2 Result of Task 1: Player's Momentum Trends
#Todo 实验结果的描述

Table: Performance Evaluation Metrics for Various Models in Momentum Prediction
[[1-Project/2024-美赛/Model I 实验结果表\|Model I 实验结果表]]

The data visualized in the plot represents the momentum of tennis players during the 2023 Wimbledon tournament. The momentum is illustrated in two aspects: within each game and the total momentum accumulated by each player throughout the entire event.

Figure: Histogram of Momentum Trends and Total Performance
[[1-Project/2024-美赛/Momentum直方图\|Momentum直方图]]

For instance, Carlos Alcaraz's momentum during the 2023 Wimbledon tournament exhibits fluctuations across various games. Notably, in the match "2023-wimbledon-1301," Game 2 stands out with the highest momentum (0.9038), while Game 7 reflects the lowest momentum (0.0095). Overall, Alcaraz maintains a moderate to high level of total momentum, demonstrating consistency throughout the competition.
Comparing his total momentum (4.9) with other players reveals that Alcaraz performs better than Alexander Zverev (total momentum: 4.64) but slightly falls short of Frances Tiafoe (total momentum: 5.65). This suggests a competitive performance but with room for improvement.

In the 2023-wimbledon-1301 match between Carlos Alcaraz and Nicolas Jarry, the game started evenly with both players scoring points in the early sets. However, as the match progressed, a notable pattern emerged. Carlos Alcaraz demonstrated a consistent and increasing momentum, securing critical points and maintaining a strong performance. On the other hand, Nicolas Jarry faced challenges, leading to missed opportunities, especially during crucial moments. Alcaraz's momentum and strategy play a crucial role in shaping the dynamics of the match, ultimately influencing the outcome in his favor.

Figure: Visualization for 2023-wimbledon-1301 Match Between Carlos Alcaraz and Nicolas Jarry
[[1-Project/2024-美赛/比赛过程可视化-折线图\|比赛过程可视化-折线图]]

## 2.3 Result of Task 2: Boost in Player Performance by Momentum Gain
This article visually depicts the trends in "Momentum," "Ace," "Net_pt_won," "Double Fault," and "Unforced Error" over different points in a tennis match. This comprehensive visualization allows for a holistic analysis of player performance dynamics, considering multiple performance metrics simultaneously.

Figure: Boost in Player Performance by Momentum Gain
[[1-Project/2024-美赛/平均得分热图\|平均得分热图]]的第1个figure

Both ace and net_pt_won show positive correlations with the momentum, indicating that as the match advances, players tend to deliver more aces and achieve success in winning points at the net. This suggests a strong connection between momentum and the enhanced performance of players in terms of ace delivery and net points won.

Figure: Drop in Player Performance by Momentum Loss
[[1-Project/2024-美赛/平均得分热图\|平均得分热图]]的第2个figure

In early games (e.g., Game 1), high momentum (around 37 points_won) correlates with low double faults (approximately 2 points_won). As matches progress (e.g., Game 5), momentum declines (around 18 points_won), and double faults increase (reaching approximately 15 points_won). In later stages (e.g., Game 8), momentum further decreases (around 15 points_won), and double faults remain elevated (around 30 points_won). This inverse relationship suggests that declining momentum may lead to more double faults, negatively impacting players' performance.

In exploring the dynamics of Wimbledon 2023, we delve into two pivotal facets: the Player Face-off Network and the Player Momentum Overview. Superstar players like Carlos Alcaraz and Novak Djokovic consistently exhibit high momentum, with their decoder outputs surpassing prior outputs. However, among Elite players, the relationship varies; for instance, Daniil Medvedev experiences a slight dip in momentum, while Roman Saiullin shows a significant increase.

Figure: Player Face-off Network For Wimbledon 2023
Table: Player Momentum Overview For Wimbledon 2023
[[1-Project/2024-美赛/球员表现图表并排\|球员表现图表并排]]


[^1]: Song, H., Li, Y., Zou, X., Hu, P., & Liu, T. (2023). Elite male table tennis matches diagnosis using SHAP and a hybrid LSTM–BPNN algorithm. _Scientific Reports_, _13_(1), 11533.