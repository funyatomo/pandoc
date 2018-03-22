# pandoc

generating github-like html document using pandoc with css file

```
$ pandoc -s -t html5 -c css/github.css README.md -o test.html
$ pandoc -s -c css/github.css --self-contained README.md -o test.html
```
