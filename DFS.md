# 深さ優先探索

再帰で実装
```
class tree():
    def __init__(self,n):
        self.n = n
        self.from = []
        self.to = []

    def input(self,from,to):
        # グラフの情報をinput

    def dfs(self, p):
        for i in self.to[p]:
            # 探索済みチェック
            # 処理

            self.dfs(i)
        
        return
```