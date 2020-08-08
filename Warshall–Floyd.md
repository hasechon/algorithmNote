# ワーシャルフロイド法

- 全ての２頂点間の最短路を求める問題(全点対最短路問題)で使用。
- O(|V|^3)
- 負のコストの辺があっても計算可能。


```
for k in range(n):
    for i in range(n):
        for j in range(n):
            d[i][j] = min(d[i][j], d[i][k] + d[k][j])
```