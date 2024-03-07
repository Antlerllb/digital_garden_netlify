---
{"dg-publish":true,"permalink":"/1-Project/语言习得/2024-03-01_Fri Transformer小疑问/"}
---

# 1 预计完成
应该还得明天，我理论上了解整个过程，但实现过程中有各种bug。
# 2 小疑问：模型和标记器的配置
- 问题
	- tokenizer和model的配置在哪找？（这个问题困惑我很久了，但一直找不到供查询的文档。）
- 做过的尝试
	- 之前是看config.json、tokenizer_config.json。但看别人代码时会发现一些json里面没用的参数，比如bert-base-cased的is_split_into_words。
	- huggingface页面也没有什么信息。
	- 在pycharm的Debug工具界面看，也没看到这个参数。

