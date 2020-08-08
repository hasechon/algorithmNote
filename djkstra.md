# ダイクストラ法

heapを使ってコストが最小の頂点を管理することでO(|E|log|V|)で計算できる。（E:辺の数, V:頂点の数）

```
from heapq import heappop,heappop,heapify

class tree:
    # 略
    # 最終到達点の値が確定していない間ループ
    while self.isFix[self.n-1] != 1:

        # コストが最小の頂点がリストの先頭にくる
        minv = self.unsettled[0]

        for  i in self.path[minv]:
            if self.isFix[i]: continue
            self.unsettled.append(i)
            self.cost = min(self.cost[i], self.cost[minv] + self.edgeCost[minv][i])

    # 最終到達点への最小コストを返す
    return self.cost[self.n-1]

```