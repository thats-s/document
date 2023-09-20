# prettier-plugin-sort-imports

[prettier-plugin-sort-imports](https://www.npmjs.com/package/@trivago/prettier-plugin-sort-imports)とはimport文を自動的に整理するプラグイン。

ドキュメント記載時のバージョンはこちら。

* prettier-plugin-sort-imports
  * 4.2.0

## 利用方法

`Prettier`の設定ファイルに`plugins`の設定を記述する。

```json
{
  "plugins": ["@trivago/prettier-plugin-sort-imports"]
}
```

## API

`Prettier`の設定ファイルに記述するオプション。

* `importOrder`
  * どの順番で並べるかを正規表現で設定
* `importOrderSeparation`
  * ソートされたimport宣言グループ間に改行区切りを入れるかどうか
* `importOrderSortSpecifiers`
* `importOrderGroupNamespaceSpecifiers`

### 記述例

```json
{
  "importOrder": ["^@?\\w", "^[./]"],
  "importOrderSeparation": true,
  "importOrderSortSpecifiers": true,
  "importOrderGroupNamespaceSpecifiers": true
}
```
