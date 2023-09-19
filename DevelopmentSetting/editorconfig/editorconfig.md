# editorconfig

[editorconfig](https://editorconfig.org/)とはコーディングスタイルを統一するために用意するファイルのこと。

## ファイル形式

`.editorconfig`ファイルを作成して記述する。

## サポートされているプロパティ

* `indent_style`
  * `tab` or `space`が設定可能
* `indent_size`
  * インデントに使用される列の幅
* `tab_width`
  * タブを表すために使用される列の幅
  * デフォルトで`indent_size`に指定した値になるので通常は不要
* `end_of_line`
  * 改行コード（`lf`・`cr`・`crlf`が設定可能）
* `charset`
  * 文字コード（`utf-8`・`utf-8-bom`等が設定可能）
* `trim_trailing_whitespace`
  * 改行文字の前にある空白文字を削除するかどうか（`true` or `false`）
* `insert_final_newline`
  * 保存時にファイルを改行で終わらせるかどうか（`true` or `false`）
