---
{"dg-publish":true,"permalink":"/1-Project/语言习得/2024-02-22_Thu 跑通Baseline与数据集处理/"}
---

# 1 之前的工作
| Check | 工作                                     | 预计完成    | 备注                                                                                                                      |
| ----- | ---------------------------------------- | --- | ------------------------------------------------------------------------------------------------------------------------- |
| ✔     | 要做的任务中的数据集（先关注英语）       |     |                                                                                                                           |
|       | 把那篇论文的代码跑出来（自己手动跑一下） | +1天    | 原来的代码封装性不强，正在重构，顺便看看[Hugging Face 官方文档](https://huggingface.co/learn/nlp-course/zh-CN/chapter1/3) |
| ✔     | 数据集统计描述                           |     |                                                                                                                           |
|       | LlaMa模型的下载与文档查看                | +30min    | 打算简单看看，等要用时再细查文档。                                                                                                                          |
|       | 中文的ChatGLM              | +30min    | 打算简单看看，等要用时再细查文档。                                                                                                                          |
# 2 目前的疑问
已有工作应该能较快结束，请问你对之后的工作有什么规划和想法吗？
# 3 实验室同主题文章
![5-Attachment/Image/2024-02-22_Thu 跑通Baseline与数据集处理-20240222.png](/img/user/5-Attachment/Image/2024-02-22_Thu%20%E8%B7%91%E9%80%9ABaseline%E4%B8%8E%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222.png)
# 4 在投论文
## 4.1 摘要
Recently, the field of language acquisition (LA) has significantly benefited from natural language processing technologies. A crucial task in LA involves tracking the evolution of language learners’ competence, namely language development assessment (LDA). However, the majority of LDA research focuses on high-resource languages, with limited attention directed toward low-resource languages. Moreover, existing methodologies primarily depend on linguistic rules and language characteristics, with limited exploration of exploiting pre-trained language models (PLMs) for LDA. In this paper, we present the IndoCL corpus (Indonesian Corpus of L2 Learners), which comprises compositions written by undergraduate students majoring in Indonesian language. Moreover, we propose a model for LDA tasks, which automatically extracts language-independent features, relieving laborious computation and reliance on specific language. The proposed model uses sequential information attention and similarity representation learning to capture the differences and common information from the first-written and second-written essays, respectively. It has demonstrated remarkable performance on both our self-constructed corpus and publicly available corpora. Therefore, it can be considered as a novel benchmark for LDA tasks. Furthermore, we investigate the feasibility of utilizing existing large-scale language models (LLMs) for LDA tasks. The results demonstrate significant potential for enhancing the performance of large-scale language models in LDA tasks.
## 4.2 模型
![5-Attachment/Image/2024-02-22_Thu 跑通Baseline与数据集处理-20240222-1.png|400](/img/user/5-Attachment/Image/2024-02-22_Thu%20%E8%B7%91%E9%80%9ABaseline%E4%B8%8E%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-1.png)
## 4.3 数据集构建
这个是我自己画的，原文详见论文的图片（CorpusBenchmark_1.tif）。
![5-Attachment/Image/数据集处理-20240222-1.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-1.png)
## 4.4 实验结果
![5-Attachment/Image/2024-02-22_Thu 跑通Baseline与数据集处理-20240222-2.png](/img/user/5-Attachment/Image/2024-02-22_Thu%20%E8%B7%91%E9%80%9ABaseline%E4%B8%8E%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-2.png)
![5-Attachment/Image/2024-02-22_Thu 跑通Baseline与数据集处理-20240222-3.png](/img/user/5-Attachment/Image/2024-02-22_Thu%20%E8%B7%91%E9%80%9ABaseline%E4%B8%8E%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-3.png)
# 5 总体情况
因为是新的任务，基本上没有直接可用的数据集，都使用了上节提及的构建方法。

| 数据集                                                                                   | 介绍                           | 语言                 | 学生等级     | 学生数量 | 文本数量 | 主题数量 | 平均tokens |
| ---------------------------------------------------------------------------------------- | ------------------------------ | -------------------- | ------------ | -------- | -------- | -------- | ---------- |
| [bawe](https://warwick.ac.uk/fac/soc/al/research/collections/bawe)                       | 本科及硕士生的写作练习         | 英语                 | 本科硕士生   | 627      | 2761     | 41       | 2730       |
| [diaz](https://slabank.talkbank.org/access/Spanish/DiazRodriguez.html)                   | 中学生和大学生的采访录音转录   | 英语                 | 中学和本科生 | 8        | 214      | 29       | 114        |
| [lcss](https://github.com/blculyn)                                                       | 汉语对话，没有主题             | 汉语                 | 不清楚       | 36       | 59       | -        | 3626       |
| [leap](https://sourceforge.net/projects/leapcorpus/files/latest/download)                | 录音转录材料，采访和讲故事     | 英语                 | 不清楚       | 50       | 173      | 3        | 270        |
| [parole](https://slabank.talkbank.org/access/English/PAROLE.html)                        | 成年人的口语练习，没有主题     | 意大利语, 法语, 英语 | 成人         | 42       | 84       | -        | 707        |
| [pelic](https://github.com/ELI-Data-Mining-Group/PELIC-dataset/tree/master/corpus_stats) | 成年人的书面写作练习和对话转录 | 英语                 | 成人         | 1177     | 46204    | 7        | 91         |
# 6 分别统计各个数据集
## 6.1 图中的字段
| 字段           | 说明                                         | 示例                                  |
| -------------- | -------------------------------------------- | ------------------------------------- |
| Category       | 文本类型                                     | Essay, Literature, Proposal, Research |
| Version        | 作者撰写的文章数量（只有撰写>1次，才能有作业的 chronological order）（文章不一定是同一个主题）                                             | 3                                      |
| Essay Number   | 文章数量                       | 190                                   |
| Average Tokens | Token数量，使用nltk和jieba分词 | 1221                                  |
以下是针对表格中字段的数据集统计。样式有点粗糙，自己看能看懂。之后如果画论文里的图，会精细画的。
## 6.2 BAWE
![5-Attachment/Image/数据集处理-20240222-2.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-2.png)
![5-Attachment/Image/数据集处理-20240222-3.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-3.png)
## 6.3 DIAZ 
category统计图的x轴乱了。我看了原csv，其实只有一个category：录音转录。
![5-Attachment/Image/数据集处理-20240222-4.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-4.png)
![5-Attachment/Image/数据集处理-20240222-5.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-5.png)
## 6.4 LEAP
![5-Attachment/Image/数据集处理-20240222-6.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-6.png)![5-Attachment/Image/数据集处理-20240222-7.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-7.png)
## 6.5 LITKEY
![5-Attachment/Image/数据集处理-20240222-8.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-8.png)
![5-Attachment/Image/数据集处理-20240222-9.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-9.png)
## 6.6 LSCC
汉语对话，没有主题，所以没有category字段。
![5-Attachment/Image/数据集处理-20240222-10.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-10.png)
## 6.7 PAROLE
成年人的口语练习，没有主题，所以没有category字段。
![5-Attachment/Image/数据集处理-20240222-11.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-11.png)
## 6.8 PELIC
![5-Attachment/Image/数据集处理-20240222-12.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-12.png)
![5-Attachment/Image/数据集处理-20240222-13.png](/img/user/5-Attachment/Image/%E6%95%B0%E6%8D%AE%E9%9B%86%E5%A4%84%E7%90%86-20240222-13.png)