---
{"dg-publish":true,"permalink":"/2-Area/数挖/2024-02-06_Tue 环境找不到genericpath/"}
---

# 1 环境找不到genericpath
## 1.1 报错文本示例
```python
libs.exception.CheckException: Fatal Python error: init_import_size: Failed to import the site module
Python runtime state: initialized
Traceback (most recent call last):
File "/opt/conda/envs/dg_crawler/lib/python3.8/site.py", line 73, in <module>
import os
File "/opt/conda/envs/dg_crawler/lib/python3.8/os.py", line 57, in <module>
import posixpath as path
File "/opt/conda/envs/dg_crawler/lib/python3.8/posixpath.py", line 28, in <module>
import genericpath
ModuleNotFoundError: No module named 'genericpath'
```
## 1.2 报错情景
- 跑爬虫代码
	- 但不是所有的python代码都会报错。
- Conda安装任意包时（之前有这个bug，今天没了）
	- python=3.8.x（试了很多个3.8的都会报错）
# 2 Jupyter自动打开之前关闭的终端
![5-Attachment/Image/2024-02-06_Tue 环境找不到genericpath-20240206.png](/img/user/5-Attachment/Image/2024-02-06_Tue%20%E7%8E%AF%E5%A2%83%E6%89%BE%E4%B8%8D%E5%88%B0genericpath-20240206.png)