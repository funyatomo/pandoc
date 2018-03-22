# pandoc

generating github-like html document using pandoc with css file

## 基本的なコマンド

```
$ pandoc -s -t html5 -c css/github.css README.md -o test.html
$ pandoc -s -c css/github.css --self-contained README.md -o test.html
```

> - [github.css](https://gist.github.com/griffin-stewie/9755783)
> - [markdown-cheatsheet.md](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa#file-markdown-cheatsheet-md)
