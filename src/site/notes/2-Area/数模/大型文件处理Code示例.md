---
{"dg-publish":true,"permalink":"/2-Area/数模/大型文件处理Code示例/"}
---

```python
from tqdm import tqdm  
import time  
my_list = [1, 2, 3]  
for i in tqdm(my_list):  
    time.sleep(2)
```