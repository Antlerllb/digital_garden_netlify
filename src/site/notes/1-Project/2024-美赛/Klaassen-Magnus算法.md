---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Klaassen-Magnus算法/"}
---

# 1 文本
Algorithm 1 Klaassen-Magnus Elo Serve Parameters procedure EloServeProbabilities(π, b, ) f ← b/2 diff ← b/4 currentProb ← .5 while |currentProb - π| >do: If currentProb < π then f += diff else f -= diff diff = diff/2 currentProb ← matchProb(f , b - f ) return f, b , −f
# 2 图片
![5-Attachment/Image/Klaassen-Magnus算法-20240202.png|450](/img/user/5-Attachment/Image/Klaassen-Magnus%E7%AE%97%E6%B3%95-20240202.png)