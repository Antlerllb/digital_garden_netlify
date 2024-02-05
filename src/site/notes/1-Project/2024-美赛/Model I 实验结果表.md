---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Model I 实验结果表/"}
---

# 1 修改
下面表格的字段记得用原文的Latex格式

| Model | $L2$ (Mean) | $L2$ (Min) | Pitch control MAE |
| ---- | ---- | ---- | ---- |
| Spline (Linear) | 0.281 | 0.212 | 0.128 |
| Spline (Quadratic) | 0.298 | 0.236 | 0.134 |
| Spline (Cubic) | 0.324 | 0.268 | 0.145 |
| LSTM | 0.215 | 0.189 | 0.102 |
| LSTM+Encoder | 0.242 | 0.161 | 0.101 |
| LSTM+Decoder | 0.198 | 0.142 | 0.099 |
| **Bi-LSTMs Sequence Model (Ours)** | **0.176** | **0.123** | **0.091** |

# 2 原图
[[5-Attachment/ZoteroNote/@MultiagentOffscreen_2022_Omidshafiei\|@MultiagentOffscreen_2022_Omidshafiei]]
![5-Attachment/Image/Model I 实验结果表-20240204.png](/img/user/5-Attachment/Image/Model%20I%20%E5%AE%9E%E9%AA%8C%E7%BB%93%E6%9E%9C%E8%A1%A8-20240204.png)
![5-Attachment/Image/Model I 实验结果表-20240204-1.png](/img/user/5-Attachment/Image/Model%20I%20%E5%AE%9E%E9%AA%8C%E7%BB%93%E6%9E%9C%E8%A1%A8-20240204-1.png)