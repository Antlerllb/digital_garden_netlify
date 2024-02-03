---
{"dg-publish":true,"permalink":"/5-Attachment/Paper/The Pile An 800GB Dataset of Diverse Text for Language Modeling/"}
---

# 1 The Pile: An 800GB Dataset of Diverse Text for Language Modeling
## 1.1 Metadata
* Authors: [[Leo Gao\|Leo Gao]], [[Stella Biderman\|Stella Biderman]], [[Sid Black\|Sid Black]], [[Laurence Golding\|Laurence Golding]], [[Travis Hoppe\|Travis Hoppe]], [[Charles Foster\|Charles Foster]], [[Jason Phang\|Jason Phang]], [[Horace He\|Horace He]], [[Anish Thite\|Anish Thite]], [[Noa Nabeshima\|Noa Nabeshima]], [[Shawn Presser\|Shawn Presser]], [[Connor Leahy\|Connor Leahy]]
* Date: 2020/12/31
- Tags: #数据集调研 #Kaggle 
- Status: #Noted
* Attachments: [Full Text PDF](zotero://open-pdf/library/items/QN3WW8CB)
* Kaggle Solution: [[4-Archives/Kaggle-LLM/DeBERTa+Pile\|DeBERTa+Pile]]
## 1.2 Abstract
Recent work has demonstrated that increased training dataset diversity improves general cross-domain knowledge and downstream generalization capability for large-scale language models. With this in mind, we present \textit{the Pile}: an 825 GiB English text corpus targeted at training large-scale language models. The Pile is constructed from 22 diverse high-quality subsets -- both existing and newly constructed -- many of which derive from academic or professional sources. Our evaluation of the untuned performance of GPT-2 and GPT-3 on the Pile shows that these models struggle on many of its components, such as academic writing. Conversely, models trained on the Pile improve significantly over both Raw CC and CC-100 on all components of the Pile, while improving performance on downstream evaluations. Through an in-depth exploratory analysis, we document potentially concerning aspects of the data for prospective users. We make publicly available the code used in its construction.
# 2 子数据集
| 子数据集           | 内容    | 重要性权重 | 文件大小   | 平均文档长度 |
| ------------------ | --- | ---------- | ---------- | ------------ |
| Pile-CC            | 多主题的网页爬取数据    | 18.11%     | 227.12 GiB | 4.33 KiB     |
| PubMed Central     | 研究所的生物医药论文    | 14.40%     | 180.55 GiB | 30.55 KiB    |
| Books3†            | 小说和非小说类的书籍    | 12.07%     | 151.44 GiB | 538.36 KiB   |
| OpenWebText2       | 多主题的网页爬取数据    | 10.01%     | 125.54 GiB | 3.85 KiB     |
| ArXiv              | 论文    | 8.96%      | 112.42 GiB | 46.61 KiB    |
| Github             | 代码    | 7.59%      | 95.16 GiB  | 5.25 KiB     |
| FreeLaw            | 法院意见（court opinions）    | 6.12%      | 76.73 GiB  | 15.06 KiB    |
| Stack Exchange     | Stack社区的问答对    | 5.13%      | 64.39 GiB  | 2.16 KiB     |
| USPTO Backgrounds  | 面向业余听众的专利介绍（patent background）    | 3.65%      | 45.81 GiB  | 4.08 KiB     |
| PubMed Abstracts   | 研究所的生物医药论文的摘要（侧重近年的论文）    | 3.07%      | 38.53 GiB  | 1.30 KiB     |
| Gutenberg (PG-19)† | 多主题的网页爬取数据    | 2.17%      | 27.19 GiB  | 398.73 KiB   |
| OpenSubtitles†     | 电影和电视的字母    | 1.55%      | 19.47 GiB  | 30.48 KiB    |
| Wikipedia (en)†    | 维基百科    | 1.53%      | 19.13 GiB  | 1.11 KiB     |
| DM Mathematics†    | 数学知识的阐述    | 1.24%      | 15.49 GiB  | 8.00 KiB     |
| Ubuntu IRC         | 与Ubuntu有关的频道聊天记录    | 0.88%      | 11.03 GiB  | 545.48 KiB   |
| BookCorpus2        | 尚未出版的书籍    | 0.75%      | 9.45 GiB   | 369.87 KiB   |
| EuroParl†          | 欧洲国会的会议记录的平行语料    | 0.73%      | 9.17 GiB   | 68.87 KiB    |
| HackerNews         | 计算机和企业家精神的文章    | 0.62%      | 7.80 GiB   | 4.92 KiB     |
| YoutubeSubtitles   | YouTube字幕的平行语料库    | 0.60%      | 7.47 GiB   | 22.55 KiB    |
| PhilPapers         | 研究所的哲学论文    | 0.38%      | 4.76 GiB   | 73.37 KiB    |
| NIH ExPorter       | 科学写作    | 0.30%      | 3.79 GiB   | 2.11 KiB     |
| Enron Emails†      | 邮件    | 0.14%      | 1.76 GiB   | 1.78 KiB     |
