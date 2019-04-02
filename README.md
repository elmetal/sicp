# sicp
sicpのメモ

## directory
### text
本文のまとめ
### problem
問題の回答コード

## 環境構築
```
brew install gauche
```

```
git clone git@github.com:shirok/Gauche-compat-sicp.git
cd Gauche-compat-sicp
./configure
make install
```
コードに以下を追記する
```
(use compat.sicp) 
```

### REPL
```
brew install rlwrap
```

```
rlwrap gosh
gosh>
```
```
gosh> (exit)
```

