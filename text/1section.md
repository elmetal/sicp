# 1section.md
# 1.1

## 中略
## 1.1.8
### ブラックボックス抽象化としての手続き

sqrtは再帰的 再帰的:手続きがそれ自身を使って定義されていること
循環的な定義の是非については1.2節で見る
ここでは他の重要な点を議論する
- 推定値が十分に良いか
- 推定値をどう改善するか  
等の手続きに分解されている

- プログラムを部品に分けていて、
- 分けられた部品が特定のタスクを行っている  
ことが重要

これによって別の手続きでもモジュールとして利用できる

### 局所名
手続きを利用する人が気にしないでいいかどうか  
→ 仮引数の名前に何を選んだかが関係ないかどうかが一つある  
つまり、仮引数の名前は手続き本体の中に局所化されているべき

### 内部定義とブロック構造
平方根を計算するプログラムは次の様になっている
```
(define (sqrt x)   
  (sqrt-iter 1.0 x))
(define (sqrt-iter guess x)  
  (if (good-enough? guess x)  
      guess  
      (sqrt-iter (improve guess x) x)))  
(define (good-enough? guess x)
  (< (abs (- (square guess) x)) 0.001)) 
(define (improve guess x)
  (average guess (/ x guess)))
```
これは、`sqrt`を使う人にとって大事なのは`sqrt`だけで、  
他の手続き`sqrt-iter`, `good-enouqh?`, `improve`は不要という点で問題がある

