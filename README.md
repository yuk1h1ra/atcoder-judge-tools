# atcoder-judge-tools

[WIP] このプロジェクトはまだ未完です

## 概要

[online judge tools](https://github.com/kmyk/online-judge-tools)のAtcoderバージョン

主に、URL記述をする際のコマンドを簡略化および省略する

pipでインストールできるように、その形式に沿った形で記述していく

#### 参考記事

- online judge tools 日本語での解説ページ
https://kimiyuki.net/blog/2017/01/19/pr-online-judge-tools/

- shell scriptにてAtcoderのスクリプトを記述する
https://qiita.com/AokabiC/items/af685bfd205dda44ec45

## 実装するべきコマンド

基本的には `aj` コマンドを作成し、実行させる。

### download

`aj dl --contest CONTEST --task TASK`

[ ] 省略可能箇所の選定をする。  
[ ] 引数の命名に気をつける  
[ ] TASKに当たる部分で複数選択可能かどうかの調査

```
$ aj dl --contest abc123 --task a
=> oj dl https://beta.atcoder.jp/contests/abc123/tasks/abc123_a
```

### test

サンプルケースを用いてテストを行う。ほとんどojと同様

`$ aj test [-c COMMAND]`

```
$ aj test [-c ./a.out]
=> oj test -c ./a.out
```

### login

ログイン時にURLがいらなくなる。

`$ aj login`

```
$ aj login
=> oj login https://beta.atcoder.jp/
```

### submit
