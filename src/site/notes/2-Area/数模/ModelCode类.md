---
{"dg-publish":true,"permalink":"/2-Area/数模/ModelCode类/"}
---

```python
# encoding: utf-8  
import os.path  
  
import pandas as pd  
  
from src.general import BaseCode  
from common.input_path1 import InputPath  
  
  
class ModelCode(BaseCode):  
    log_name = 'model'  
    def __init__(self):  
        super().__init__()  
  
    def run_model(self):  
        ...  
  
  
if __name__ == '__main__':  
    model = ModelCode()  
    model.run_model()
```