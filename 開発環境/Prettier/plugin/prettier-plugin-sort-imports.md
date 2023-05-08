# prettier-plugin-sort-imports

[prettier-plugin-sort-imports](https://www.npmjs.com/package/@trivago/prettier-plugin-sort-imports)とはimport文を自動的に整理するプラグイン。

ドキュメント記載時のバージョンはこちら。

* prettier-plugin-sort-imports
  * 4.1.1

## 利用方法

`Prettier`の設定ファイルに`importOrder`の設定を記述する。

```json
{
  "importOrder": ["^@?\\w", "^[./]"]
}
```
