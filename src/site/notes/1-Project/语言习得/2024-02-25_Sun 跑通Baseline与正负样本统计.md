---
{"dg-publish":true,"permalink":"/1-Project/语言习得/2024-02-25_Sun 跑通Baseline与正负样本统计/"}
---

# 1 之前的工作
| Check | 工作 | 预计完成 | 备注 |
| ---- | ---- | ---- | ---- |
| ✔ | 整理数据集（样本统一格式） |  |  |
| ✔ | 统计正负样本 |  |  |
|  | 跑通BERT4EVER | +1天 | 前2天有点杂事耽搁了，后面会加快。 |
|  | LlaMa模型的下载与文档查看 | +30min |  |
|  | 中文的ChatGLM | +30min |  |
# 2 等待清单
- 中文：ChatGLM
- Cite实验室的预印本
- 对不同student写出的essay进行判断
# 3 目前疑问
之前老师说，可以有一个韩语作业的扫描版，需要我们自己OCR并匿名化。你感觉这个好搞吗？（因为我自己看不懂韩语，不是很有底）
# 4 样本统计
对于自构建的数据集，没有统计负样本，因为负样本数量取决于我们的构建方式。

| 样本集 | 正样本数 | 负样本数 | 比例 | 来源 |
| ---- | ---- | ---- | ---- | ---- |
| bawe | 2014503 | - | - | 自构建，源数据是别人的。 |
| diaz | 2738 | - | - | 自构建，源数据是别人的。 |
| leap | 551 | - | - | 自构建，源数据是别人的。 |
| litkey | 7670 | - | - | 自构建，源数据是别人的。 |
| lscc | 27157 | - | - | 自构建，源数据是别人的。 |
| parole | 557 | - | - | 自构建，源数据是别人的。 |
| pelic | 903590 | - | - | 自构建，源数据是别人的。 |
| clta_cows | 17745 | 17745 | 1:1 | 现成的数据集。它的负样本就是把所有正样本倒过来。 |
# 5 数据集描述
结论：如果把主题局限于写作的评估，能用的好像只有bawe、lscc、pelic。

| 数据集名称 | 总描述                                                       | 目标语言   |
| ---------- | ------------------------------------------------------------ | ---------- |
| bawe       | 本科及硕士生的写作练习。主题：艺术与人文、社会科学、生命科学和物理科学 | 英语       |
| diaz       | 口语转录的文本。地点：西班牙和巴塞罗那。人群：成人，来自印欧以及亚洲人（主要母语为德语、瑞典语、冰岛语、韩语、汉语） | 西班牙语   |
| leap       | 口语转录的文本。地点：德国比勒费尔德大学。人群：英国人和德国人。主题：对于韵律的学习情况。 | 英语 |
| litkey     | 小学生看图写故事。           | 德语       |
| lscc       | 口语转录的文本。主题：日常交流。人群：汉语母语者、英语母语者。 | 汉语       |
| parole     | 口语作品的转录文本。人群：英语、法语和意大利语的学习者。             | 英语       |
| pelic      | 书面写作、口语转录。主题：CEFR考试。 | 英语       |
