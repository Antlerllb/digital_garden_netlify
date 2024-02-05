---
{"dg-publish":true,"permalink":"/1-Project/2024-美赛/Appendix A/"}
---

code/lstm.py
```python
import torch
import torch.nn as nn

class BiLSTM(nn.Module):
    def __init__(self, input_size, hidden_size, num_layers, output_size, bidirectional=True):
        super(BiLSTM, self).__init__()
        
        self.lstm = nn.LSTM(input_size=input_size, 
                            hidden_size=hidden_size, 
                            num_layers=num_layers, 
                            batch_first=True, 
                            bidirectional=bidirectional)
        
        # Output layer
        self.fc = nn.Linear(hidden_size * 2 if bidirectional else hidden_size, output_size)
        
    def forward(self, x):
        # Forward pass through the LSTM layer
        lstm_out, _ = self.lstm(x)
        
        # Concatenate the hidden states from both directions if bidirectional
        if self.lstm.bidirectional:
            lstm_out = torch.cat((lstm_out[:, -1, :self.lstm.hidden_size], 
                                  lstm_out[:, 0, self.lstm.hidden_size:]), dim=1)
        else:
            lstm_out = lstm_out[:, -1, :]
        
        # Final output through the fully connected layer
        out = self.fc(lstm_out)
        
        return out
```
