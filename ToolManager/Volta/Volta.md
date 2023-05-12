# Volta

[Volta](https://volta.sh/)とは`Node.js`バージョン管理ツール。

ドキュメント記載時のバージョンはこちら

* v1.1.1

## インストール方法

既に他のバージョン管理ツールをインストールしている場合はアンインストールしてから行う。

[公式のドキュメント](https://docs.volta.sh/guide/getting-started)を参照してインストールを実施。

注意点に書かれている通り、開発者モードを有効にしておく。

## Volta コマンド

主に使用するコマンド。

### install

バージョンを指定してインストールしたい場合。

```bash
volta install node@14.15.5
```

アバウトにバージョンを指定したい場合は以下のコマンドを実行すると、リクエストに一致する適切なバージョンが選択される。

```bash
volta install node@14
```

最新の`LTS`リリースを選択したい場合。

```bash
volta install node
```

現在選択中の`node`のバージョンに対応した`npm`のバージョンをインストールしたい場合。

```bash
volta install npm@bundle
```

### pin

該当のプロジェクトで使用するバージョンを固定したい場合。

```bash
volta pin node@12.20.2
volta pin npm@6.4
```

上記のコマンドを実行すると`package.json`に以下の記述が追加される。

```json
"volta": {
  "node": "12.20.2",
  "npm": "6.4"
}
```

これでプロジェクトのメンバー全員が同じバージョンを自動的に取得する。
