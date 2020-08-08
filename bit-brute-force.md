# bit全探索

```
# n個の要素に対して選ぶor選ばないの組み合わせを全探索
for i in range(2**n):
    for j in range(n):
        if (i>>j) & 1:
            # 処理
```

