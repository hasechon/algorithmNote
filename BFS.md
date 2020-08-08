# 幅優先探索

dequeを使って実装

```
from collections import deque

t = tree()

l = deque()
l.append(0)
while len(l) > 0:
    p = l.popleft()
    for i in t.to(p):
        # 処理
        l.append(i)
```