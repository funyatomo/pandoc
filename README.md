# pandoc

generating github-like html document using pandoc with css file

## 基本的なコマンド
githubライクなスタイルシートを取り込んでの，markdown文書からhtml文書への変換

```
$ pandoc -s -t html5 -c css/github.css README.md -o test.html
```

拡張子を指定していれば，`-t html5`は無くても大丈夫  `-s (--standalone)`は適切なヘッダやフッタ付きの完全なhtml文書を出力するのに必要

htmlにスタイルシートを埋め込むには`--self-contained`とする

```
$ pandoc -s -c css/github.css --self-contained README.md -o test.html
```

> - [github.css](https://gist.github.com/griffin-stewie/9755783)
> - [markdown-cheatsheet.md](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa#file-markdown-cheatsheet-md)
