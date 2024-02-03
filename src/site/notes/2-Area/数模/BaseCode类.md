---
{"dg-publish":true,"permalink":"/2-Area/数模/BaseCode类/"}
---

```python
# encoding: utf-8  
import os.path  
from common.input_path1 import InputPath  
  
  
class BaseCode(object):  
    @staticmethod  
    def get_output_path(sub_path):  
        return os.path.join(InputPath.OUTPUT_PATH, sub_path)
```