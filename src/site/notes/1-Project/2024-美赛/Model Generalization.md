---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Model Generalization/"}
---

# 1 Model Generalization: Shared Momentum in Multiagent Ball Games
## 1.1 Three Dimensional Kinematics: Spherical Object and Attacker-defender Dribble Model
In this section, we focus on the generalization of the momentum concept across various ball games, namely basketball, football, and table tennis. The data collection process involves obtaining datasets from different games, each offering unique insights into player dynamics and game characteristics.

Table: Multiagent Ball Games Dataset Overview

| Ball Game | Dataset | Content（用无序列表） |
| ---- | ---- | ---- |
| Basketball | NBA[^2] | Player metrics data, Performance statistics, Physical activity records |
| Football | San Jose (SJ) Earthquakes[^1] | (x, y)-player position data, Log of all 1v1 situations |
| Table Tennis | OSAI[^3] | Players' potential features, In-match statistics |

**Spherical Object Kinematics**[^4]: Angular momentum ($L$) is a vector quantity representing the rotational motion of an object. It is the product of the moment of inertia ($I$ ) and the angular velocity ($ω$) of the object. It provides a quantitative measure of the rotational motion of the object and is crucial in understanding the dynamics of various sports activities such as basketball, football, table tennis, and tennis.

Figure: Flow Chart of Angular Momentum Calculation
[[1-Project/2024-美赛/角动量流程图\|角动量流程图]]

In various sports like basketball, football, table tennis, and tennis, the concept of angular momentum is integral. When players shoot, kick, or hit the ball with a spinning motion, angular momentum comes into play. The moment of inertia, influenced by the distribution of mass within the ball, determines the magnitude of angular momentum. This spinning motion significantly impacts the trajectory and behavior of the ball, emphasizing the role of angular momentum in shaping the outcome of plays in these sports.

Figure: Angular Momentum in Multiagent Ball Games
[[1-Project/2024-美赛/泛化的球和球场图\|泛化的球和球场图]]

For instance, I advocate for the generalization capability of a Momentum prediction model developed for tennis matches to basketball games. In this context, I consider the basketball Shot Depth as analogous to the Serve Depth in Tennis, the Shot Height as equivalent to the Serve Width in Tennis, and the Shot Velocity as comparable to the Speed Mph in Tennis. This cross-domain mapping allows us to leverage insights from tennis momentum modeling and apply them to basketball scenarios, providing a foundation for a more versatile predictive model across different sports.

Figure: Action Simulation For Single Basketball Player
[[1-Project/2024-美赛/投篮可视化\|投篮可视化]] + [[1-Project/2024-美赛/宽度深度-动量泛化\|宽度深度-动量泛化]]

In addition to the impact of shooting actions on momentum, we are also considering the role of passing actions. Using a 3D heatmap, with Shoot Distance as a control variable, we aim to model the relationship between Pass Distance and Momentum. The results indicate a positive correlation, highlighting the influence of passing actions on the overall momentum in both basketball and tennis scenarios.
**Attacker-defender Dribble Model**[^5]: We are currently developing a generalized model applicable to basketball, soccer, tennis, and table tennis. Within this framework, we abstract the competing entities into two primary roles: "Attacker" and "Defender." Our model attributes three force components to the Attacker: Attraction to the goal, Repulsion by the defender, and Physiological resistance, resulting in the calculation of the Overall Attacker Momentum. Simultaneously, the Defender is characterized by three force components: Attraction to the goal, Attraction to the attacker, and Physiological resistance, culminating in the computation of the Overall Defender Momentum. This unified modeling approach allows us to capture the momentum dynamics between attackers and defenders across diverse sports.

Figure: Attacker-defender Dribble Model
[[1-Project/2024-美赛/泛化模型解释图\|泛化模型解释图]]

## 1.2 Result of Task 4: Generalization For Basketball, Football and Table Tennis


[[1-Project/2024-美赛/篮球战局图\|篮球战局图]]


[[1-Project/2024-美赛/运动效果对比图\|运动效果对比图]]






Table: 
[[1-Project/2024-美赛/误差分析表\|误差分析表]]


[^1]: https://www.sjearthquakes.com/
[^2]: https://zenodo.org/records/8056757
[^3]: https://osai.ai
[^4]: Opatrný, T., Richterek, L., & Opatrný, M. (2018). Analogies of the classical Euler top with a rotor to spin squeezing and quantum phase transitions in a generalized Lipkin-Meshkov-Glick model. _Scientific Reports_, _8_(1), 1984.
[^5]: Brink, L., Ha, S. K., Snowdon, J., Vidal-Codina, F., Rauch, B., Wang, F., … & Hosoi, A. E. (2023). Measuring skill via player dynamics in football dribbling. _Scientific Reports_, _13_(1), 19004.