# クラスカル法

- 最小全域木問題に使用
- 辺のコストを小さい順に見ていき、頂点同士を接続するか判断する。
- 接続することによって閉路が発生することを避けるため、接続する頂点同士が既に同じ連結成分にないか確認する。
- 同じ連結成分にあるかはUnion-Find木を使って管理する。
- 計算量はO(|E|log|V|)。 辺のソートがボトルネック。

```
# 略
path.sort()
uf = UnionFind()
ans = 0

for weight, from, to in path:
    if uf.same(from, to) != 1:
        uf.union(from, to)
        ans += weight
```
