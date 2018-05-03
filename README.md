# GitHub

## GitHub用の設定

### markdownファイルに自分用のスタイルを適用する

* chromeの拡張機能に stylish を入れる。
* stylish に下記のスタイルを追加する。

```css
#readme h2 {
    text-decoration: underline;
}
#readme h3 {
    color: white;
    background-color: #9999AA;
    padding: 8px 8px 8px 8px;
    border-radius: 4px;
}
```

* 適用するURLを下記にする。

```code
適用先 => "正規表現に一致するURL" を選択する。
URL => https://github.com/.+/.+.(md|adoc|rst)
```

README.md をクリックして（URLに README.md が入っている状態にして）、スタイルが適用されていればOK。

### import用（↑と同じ）

stylish の スタイルの管理 > import で↓を張り付ける。

```code
@-moz-document regexp("https://github.com/.+/.+.(md|adoc|rst)") {
#readme h2 {
    text-decoration: underline;
}
#readme h3 {
    color: white;
    background-color: #9999AA;
    padding: 8px 8px 8px 8px;
    border-radius: 4px;
}
}
```