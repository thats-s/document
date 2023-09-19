# favicon

ブラウザのタブなどに表示されるアイコン。

## 設定方法

最低限3つのアイコンを用意すれば各環境で表示できる。

- あらゆるブラウザ向けに`svg`
- iOSのホーム画面用に`png`（180 x 180）
- `svg`非対応環境（Safari）用に`.ico`（32 x 32）

```html
<!-- head内に記述 -->
<link rel="icon" href="/favicon.svg" sizes="any" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png"><!-- 180x180px -->
<!-- favicon.icoをルートディレクトリ置くだけで、head内には書かない -->
```

ここでの注意点は`.ico`は記述しないこと。記述してしまうと他のアイコン（`svg`等）を上書きしてしまう。
Chromeのバグ？

ルートディレクトリに置いておくことで、Safariなどの`svg`[非対応環境](https://caniuse.com/link-icon-svg)のフォールバックとして機能する。

## ダークモード対応

`svg`内にcssを書くことでダークモードに対応が可能。

```svg
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
  <style>
    path {
      fill: #212121; <!-- ライトモードの色 -->
    }
    @media (prefers-color-scheme: dark) {
      path {
        fill: white; <!-- ダークモードの色 -->
        opacity: 0.5; <!-- 他にも色々かける -->
      }
    }
  </style>
  <path d="....
```
