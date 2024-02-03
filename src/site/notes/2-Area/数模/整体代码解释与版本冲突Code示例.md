---
{"dg-publish":true,"permalink":"/2-Area/数模/整体代码解释与版本冲突Code示例/"}
---

```python
import gc  
large_list = [i for i in range(10 ** 6)]  
del large_list  
gc.collect()  
print("垃圾回收后的内存使用情况：", gc.mem_alloc())
```