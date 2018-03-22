# pandoc

pandocはいくつかのマークアップ言語の文書を別の形式の文書に変換するコマンドラインツール

- 目的:generating github-like html document using pandoc with css file

## pandocのインストール
msiファイルでインストールを行うか，zipファイルを解凍してpandoc.exeをパスの通ったディレクトリに配置する

[pandoc.org](https://pandoc.org)

pandocの日本語版リファレンス

[Pandoc ユーザーズガイド日本語版](http://sky-y.github.io/site-pandoc-jp/users-guide/)

## 基本的なコマンド
githubライクなスタイルシートを取り込んでの，markdown文書からhtml文書への変換

```
$ pandoc -s -t html5 -c css/github.css README.md -o test1.html
```

- 拡張子を指定していれば，`-t html5`は無くても大丈夫
- `-s (--standalone)`は適切なヘッダやフッタ付きの完全なhtml文書を出力するのに必要

htmlにスタイルシートを埋め込むには`--self-contained`とする

```
$ pandoc -s -c css/github.css --self-contained README.md -o test2.html
```

## cssをホームディレクトリに
ホームディレクトリ直下にcssファイルを配置し，エイリアスも設定する

```
$ mkdir ~/.pandoc
$ mv css/github.css ~/.pandoc/
$ alias pandoc='pandoc -s -c ~/.pandoc/github.css --self-contained'
```


> ## Source
> - [github.css](https://gist.github.com/griffin-stewie/9755783)
> - [markdown-cheatsheet.md](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa#file-markdown-cheatsheet-md)

> ## Github webpage
> - [funyatomo/pandoc](https://github.com/funyatomo/pandoc)

> ## Reference
> - Comming soon
