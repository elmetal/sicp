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
### slib
```
$ cd ~/Downloads
$ curl -O http://groups.csail.mit.edu/mac/ftpdir/scm/slib-3b5.zip
$ unzip slib-3b5.zip
$ sudo mkdir /usr/local/slib
$ sudo cp -r slib /usr/local
```

### sicp互換
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

